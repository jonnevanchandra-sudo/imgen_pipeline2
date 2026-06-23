# Pipeline Changes

Entries below are ordered by where the stage sits in the pipeline (execution order).

```
1.2 Campaign_Brief
   ↓
   ... Strategy → Narrative → Art Direction ...
   ↓
5a Image_Analysis (Stage 5.0, optional pre-stage — only if reference images uploaded)
   ↓
5.2 Scene-Assembly  (also has 5a Image Analysis's function, haven't combined/separate)
   ↓
6.1 Composition_Rendering
   ↓
7.1 Synthesis
   ↓
8.1.1 Prompt_Compiler ─┐
8.2.1 Prompt_Compiler ─┴─ (alternative final compilers)
```


---

**1.1 Campaign_Brief.md** — new file, extends 1.0 without touching it
- adds `ProductSpec` inside `MandatoryRequirements`
- use this when a campaign needs a specific product model in the image
- pairs with 5.2 — ProductSpec entries flow downstream as named entities

---

**1.2 Campaign_Brief.md** — new file, canonical Campaign Brief; absorbs 1.0 + 1.1 into one stage
- strict superset of 1.0 and 1.1 — `ProductSpec` is optional inside `MandatoryRequirements`; omit it and this behaves exactly like 1.0
- 1.0 and 1.1 kept in the repo as historical/reference only, same relationship 5.2 has to 5/5.1

---

**5a Image_Analysis.md** (Stage 5.0) — new file, pre-processing stage before Stage 5
- runs before Scene Assembly when client uploads reference assets (people, venues, products, brand assets)
- requires a Client Intent Declaration per image (what to lock, how strictly, what to exclude) before extraction
- classifies each asset, separates Observable/Inferred/Uncertain attributes with confidence scores, assigns entity IDs and PreservationContracts
- produces ImageAnalysisContract consumed by Scene Assembly as optional input
- **naming clarification:** `5.0` is a separate stage that runs *before* Stage 5 — it is not a variant of Scene Assembly. `5.1` is the extended drop-in replacement *for* Stage 5 itself. When both are in play: 5.0 → 5.1 → 6, not 5.0 → 5 → 5.1.

---

**5.2 Scene-Assembly.md** — new file, canonical Stage 5, supersedes 5 / 5.1
- adds named product preservation (from 5.1): if CampaignContract has a `ProductSpec`, locks model name + visual descriptors together as immutable
- cannot override immutable attributes, brand/strategic direction, or scene construction decisions
- conflicts between client signals and upstream constraints are recorded as `ClientPreferenceConflicts` and deferred to Synthesis (Stage 7)
- when none of ProductSpec / reference images / ClientPreferenceContract are present, behaves identically to base Scene Assembly (5)

---

**6.1 Composition_Rendering.md** — existing file, extended with three rendering requirements
- adds Human Subject Rendering Requirement: human skin/features must show natural texture, pores, tone variation, and asymmetry — no airbrushing, no "AI-perfect" or beauty-filtered rendering, applies regardless of Reality Model
- adds Depth of Field Realism: background blur must follow progressive, depth-dependent optical falloff tied to `CameraPlan.focal_length_mm`/`aperture_f_stop` — not a flat uniform blur layer
- adds Multi-Subject Pose Variation Requirement: whenever two or more human subjects share an action, each must be at an independent point in the action cycle (different stride phase, arm position, body lean, weight distribution) — no identical, mirrored, or synchronized poses; fixes the "cloned stride" AI artifact systemically for all runs
- adds `MaterialPlan.human_skin_rendering` and `OpticalPlan.bokeh_behavior` fields, plus `RenderingConstraints.natural_skin_rendering_required` and `RenderingConstraints.pose_variation_required`
- adds three new Perceptual Validation assertions for the independent VLM Critic: Skin Naturalism Assertion, Depth of Field Realism Assertion, Pose Variation Assertion
- adds Depth of Field Category Selection: aperture must come from one of three categories — Environmental Context (`f/8`-`f/11`, background carries part of the story), Atmospheric/Soft Focus (`f/4`-`f/5.6`, the **default**), or Commercial Isolation (`f/1.8`-`f/2.8`, background communicates nothing); selection is driven by `HierarchyPlan`/`AttentionPlan`, giving the existing "scene readability" requirement concrete decision criteria and preventing AI image generators from defaulting to overly blurry backgrounds
- adds `CameraPlan.depth_of_field_category` field; `aperture_f_stop` must fall within the selected category's range; `OpticalPlan.bokeh_behavior` and the Depth of Field Realism falloff shape must match the selected category's character

---

**7.1 Synthesis.md** — existing file, extended with structured camera spec pass-through
- consolidates all upstream contracts (0–6.1) into one authoritative SynthesisContract
- resolves conflicts (including `ClientPreferenceConflicts` from 5.2.5), suppresses redundant communication, maps observable human signals
- may consolidate, resolve, prioritize, suppress — but introduces no new creative decisions
- adds `PhysicalRendering.CameraSpecs` (`focal_length_mm`, `aperture_f_stop`) — copied **verbatim** from 6.1's `CameraPlan`, never paraphrased or absorbed into prose; previously the numbers rode loosely inside the `CameraIntent` sentence and could be lost or rounded in translation
- output consumed directly by the Prompt Compiler (8.1.1 / 8.2.1)

---

**8.1.1 Prompt_Compiler.md** — new file, v2.3, extends 8.1 (v2.2) without touching it
- adds Brand Asset Embedding: when a `ReferenceAssetManifest` is present (from 5.2/5.2.5), brand asset reproduction instructions are written inline within the flat VisualPrompt prose, at the point where each asset is described
- pattern: "[visual description]. This is reference_asset_XX — reproduce it exactly: same shape, same color, same proportions. Do not redraw from memory."
- strictness (`Exact` / `Close`) taken from the ReferenceAssetManifest controls instruction strength
- appends `ReferenceAssetManifest` as a sibling YAML key after `VisualPrompt` — app-level metadata for API file attachment, not part of the prompt text
- brand asset instructions are never pruned, regardless of token pressure
- identical to 8.1 when no ReferenceAssetManifest is present

---

**8.2 Prompt_Compiler.md** — existing file, added Output Style section
- mandates short, varied prose — no long explanatory paragraphs
- sentence rhythm should vary across blocks for model parsing clarity
- simple blocks (FORMAT, LIGHTING, CAMERA) can be flattened to a single string instead of nested sub-keys
- no rationale in the output — instructions only, no "this communicates X" language
- NEGATIVE stays as a flat list of short prohibitions
- adds `BRAND_ASSETS` conditional fixed block — references uploaded brand assets by ID, tells the model to reproduce exactly rather than infer from training data
- adds `ReferenceAssetManifest` sibling key — app-level list of files to attach as reference image inputs to the API call

---

**8.2.1 Prompt_Compiler.md** — new file, v3.1, extends 8.2 (v3.0) without touching it
- motivation: the generator's attention over the prompt is a fixed budget — every redundant or default-restating sentence dilutes the unique, default-fighting instructions (product identifiers, pose variation, safe zones); Trial_07's ~600-word prompt stated "not posed to camera" 4×, bokeh behavior 4×, and warm lighting in 7 places
- adds the **Compression System**, run as a Compression Pass between NLP Block Writer and JSON Assembly:
  - **Single-Statement Rule** — every fact appears exactly once, in a defined home block (ownership table maps fact types to blocks: all optics → CAMERA, all light → LIGHTING, environment identity → HIGH.setting, etc.); NEGATIVE keeps a deliberate exemption to fence failure modes whose positive form exists elsewhere
  - **Default-Elision Rule** — the "surprisal test": omit any sentence the generator would follow unprompted (floor anchoring, ordinary scale, scenery already implied by a named real-world setting); keep only instructions that fight model defaults
  - **Word Budget** — 200–300 word target, 400 hard ceiling (BRAND_ASSETS exempt); pruning order LOW → MEDIUM → SCENE leftovers → phrasing
- fixed blocks change from "always written in full" to "always present, written lean" — sub-fields with no surviving content are dropped, compact blocks flatten to single strings; a 1–2 sentence SCENE block is the expected outcome, not a failure
- compression removes restatements, never the only statement of a resolved requirement — layer-isolation boundaries unchanged
- CAMERA block consumes `RenderingResolution.CameraSpecs` and must state `focal_length_mm` + `aperture_f_stop` **verbatim as values** (e.g. "35mm at f/2.8") — never default-elided, never paraphrased into qualitative language like "shallow depth of field"
- supersedes 8.2 as the compiler of choice for GPT Image 2.0 runs; 8.2 retained as reference

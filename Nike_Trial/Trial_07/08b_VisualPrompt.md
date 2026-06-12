# Visual Prompt — Nike Chill Run Club (Stage 8.2.1)

Framework: `8.2.1 Prompt_Compiler.md` v3.1 (GPT Image 2.0 JSON priority-block format + Compression System)
Input: SynthesisContract (Stage 7.1) — same contract as `08_VisualPrompt.md`; only the compiler differs.

No reference images were supplied for this run, so **no `BRAND_ASSETS` block** and **no `ReferenceAssetManifest`** are included. The Nike Pegasus requirement is carried as a textual `HIGH.brand` instruction — model name first, visual identifiers following.

```json
{
  "VisualPrompt": {
    "CRITICAL": {
      "subjects": "Four or five Hong Kong professionals, twenties, visibly diverse in gender and styling, jogging together at night. Mid-laugh, engaged with each other, never the camera.",
      "emotion": "A shared exhale — relief after a long workday. Light, social, unguarded. Recovery, not effort."
    },
    "HIGH": {
      "action": "Conversational pace, slow enough to talk. Arms loose, no competitive form.",
      "brand": "One subject wears Nike Pegasus (latest generation), visible mid-stride in the lower frame: engineered mesh upper with Flywire cable overlays at the midfoot, thick foam midsole with a lateral crash rail, moderately stacked padded heel, contrasting lateral Swoosh legible at this distance. Worn-in, not box-fresh.",
      "setting": "A Hong Kong harbourfront promenade at night — an ordinary, lived-in city evening."
    },
    "LOW": {
      "style": "Warm editorial lifestyle photography — documentary-candid, premium but unpolished."
    },
    "FORMAT": "Square 1:1 or vertical 4:5 for an Instagram feed post. No faces, the Swoosh, or the visible shoe in the top 10% or bottom 20% of the frame — Instagram UI may cover those zones.",
    "LIGHTING": "Warm streetlamp key from the side and front; background a stop or more darker and cooler. Skin reads warm, never orange. No neon-blue cast, no theatrical shadows, no studio flatness.",
    "CAMERA": "Eye-level near full shot, knees up, one subject's shoes at the bottom edge — the camera is one of the group. 35mm at f/2.8: the group sharp, progressive bokeh falloff behind them — railing and near water semi-legible, far towers dissolving into soft warm circles. No uniform blur layer.",
    "AUTHENTICITY": {
      "human_authenticity": "Real skin — visible pores, subtle tone variation, a light post-workday flush. Asymmetric candid expressions. Each runner at a different point in the stride cycle: independent gait phases, arm positions, and body lean — never synchronized or mirrored.",
      "environmental_authenticity": "Slightly uneven paving, ambient light spill, faint haze over the water.",
      "material_authenticity": "Fabric creases on jackets and bags; matte, non-glossy surfaces.",
      "imperfection_rule": "Credibility beats polish — keep the asymmetries."
    },
    "SCENE": "The railing runs alongside the group on one side; the dense illuminated skyline sits across the water behind them.",
    "NEGATIVE": "No solo runner. No sprinting or race faces. No race numbers or finish lines. No posed lineup. No studio product shot. No product-hero framing. No competitor brands. No airbrushed skin. No synchronized strides."
  }
}
```

---

## Compile Notes

- **Word count: ~310** (vs. ~600 in `08_VisualPrompt.md` from the same contract) — slightly above the 200–300 target, within the 400 ceiling. The overage is the Pegasus descriptor set in `HIGH.brand`, which is protected content and not compressible.
- **Single-Statement Rule applied:**
  - "Not posed to camera" — was stated 4× (CRITICAL, HIGH.action, SCENE, NEGATIVE); now once in CRITICAL.subjects ("never the camera"), with one NEGATIVE fence ("No posed lineup") under the exemption.
  - Bokeh/DOF — was described 4× (CAMERA twice, MEDIUM.skyline, SCENE.depth_structure); now lives only in CAMERA.
  - The skyline — was described in HIGH.setting, MEDIUM.skyline, and three SCENE sub-keys; now stated once, in SCENE.
  - Warm lighting — was spread across 5 LIGHTING sub-keys plus LOW.style plus MEDIUM.skyline; now one flat LIGHTING string.
  - Shoe wear ("worn-in") — was in both HIGH.brand and AUTHENTICITY.material; home block is brand.
- **Default-Elision applied (cut entirely):** floor anchoring, "shoes are true-to-life scale," "group fills most of the frame at natural human scale," "skyline reads distant and smaller," "subjects face each other" as a separate SCENE fact (implied by CRITICAL), streetlamps/railing/water as setting furniture (implied by "harbourfront promenade at night" — railing kept only as a placement fact in SCENE).
- **MEDIUM omitted:** `main_character` ("quietly self-possessed") is a psychological nuance with no distinct visual signature — cut per the MEDIUM block definition. `skyline` content was fully redundant after dedup.
- **Pose variation:** carried in AUTHENTICITY.human_authenticity per the v3.1 block definition (multi-subject shared action → independent gait phases), consistent with the SynthesisContract's `ImperfectionRendering` ("preserve slight asymmetries in pose... do not correct toward symmetry"). One NEGATIVE fence added ("No synchronized strides"). Note: Trial_07's Synthesis predates the 6.1 pose-variation edit, so this instruction enters via the compiler framework, not the contract.
- **No new creative decisions** — every surviving sentence traces to a resolved element in the Synthesis Contract; compression removed restatements only.

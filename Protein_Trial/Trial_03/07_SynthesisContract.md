# Synthesis Contract — Natural Protein Powder (Stage 7.1, Trial_03)

Framework: `7.1 Synthesis.md` (Camera Specs + Luminance Hierarchy verbatim pass-through)
Inputs: Brand (0, assumed mode), Campaign (1), Strategy (2), Narrative (3), Art Direction (4) — all unchanged from Trial_01/02 — plus Scene (5.2.5, Trial_03) and Composition & Rendering (6.1, Trial_03, reframed per the Style/Angle/Distance brief)
Decision Type: Communication Resolution — consolidates, resolves, prioritizes; introduces no new creative decisions.

```json
{
  "SynthesisContract": {

    "ExecutiveSummary": "A woman in her own bright, polished home kitchen is caught — in a frontal, eye-level, waist-up portrait — in the private moment of genuinely enjoying a creamy smoothie, her gaze on the glass at her lips, while the real ingredients it came from — banana, oats, berries, vanilla, the open kraft pouch and scoop — sit within reach beside her. Rendered as crisp, bright, high-end lifestyle-campaign photography, the image still communicates 'healthy that genuinely tastes good, made from food you recognize' as a food moment, never a supplement ad.",

    "CommunicationResolution": {
      "PrimaryCommunication": {
        "statement": "This protein genuinely tastes good — enjoyment you don't have to fake, because it's made of real food.",
        "derived_from": {
          "campaign": "Reposition against the category objection: chalky, artificial, tolerated",
          "brand": "Food brand, not supplement brand; taste-first, ingredient transparency",
          "strategy": "TastePleasure + IngredientHonesty; collapse the Indulgence↔Health tradeoff",
          "narrative": "Resigned skepticism → the quiet surprise of genuine enjoyment",
          "art_direction": "The Honest Sip — private pleasure with ingredients as quiet evidence"
        }
      },
      "SecondaryCommunication": [
        { "statement": "It's made from natural, recognizable ingredients — what's beside her IS the ingredient list.", "supports": "PrimaryCommunication", "priority": "High" },
        { "statement": "It belongs to ordinary daily life — a kitchen morning, not a training plan.", "supports": "PrimaryCommunication", "priority": "Medium" },
        { "statement": "The product (open pouch + scoop) is the source of the moment — present, not pushed.", "supports": "PrimaryCommunication", "priority": "High" }
      ],
      "SuppressedCommunication": [
        { "statement": "Athletic performance, muscle, training context", "reason": "Strategy forbidden_meaning AthleticPerformance; reintroduces the category framing the campaign exists to escape." },
        { "statement": "Clinical purity / quantified nutrition claims", "reason": "Strategy forbidden_meaning ClinicalEfficacy; naturalness is proven by visible food, not claimed." },
        { "statement": "Product-hero pack shot", "reason": "Strategy forbidden_positioning SupplementHero; the pack stays a kitchen object even with 'clear product focus' framing." },
        { "statement": "Posed, to-camera delight", "reason": "ArtDirection ToneGuard — the new frontal camera angle must not collapse the subject's gaze/attention into a performed-for-camera expression." }
      ],
      "MemoryAnchor": {
        "statement": "The unguarded 'oh, that's actually good' sip — with real food beside her as the receipt, shot like a campaign but felt like a real moment.",
        "justification": "One intimate, sensory beat that encodes both messages (pleasure + naturalness), now carried in a brighter, more polished frame without losing its private quality."
      }
    },

    "ObservableSignalMapping": [
      {
        "communication": "Genuine taste pleasure",
        "human_signal": "Unperformed savoring — eyes softened or closed, half-smile, gaze on the glass at her lips, not on the camera",
        "observable_requirements": ["expression caught mid-moment, not posed to camera", "gaze directed at the glass/moment despite frontal camera position"],
        "Visual Evidence Examples": ["a just-after-the-sip half-smile with eyes lowered toward the glass", "fingers loose around the glass"],
        "allocation_priority": "MustSurvive"
      },
      {
        "communication": "Natural / real ingredients",
        "human_signal": "Recognizable whole foods within reach beside the open pack",
        "observable_requirements": ["banana, oats, berries, vanilla pod individually identifiable", "scoop with powder beside the open kraft pouch", "casual, not over-styled placement"],
        "Visual Evidence Examples": ["a peeled banana and scattered oats beside the pack", "scoop dusted with powder"],
        "allocation_priority": "MustSurvive"
      },
      {
        "communication": "Tastes good (the drink itself)",
        "human_signal": "Appetite-credible drink",
        "observable_requirements": ["visibly thick, creamy blended texture", "natural pale oat-vanilla tone, no artificial color"],
        "Visual Evidence Examples": ["texture clinging to the glass wall", "a faint berry swirl"],
        "allocation_priority": "PreserveWhenPossible"
      },
      {
        "communication": "Ordinary daily life, elevated",
        "human_signal": "Bright, clean home kitchen, casual clothes",
        "observable_requirements": ["home kitchen reads clearly even when polished/bright", "no athletic wear or gym objects"],
        "Visual Evidence Examples": ["soft knit top", "tidy counter and cabinetry in soft daylight"],
        "allocation_priority": "SimplifyWhenConstrained"
      }
    ],

    "CommunicationAllocation": [
      { "component": "Unperformed savoring moment, gaze on the glass not the camera", "supports": ["PrimaryCommunication"], "priority": "Critical", "survival_policy": "MustSurvive", "derived_from": ["Narrative", "ArtDirection"], "justification": "The emotional proof of taste; without it this is a posed campaign portrait, not an honest sip." },
      { "component": "Recognizable ingredients + open pack as evidence, within reach beside her", "supports": ["PrimaryCommunication", "SecondaryCommunication"], "priority": "Critical", "survival_policy": "MustSurvive", "derived_from": ["Campaign MandatoryRequirements", "Scene"], "justification": "Carries 'natural' without copy; also the product's required presence and the 'clear product focus' of the new brief." },
      { "component": "Appetite-credible creamy drink", "supports": ["PrimaryCommunication"], "priority": "High", "survival_policy": "PreserveWhenPossible", "derived_from": ["Scene"], "justification": "The object of the pleasure; links face to ingredients." },
      { "component": "Bright, clean home-kitchen setting", "supports": ["SecondaryCommunication"], "priority": "Medium", "survival_policy": "SimplifyWhenConstrained", "derived_from": ["Strategy EverydayBelonging", "Scene"], "justification": "Context may simplify under DOF softening but must never become a gym, studio void, or generic backdrop." },
      { "component": "Crisp, polished, high-end lifestyle-campaign register", "supports": ["PrimaryCommunication"], "priority": "Low", "survival_policy": "RemoveWhenConstrained", "derived_from": ["New Creative Direction", "Composition"], "justification": "Aesthetic register from the user's Style brief; reducible under pressure, must never override the Critical savoring/ingredient facts." }
    ],

    "ExecutionResolution": {
      "PrimaryExecutionMode": "Bright, crisp lifestyle-campaign portrait of an intimate candid food moment — frontal/eye-level/waist-up, but captured mid-savor, not staged delight",
      "SupportingExecutionModes": ["Ingredient evidence within reach beside the subject", "Product pack present as a kitchen object, clearly visible but not hero-lit"],
      "ExecutionRequirements": ["Single subject genuinely savoring, gaze on the glass", "Ingredients individually recognizable", "Open pack + scoop visible", "Bright, clean home kitchen in even daylight", "Eye-level, frontal, waist-up framing per the new brief"],
      "ExcludedExecutionModes": ["Gym or athletic context", "Clinical/studio product shot", "Posed to-camera delight or smile-at-lens expression", "Styled commercial flat-lay of ingredients", "Before/after framing"]
    },

    "HierarchyResolution": {
      "PrimaryFocus": ["entity_01 (the savoring moment)"],
      "SecondaryFocus": ["entity_02 (the drink)", "entity_03 (pack + scoop)", "entity_04 (ingredients)"],
      "SupportingFocus": ["entity_05 (kitchen)"],
      "AttentionSequence": ["entity_01", "entity_02", "entity_03", "entity_04", "entity_05"]
    },

    "RenderingResolution": {

      "PerceptualRendering": {
        "EmotionalTone": "Quiet, intimate pleasure — a private 'oh, that's actually good', savoring not celebration — now presented with the brightness and polish of an aspirational lifestyle campaign",
        "Atmosphere": "Bright, clean, crisp home-kitchen morning; airy and high-clarity, unhurried"
      },

      "PhysicalRendering": {
        "RealityModel": "Realistic",
        "CameraIntent": "Eye-level, straight-on, waist-up medium shot at a balanced mid distance — the camera sits frontally in front of the subject, undistorted natural proportions, while her gaze stays on the glass rather than the lens",
        "CameraSpecs": {
          "focal_length_mm": "85mm",
          "aperture_f_stop": "f/4"
        },
        "LightingIntent": "Bright, soft, broadly even key light with gentle fill — minimal harsh shadow, crisp and polished, consistent with high-end lifestyle-campaign photography, while still keeping the subject as the brightest point in the frame",
        "LuminanceHierarchy": [
          { "element": "entity_01", "luminance_priority": "Brightest" },
          { "element": "entity_02", "luminance_priority": "Mid" },
          { "element": "entity_03", "luminance_priority": "Mid" },
          { "element": "entity_04", "luminance_priority": "Mid" },
          { "element": "entity_05", "luminance_priority": "Dimmest" }
        ],
        "MaterialBehavior": "Thick smoothie texture clinging to the glass; matte kraft pouch; dusty scoop; real oat/berry/banana surfaces — all rendered with crisp, high-clarity (8k photorealistic) surface definition; nothing glossy or plastic",
        "OpticalIntent": "Atmospheric/Soft Focus falloff consistent with CameraSpecs (85mm, f/4) — face, glass, pack, and ingredients all sharp and crisp within or near the focal plane; the kitchen behind softens progressively into recognizable but gentle bright shapes (cabinetry, window), never collapsing into hard cutout bokeh"
      },

      "RenderingQuality": {
        "DetailRendering": "Expression, drink texture, pack, and ingredients all rendered crisp and sharp; kitchen softened by depth but recognizable as a bright, clean space",
        "TextureRendering": "Visible skin pores, knit fabric, oat grain, berry skin, kraft paper tooth — all high-clarity per the '8k photorealistic' style",
        "LightingRendering": "Bright, even, soft key light with gentle fill; face reads brightest, counter items close behind, kitchen/window held visibly dimmer despite the overall bright exposure",
        "DepthRendering": "Subject and counter items (within/near the waist-up frame) sharp; kitchen backdrop separated by Atmospheric falloff, recognizable but secondary",
        "CommercialRendering": "Crisp, polished, high-end lifestyle-campaign realism — appetizing and aspirational, but never laboratory-clean or staged-flat-lay"
      },

      "AuthenticityBehavior": {
        "HumanAuthenticityRendering": "Natural skin texture — pores, tone variation; relaxed asymmetric mid-savor expression, gaze on the glass; nothing beauty-filtered or posed-to-camera, regardless of the polished overall style",
        "EnvironmentalAuthenticityRendering": "Bright, clean home kitchen — tidy but lived-in, real morning light behavior",
        "MaterialAuthenticityRendering": "Just-used but tidy arrangement: scoop dusted with powder, banana freshly peeled, berries loose — matte natural materials kept crisp, not over-styled into a flat-lay",
        "ImperfectionRendering": "Credibility over staging — keep casual placement and small imperfections on skin/ingredients even as surfaces and lighting read as polished/high-end"
      }
    },

    "PreservationResolution": {
      "PreservedEntities": [
        "Single woman, early thirties, casual home clothes, genuinely savoring mid-moment, gaze on the glass (NOT posed to camera, NOT a group)",
        "Thick creamy smoothie with natural pale oat-vanilla tone",
        "Matte kraft protein pouch, open, with scoop — clean minimal label with NO legible text or invented logo",
        "Recognizable real ingredients: banana, rolled oats, berries, vanilla pod"
      ],
      "PreservedContext": [
        "Bright, clean home kitchen in even daylight",
        "Eye-level, frontal, waist-up framing per the new Style/Angle/Distance brief",
        "Instagram feed placement — safe zones clear of the face, the pack, and the glass"
      ],
      "PreservedBrandRequirements": [
        "Food-brand behavior throughout — pack as kitchen object, never a clinical hero shot, even with 'clear product focus'",
        "No legible fabricated brand text anywhere in frame"
      ],
      "PreservedNarrativeRequirements": [
        "Emotional read is quiet genuine enjoyment — never performed delight, never effortful health virtue, even in a frontal campaign-style frame"
      ],
      "PreservedConstraints": [
        "No competitor brands or look-alike packaging",
        "No gym equipment or athletic context",
        "Vertical 4:5 (or square 1:1) for Instagram feed",
        "Natural, non-airbrushed skin texture — mandatory regardless of 'crisp and polished' style language"
      ]
    }
  }
}
```

---

## Resolution Notes

- **CameraSpecs** (85mm, f/4) carried verbatim from the Trial_03 `CameraPlan` per the 6.1 → 7.1 pass-through rule; `CameraIntent` and `OpticalIntent` reference but do not restate the numbers.
- **LuminanceHierarchy** carried verbatim per-entity from `HierarchyPlan.luminance_priority`; `LightingIntent` and `RenderingQuality.LightingRendering` remain consistent with these rankings without restating them as a list.
- **New Creative Direction (Style/Angle/Distance brief)** is consolidated, not introduced fresh — every phrase in the brief is traced to a CameraSpecs value, a LightingIntent/MaterialBehavior clause, or an AttentionSequence/HierarchyResolution entry already present in Stage 5/6.
- **ArtDirection's "not performed to camera" ToneGuard** is explicitly preserved as a SuppressedCommunication entry and an immutable attribute on entity_01 — the frontal camera angle and the subject's private gaze are kept as independent variables throughout.
- **Human Subject Rendering Requirement** is restated in `PreservedConstraints` to make explicit that "crisp and polished, 8k photorealistic" governs surfaces/materials/lighting, not skin.
- **No reference-asset obligation** — generic pack carried textually; when real packaging exists, rerun 5.2.5 with the file so a `ReferenceAssetManifest` → `BRAND_ASSETS` path activates.
- **Single subject** → `pose_variation_required: false` upstream.
- Prompt Compiler can execute from this contract alone.

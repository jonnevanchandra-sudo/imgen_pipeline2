# Synthesis Contract
**Brand:** CLEVER Protein
**Campaign:** The 3 PM Office Rescue (3點鐘辦公室救星)
**Framework:** Synthesis Framework v8.1
**Stage:** 7 — Communication Resolution

---

```json
{
  "SynthesisContract": {

    "ExecutiveSummary": "A close, high-angle view over an ordinary HK office desk at mid-afternoon. In the foreground, a CLEVER Weight Down pouch (soft pink/rose-and-white packaging, CLEVER wordmark, '減重蛋白' label) sits alongside a prepared shake — bright, sharp, and composed, the clear focal point. A single hand with natural skin texture reaches toward it in a calm, unremarkable gesture. Further back on the desk, softly recessed, sits a typical 3pm office snack-run order — siu mai in a takeaway container and an iced lemon tea — recognizable but visually settled into the background. The mood is calm and unhurried: an ordinary afternoon in which a small, smart choice has simply, quietly, already happened.",

    "CommunicationResolution": {
      "PrimaryCommunication": {
        "statement": "At 3pm, reaching for CLEVER Weight Down is the obvious, already-made choice — calm, not a contest.",
        "derived_from": {
          "campaign": "The 3 PM Office Rescue — reframes the daily snack-run moment around a smarter substitute, without medical/extreme-dieting framing",
          "brand": "Composed, precise, quietly confident — 'Clever choice' as the brand's central decision narrative; purity/clarity visual signature (pink/white, translucency)",
          "strategy": "The Smart 3pm Swap — Confidence (Critical) and Accessibility (Critical) activated; willpower-battle reframed as a solved habit",
          "narrative": "Calm Mastery / Quiet Confidence — restless/tempted → settled/decided; 'I have to resist' → 'I already chose'",
          "art_direction": "The Quiet Swap — a single mid-afternoon moment where the CLEVER product is already part of the scene as the resolved choice, while the familiar snack-run option has receded"
        }
      },
      "SecondaryCommunication": [
        {
          "statement": "The familiar 3pm snack run (siu mai + iced lemon tea) is the 'hidden calorie' option that's been quietly passed over.",
          "supports": "PrimaryCommunication",
          "priority": "High"
        },
        {
          "statement": "This is satiety without sacrifice — CLEVER Weight Down looks like a real, satisfying part of the moment, not a deprivation substitute.",
          "supports": "PrimaryCommunication",
          "priority": "High"
        },
        {
          "statement": "This is my desk, my 3pm — an ordinary, recognizable HK office moment.",
          "supports": "PrimaryCommunication",
          "priority": "Medium"
        }
      ],
      "SuppressedCommunication": [
        {
          "statement": "Weight-loss transformation / before-after framing",
          "reason": "Forbidden by StrategyContract.MeaningConstraints — contradicts the 'smart everyday choice' framing and would invoke clinical/medical weight-loss meaning"
        },
        {
          "statement": "Guilt or shame directed at the comparison snack or the people who eat it",
          "reason": "Explicitly forbidden by StrategyContract.MeaningConstraints and ArtDirectionContract.DistinctivenessValidation — the resolution must come from substitution, not shame"
        },
        {
          "statement": "Clinical / lab supplement aesthetic",
          "reason": "Forbidden by StrategyContract.StrategicConstraints.forbidden_positioning and BrandContract.CoreTensions — contradicts the soft pink/white, café-adjacent visual identity"
        },
        {
          "statement": "Hardcore athletic-performance framing",
          "reason": "Forbidden by StrategyContract.MeaningConstraints — this campaign is an audience-extension into everyday office life, not an athletic context"
        },
        {
          "statement": "Loud graphic 'VS' / split-screen scoreboard treatment",
          "reason": "ArtDirectionContract.DistinctivenessValidation explicitly avoids a dramatized comparison-graphic; the contrast must read through scene composition (foreground/resolved vs. background/receded), not graphic overlay"
        }
      ],
      "MemoryAnchor": {
        "statement": "That quiet desk shot where the smart 3pm pick was just... already sitting there, already chosen.",
        "justification": "The image must be remembered as a calm, ordinary moment that happens to contain a resolved decision — not as a comparison graphic or a willpower story. The MemoryAnchor is the quiet resolution itself, anchored by the CLEVER product's foreground presence."
      }
    },

    "ObservableSignalMapping": [
      {
        "communication": "Already decided",
        "human_signal": "A hand reaching toward the CLEVER product in a calm, unremarkable gesture — no hesitation, no comparison, no deliberation visible",
        "observable_requirements": [
          "Hand (entity_03) is mid-reach toward or resting near the CLEVER product (entity_01), not toward the comparison snack",
          "Gesture reads as natural and habitual, not posed or emphatic",
          "No visible tension, gripping, or 'choosing between two things' body language"
        ],
        "Visual Evidence Examples": [
          "A relaxed hand resting on or reaching toward the pouch/shake as if about to pick it up mid-afternoon",
          "Fingers naturally curved, wrist at a comfortable angle — the gesture of a routine action, not a decision moment"
        ],
        "allocation_priority": "MustSurvive"
      },
      {
        "communication": "CLEVER is the clean, composed, smart choice",
        "human_signal": "The CLEVER Weight Down product presents as visually composed, bright, and clear — distinct from the more casual comparison items",
        "observable_requirements": [
          "Pink/rose-and-white pouch with CLEVER wordmark and '減重蛋白' label clearly legible",
          "Prepared shake visible as a smooth, uniform beverage",
          "Product is the brightest and sharpest element in the frame"
        ],
        "Visual Evidence Examples": [
          "Pouch and shake in sharp focus, soft daylight catching the clean packaging surface",
          "CLEVER wordmark and '減重蛋白' text crisp and readable at small Instagram size"
        ],
        "allocation_priority": "MustSurvive"
      },
      {
        "communication": "Hidden-calorie snack run = passed-over option",
        "human_signal": "The siu mai + iced lemon tea order is recognizable but visually settled — present, not competing",
        "observable_requirements": [
          "Siu mai in a takeaway container and a cold tea drink in a disposable cup, recognizable as a typical HK office snack-run order",
          "Items presented in an ordinary, slightly worn takeaway manner — not styled",
          "Positioned further back / softer focus than the CLEVER product"
        ],
        "Visual Evidence Examples": [
          "Takeaway box and cup sitting toward the back of the desk, mildly softened but identifiable",
          "No special lighting or framing elevating these items beyond ordinary desk clutter"
        ],
        "allocation_priority": "PreserveWhenPossible"
      },
      {
        "communication": "This is my desk, my 3pm (recognition)",
        "human_signal": "An ordinary HK office desk environment with ambient daylight and incidental everyday objects",
        "observable_requirements": [
          "Desk surface visible with everyday work objects at frame edges (e.g. laptop edge, notebook, pen)",
          "Soft ambient mid-afternoon interior daylight",
          "No staged or studio-clean environment"
        ],
        "Visual Evidence Examples": [
          "A corner of a laptop or notebook visible at the edge of frame",
          "Natural window light falling softly across the desk surface"
        ],
        "allocation_priority": "PreserveWhenPossible"
      },
      {
        "communication": "Natural, unposed human presence",
        "human_signal": "A real hand with natural skin texture — not airbrushed or idealized",
        "observable_requirements": [
          "Visible natural skin texture on entity_03 — pores, subtle tone variation, natural knuckle/joint detail",
          "No face or other identity-bearing features visible"
        ],
        "Visual Evidence Examples": [
          "Hand skin showing natural micro-texture and slight tonal variation under soft daylight"
        ],
        "allocation_priority": "PreserveWhenPossible"
      }
    ],

    "CommunicationAllocation": [
      {
        "component": "CLEVER Weight Down product — clean, composed, foreground, brightest/sharpest",
        "supports": ["PrimaryCommunication"],
        "priority": "Critical",
        "survival_policy": "MustSurvive",
        "derived_from": ["SceneContract.PreservationContracts (entity_01, Critical/Near Exact)", "CompositionRenderingContract.HierarchyPlan (entity_01, Primary/Brightest)", "CampaignContract.MandatoryRequirements.ProductSpec"],
        "justification": "This is the single non-negotiable element — without the product clearly present, composed, and dominant, the entire 'already chosen' communication collapses."
      },
      {
        "component": "Calm hand reaching toward the CLEVER product",
        "supports": ["PrimaryCommunication"],
        "priority": "Critical",
        "survival_policy": "MustSurvive",
        "derived_from": ["SceneContract.Relationships (entity_03 reaching_toward entity_01)", "CompositionRenderingContract.AttentionPlan", "NarrativeContract.DesiredTransformation"],
        "justification": "The hand's calm gesture is the only human signal carrying 'already decided' — without it, the scene risks reading as a static product shot rather than a lived moment."
      },
      {
        "component": "Comparison snack/drink (siu mai + iced lemon tea) recognizable but receded",
        "supports": ["SecondaryCommunication — hidden-calorie passed-over option"],
        "priority": "High",
        "survival_policy": "PreserveWhenPossible",
        "derived_from": ["SceneContract.PreservationContracts (entity_02, Medium/Approximate)", "CompositionRenderingContract.OpticalPlan (bokeh_behavior)", "StrategyContract.ContextualTensions"],
        "justification": "The contrast is essential to the campaign's comparison logic, but must remain secondary — if token pressure forces simplification, this may be reduced to a single recognizable item rather than the full order, but cannot be removed entirely."
      },
      {
        "component": "Ordinary HK office desk environment",
        "supports": ["SecondaryCommunication — this is my desk, my 3pm"],
        "priority": "Medium",
        "survival_policy": "PreserveWhenPossible",
        "derived_from": ["SceneContract.Entities (entity_04)", "ArtDirectionContract.SubjectRelationshipLogic (Recognition)"],
        "justification": "Grounds the scene as real and relatable; may be simplified to minimal incidental cues under constraint without losing the core communication."
      },
      {
        "component": "Natural skin texture on the hand",
        "supports": ["PrimaryCommunication — authenticity of the moment"],
        "priority": "Medium",
        "survival_policy": "PreserveWhenPossible",
        "derived_from": ["CompositionRenderingContract.RenderingConstraints.natural_skin_rendering_required", "CompositionRenderingContract.MaterialPlan"],
        "justification": "Reinforces credibility of the moment; a hard constraint on rendering quality but does not independently carry a unique communication if simplified."
      },
      {
        "component": "Soft daylight / calm atmospheric tone",
        "supports": ["PrimaryCommunication — emotional register of calm resolution"],
        "priority": "Low",
        "survival_policy": "RemoveWhenConstrained",
        "derived_from": ["CompositionRenderingContract.LightingPlan", "CompositionRenderingContract.AtmosphericPlan", "NarrativeContract.NarrativeLensSelection"],
        "justification": "Important for tone but the last element to compress — the core communication survives even with simplified lighting description."
      }
    ],

    "ExecutionResolution": {
      "PrimaryExecutionMode": "Close, high-angle desk shot — CLEVER Weight Down product in sharp foreground as the resolved choice, with a hand calmly reaching toward it; the comparison snack/drink visible but softly receded in the background of the same desk.",
      "SupportingExecutionModes": [
        "Natural human-hand interaction as the sole human presence, grounding the moment without introducing a posed figure",
        "Ordinary office desk environment establishing 'my desk, my 3pm' recognition"
      ],
      "ExecutionRequirements": [
        "CLEVER Weight Down must be rendered per its PreservationContract (wordmark, '減重蛋白' label, pink/white pouch, prepared shake) and must occupy the foreground/brightest position",
        "The comparison snack/drink must remain identifiable as a typical HK 3pm snack-run order, even while softened",
        "Only one human element (a single hand) is present — no additional figures or faces",
        "Environment must read as an ordinary office desk with ambient daylight, not a styled or studio setting"
      ],
      "ExcludedExecutionModes": [
        "Split-screen or graphic 'VS' comparison layout",
        "Before/after weight-loss or body-transformation imagery",
        "Clinical/lab supplement product photography",
        "Guilt-framed close-up of the comparison snack",
        "Full human figure or visible face",
        "Dramatic, moody, or high-contrast cinematic lighting"
      ]
    },

    "HierarchyResolution": {
      "PrimaryFocus": [
        "entity_01 — CLEVER Weight Down product (pouch + prepared shake): the resolved, already-chosen object; brightest and sharpest element, first point of attention"
      ],
      "SecondaryFocus": [
        "entity_03 — hand reaching toward entity_01: reinforces the 'quiet swap' relationship without competing with the product",
        "entity_02 — siu mai + iced lemon tea: the passed-over option, recognizable but softened and receded"
      ],
      "SupportingFocus": [
        "entity_04 — ordinary HK office desk environment: grounds the scene without drawing attention"
      ],
      "AttentionSequence": [
        "1. CLEVER Weight Down product (entry point — brightest, sharpest)",
        "2. Hand reaching toward the product — reinforces the relationship",
        "3. Comparison snack/drink — softened, completes the contrast",
        "4. Desk environment — ambient context"
      ]
    },

    "RenderingResolution": {

      "PerceptualRendering": {
        "EmotionalTone": "Calm, settled, quietly confident — the feeling of a small decision that has already been made without effort or announcement. Not triumphant, not instructional, not dramatized.",
        "Atmosphere": "An ordinary mid-afternoon HK office interior — soft ambient daylight, unhurried, uncluttered. Nothing about the scene signals 'staged moment'; it reads as a candid slice of a real workday."
      },

      "PhysicalRendering": {
        "RealityModel": "Realistic — clean commercial-lifestyle photography register, consistent with CLEVER's premium-but-approachable e-commerce visual identity.",
        "CameraIntent": "High-angle, close-up view looking down over the desk at near distance — the perspective of someone looking at their own workspace. The CLEVER product and hand sit in the sharp near-field; the comparison snack/drink and desk surroundings recede behind them.",
        "CameraSpecs": {
          "focal_length_mm": "50mm",
          "aperture_f_stop": "f/4"
        },
        "LightingIntent": "Soft, even ambient daylight consistent with an office interior, keying onto the product and hand as the brightest area of the frame, with a gentle natural falloff toward the desk background. No dramatic, moody, or directional studio lighting.",
        "LuminanceHierarchy": [
          { "element": "entity_01", "luminance_priority": "Brightest" },
          { "element": "entity_03", "luminance_priority": "Mid" },
          { "element": "entity_02", "luminance_priority": "Dimmest" },
          { "element": "entity_04", "luminance_priority": "Dimmest" }
        ],
        "MaterialBehavior": "CLEVER pouch and shake render with a clean matte/soft-sheen finish consistent with minimalist packaging; the takeaway container and cup for the comparison snack/drink show ordinary, slightly worn disposable materials — the material contrast itself reinforces 'considered choice' vs. 'grab-and-go'.",
        "OpticalIntent": "At 50mm/f/4, the product and hand remain fully sharp in the near field. The comparison snack/drink shows mild progressive softening — edges and label details lose crispness but overall shapes remain identifiable. The desk surroundings show the most softening, reduced to soft recognizable forms rather than hard bokeh discs."
      },

      "RenderingQuality": {
        "DetailRendering": "CLEVER wordmark and '減重蛋白' label text must be sharp and legible at Instagram viewing size. Hand skin texture must show fine detail.",
        "TextureRendering": "Clean matte packaging texture on the CLEVER product; ordinary worn disposable textures on the comparison items; natural skin texture on the hand; everyday desk surface texture.",
        "LightingRendering": "Soft, neutral-to-warm daylight color temperature throughout — no cold clinical cast, no dramatic warm/cool color grading.",
        "DepthRendering": "Clear near-to-far depth progression: product and hand sharp in the foreground, comparison snack/drink mildly softened in the midground/background, desk surroundings most softened — depth must reinforce the Brightest/Mid/Dimmest luminance ranking.",
        "CommercialRendering": "Clean commercial-lifestyle quality consistent with CLEVER's e-commerce visual identity, but candid rather than studio-staged — must read as a real desk moment, not a product-shot composition."
      },

      "AuthenticityBehavior": {
        "HumanAuthenticityRendering": "The hand (entity_03) must show visible natural skin texture — pores, subtle tone variation, natural knuckle/joint detail — with no airbrushing or AI-perfect smoothing. Gesture must read as natural and habitual, not posed.",
        "EnvironmentalAuthenticityRendering": "The desk and office environment must read as ordinary and lived-in — incidental everyday objects at frame edges, natural ambient daylight, no styled or studio-clean staging.",
        "MaterialAuthenticityRendering": "CLEVER packaging renders clean and considered; comparison takeaway items render as ordinary, slightly worn disposable materials — the contrast in material care is itself part of the communication.",
        "ImperfectionRendering": "Minor real-world imperfections (slightly uneven desk clutter, natural skin variation, ordinary takeaway packaging wear) are correct and reinforce that this is a candid moment, not a constructed product shot."
      }
    },

    "PreservationResolution": {
      "PreservedEntities": [
        "entity_01: CLEVER Weight Down — stand-up pouch in soft pink/rose-and-white packaging with the 'CLEVER' wordmark and '減重蛋白'/'Weight Down' label text, shown alongside or as a prepared shake. These attributes are immutable per SceneContract.PreservationContracts and must reach the Prompt Compiler's `brand` key in HIGH, product name first, visual descriptors following.",
        "entity_03: A single human hand reaching toward or resting near entity_01, with natural skin texture and no face or identity-bearing features visible. Cannot be expanded into a full figure or additional subjects."
      ],
      "PreservedContext": [
        "Instagram 4:5 vertical format (1080 x 1350px)",
        "Bottom 15-20% of frame reserved for caption/CTA overlay — must remain clear of critical visual information",
        "No on-image legible text is expected from the generator other than the CLEVER wordmark and '減重蛋白' label on entity_01 — all other captioning is added separately as Instagram post copy"
      ],
      "PreservedBrandRequirements": [
        "Soft pink/rose-and-white palette anchors entity_01 — the CLEVER side of the scene must carry the brand's signature clean visual language",
        "'CLEVER' wordmark and '減重蛋白' label text are the only legible-text elements permitted in the image",
        "CLEVER product must occupy the foreground/brightest/sharpest position relative to the comparison snack/drink"
      ],
      "PreservedNarrativeRequirements": [
        "The comparison snack/drink (entity_02) must remain recognizable as siu mai + iced lemon tea/bubble tea — required to carry the 'hidden calorie passed-over option' communication — while staying visually secondary/receded",
        "The overall emotional register must remain calm and settled — no dramatized contrast, no guilt-framing of entity_02, no willpower-struggle imagery",
        "Only one human element (a hand) is present — no additional figures, faces, or shared multi-subject actions"
      ],
      "PreservedConstraints": [
        "natural_skin_rendering_required: true — entity_03 must show natural, unretouched skin texture",
        "pose_variation_required: false — single hand only, no multi-subject pose constraint applies",
        "CameraSpecs (50mm, f/4) and the Atmospheric depth-of-field category must be carried through verbatim — full background isolation (Commercial Isolation) would remove entity_02's required legibility"
      ]
    }

  }
}
```

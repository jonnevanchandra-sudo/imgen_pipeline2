# Synthesis Contract — Natural Protein Powder (Stage 7.1)

Framework: `7.1 Synthesis.md`
Inputs: Brand (0, assumed mode), Campaign (1), Strategy (2), Narrative (3), Art Direction (4), Scene (5.2.5), Composition & Rendering (6.1)
Decision Type: Communication Resolution — consolidates, resolves, prioritizes; introduces no new creative decisions.

```json
{
  "SynthesisContract": {

    "ExecutiveSummary": "A woman in her own morning kitchen is caught in the private moment of genuinely enjoying a creamy smoothie, while the real ingredients it came from — banana, oats, berries, vanilla, the open kraft pouch and scoop — sit in just-used disarray on the counter. The image communicates 'healthy that genuinely tastes good, made from food you recognize' as a food moment, never a supplement ad.",

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
        { "statement": "It's made from natural, recognizable ingredients — the counter IS the ingredient list.", "supports": "PrimaryCommunication", "priority": "High" },
        { "statement": "It belongs to ordinary daily life — a kitchen morning, not a training plan.", "supports": "PrimaryCommunication", "priority": "Medium" },
        { "statement": "The product (open pouch + scoop) is the source of the moment — present, not pushed.", "supports": "PrimaryCommunication", "priority": "High" }
      ],
      "SuppressedCommunication": [
        { "statement": "Athletic performance, muscle, training context", "reason": "Strategy forbidden_meaning AthleticPerformance; reintroduces the category framing the campaign exists to escape." },
        { "statement": "Clinical purity / quantified nutrition claims", "reason": "Strategy forbidden_meaning ClinicalEfficacy; naturalness is proven by visible food, not claimed." },
        { "statement": "Product-hero pack shot", "reason": "Strategy forbidden_positioning SupplementHero; the pack stays a kitchen object." }
      ],
      "MemoryAnchor": {
        "statement": "The unguarded 'oh, that's actually good' sip — with real food on the counter as the receipt.",
        "justification": "One intimate, sensory beat that encodes both messages: pleasure (the face) and naturalness (the counter)."
      }
    },

    "ObservableSignalMapping": [
      {
        "communication": "Genuine taste pleasure",
        "human_signal": "Unperformed savoring — eyes softened or closed, half-smile, glass still at the lips",
        "observable_requirements": ["expression caught mid-moment, not posed to camera", "body relaxed, at home"],
        "Visual Evidence Examples": ["a just-after-the-sip half-smile", "fingers loose around the glass"],
        "allocation_priority": "MustSurvive"
      },
      {
        "communication": "Natural / real ingredients",
        "human_signal": "Recognizable whole foods in just-used disarray beside the open pack",
        "observable_requirements": ["banana, oats, berries, vanilla pod individually identifiable", "scoop with powder beside the open kraft pouch", "casual placement, not a styled flat-lay"],
        "Visual Evidence Examples": ["oats scattered where the scoop was used", "a peeled banana next to the blender glass"],
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
        "communication": "Ordinary daily life",
        "human_signal": "Lived-in home kitchen, morning light, casual clothes",
        "observable_requirements": ["home kitchen reads clearly", "no athletic wear or gym objects"],
        "Visual Evidence Examples": ["soft knit top", "everyday kitchen clutter at the frame edges"],
        "allocation_priority": "SimplifyWhenConstrained"
      }
    ],

    "CommunicationAllocation": [
      { "component": "Unperformed savoring moment", "supports": ["PrimaryCommunication"], "priority": "Critical", "survival_policy": "MustSurvive", "derived_from": ["Narrative", "ArtDirection"], "justification": "The emotional proof of taste; without it this is a stock food photo." },
      { "component": "Recognizable ingredients + open pack as evidence", "supports": ["PrimaryCommunication", "SecondaryCommunication"], "priority": "Critical", "survival_policy": "MustSurvive", "derived_from": ["Campaign MandatoryRequirements", "Scene"], "justification": "Carries 'natural' without copy; also the product's required presence." },
      { "component": "Appetite-credible creamy drink", "supports": ["PrimaryCommunication"], "priority": "High", "survival_policy": "PreserveWhenPossible", "derived_from": ["Scene"], "justification": "The object of the pleasure; links face to ingredients." },
      { "component": "Home kitchen / morning ordinariness", "supports": ["SecondaryCommunication"], "priority": "Medium", "survival_policy": "SimplifyWhenConstrained", "derived_from": ["Strategy EverydayBelonging", "Scene"], "justification": "Context may simplify but must never become a gym or studio." },
      { "component": "Warm editorial food-photography register", "supports": ["PrimaryCommunication"], "priority": "Low", "survival_policy": "RemoveWhenConstrained", "derived_from": ["Brand RenderingStyle", "Composition"], "justification": "Aesthetic register; reducible under pressure." }
    ],

    "ExecutionResolution": {
      "PrimaryExecutionMode": "Intimate candid food-moment realism — captured mid-savor, not staged",
      "SupportingExecutionModes": ["Ingredient evidence in just-used disarray", "Product pack present as a kitchen object"],
      "ExecutionRequirements": ["Single subject genuinely savoring", "Ingredients individually recognizable", "Open pack + scoop visible", "Home kitchen in morning daylight"],
      "ExcludedExecutionModes": ["Gym or athletic context", "Clinical/studio product shot", "Posed to-camera delight", "Styled commercial flat-lay", "Before/after framing"]
    },

    "HierarchyResolution": {
      "PrimaryFocus": ["entity_01 (the savoring moment)"],
      "SecondaryFocus": ["entity_02 (the drink)", "entity_04 (ingredients)", "entity_03 (pack + scoop)"],
      "SupportingFocus": ["entity_05 (kitchen)"],
      "AttentionSequence": ["entity_01", "entity_02", "entity_04", "entity_03", "entity_05"]
    },

    "RenderingResolution": {

      "PerceptualRendering": {
        "EmotionalTone": "Quiet, intimate pleasure — a private 'oh, that's actually good', savoring not celebration",
        "Atmosphere": "Fresh, airy home-kitchen morning; light and unhurried"
      },

      "PhysicalRendering": {
        "RealityModel": "Realistic",
        "CameraIntent": "Eye-level near medium shot from the waist up — the viewer stands at the counter inside the moment; face dominant, counter evidence in the lower frame",
        "CameraSpecs": {
          "focal_length_mm": "50mm",
          "aperture_f_stop": "f/2.2"
        },
        "LightingIntent": "Soft directional morning window light keying face and glass, natural bounce fill, gentle falloff into the kitchen — daylight credibility, no theatrical shaping",
        "MaterialBehavior": "Thick smoothie texture clinging to the glass; matte kraft pouch; dusty scoop; real oat/berry/banana surfaces; nothing glossy or plastic",
        "OpticalIntent": "Progressive falloff consistent with CameraSpecs — face and glass sharp, counter ingredients semi-legible and identifiable, window and kitchen dissolving soft and bright; no flat cutout blur"
      },

      "RenderingQuality": {
        "DetailRendering": "Expression and drink texture sharpest; ingredients identifiable; background softened by depth",
        "TextureRendering": "Visible skin pores, knit fabric, oat grain, berry skin, kraft paper tooth",
        "LightingRendering": "Soft warm daylight with natural falloff; bright, appetizing highlights on the drink",
        "DepthRendering": "Foreground counter evidence / midground face / background kitchen separated by focus",
        "CommercialRendering": "Editorial food-and-lifestyle realism — appetizing but never laboratory-clean"
      },

      "AuthenticityBehavior": {
        "HumanAuthenticityRendering": "Natural skin texture — pores, tone variation; relaxed asymmetric mid-savor expression; nothing beauty-filtered or posed",
        "EnvironmentalAuthenticityRendering": "Lived-in kitchen — everyday objects at frame edges, light wear on the counter, real morning light behavior",
        "MaterialAuthenticityRendering": "Just-used disarray: scattered oats, a drip or smudge near the blender glass, powder dust on the scoop; matte natural materials",
        "ImperfectionRendering": "Credibility over polish — keep casual placement and small imperfections; do not correct toward styled perfection"
      }
    },

    "PreservationResolution": {
      "PreservedEntities": [
        "Single woman, early thirties, casual home clothes, genuinely savoring mid-moment (NOT posed to camera, NOT a group)",
        "Thick creamy smoothie with natural pale oat-vanilla tone",
        "Matte kraft protein pouch, open, with scoop — clean minimal label with NO legible text or invented logo",
        "Recognizable real ingredients: banana, rolled oats, berries, vanilla pod"
      ],
      "PreservedContext": [
        "Lived-in home kitchen in morning daylight",
        "Instagram feed placement — safe zones clear of the face, the pack, and the glass"
      ],
      "PreservedBrandRequirements": [
        "Food-brand behavior throughout — pack as kitchen object, never a clinical hero shot",
        "No legible fabricated brand text anywhere in frame"
      ],
      "PreservedNarrativeRequirements": [
        "Emotional read is quiet genuine enjoyment — never performed delight, never effortful health virtue"
      ],
      "PreservedConstraints": [
        "No competitor brands or look-alike packaging",
        "No gym equipment or athletic context",
        "Vertical 4:5 (or square 1:1) for Instagram feed"
      ]
    }
  }
}
```

---

## Resolution Notes

- **CameraSpecs** (50mm, f/2.2) carried verbatim from `CameraPlan` per the 6.1 → 7.1 pass-through rule; `CameraIntent` and `OpticalIntent` reference but do not restate the numbers.
- **No reference-asset obligation** — generic pack carried textually; when real packaging exists, rerun 5.2.5 with the file so a `ReferenceAssetManifest` → `BRAND_ASSETS` path activates.
- **Single subject** → `pose_variation_required: false` upstream; AuthenticityBehavior covers skin/material/environment naturalism only.
- Prompt Compiler can execute from this contract alone.

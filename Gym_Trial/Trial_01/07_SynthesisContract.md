# Synthesis Contract — Anytime Fitness Sai Ying Pun (Stage 7.1)

Framework: `7.1 Synthesis.md`
Inputs: All upstream contracts (Stages 0–6.1)
Decision Type: Communication Resolution — consolidates, resolves, prioritizes, suppresses. Introduces no new creative decisions.

```json
{
  "SynthesisContract": {

    "CoreMessage": "A single HKU-aged student trains, focused and at ease, inside the real Anytime Fitness Sai Ying Pun — recognizable, close to campus, and open whenever they are.",

    "CommunicationPriorities": [
      { "rank": 1, "signal": "Genuine, candid effort — the student is mid-rep, focused inward, not performing for the camera (Open 24/7 / 'just go when you can' identity)" },
      { "rank": 2, "signal": "Recognizable Anytime Fitness Sai Ying Pun environment — AF wall/rig and the specific Torque rack with colorful plates, both clearly this gym" },
      { "rank": 3, "signal": "Approachable, modern, welcoming space — broader gym floor reads as clean, spacious, not intimidating" }
    ],

    "SuppressedSignals": [
      "Any signal of elite athleticism, competitive intensity, or 'maximum effort' grimacing — explicitly forbidden by StrategyContract.MeaningConstraints",
      "Any signal of group/community activity — single-subject only, per CampaignContract.MandatoryRequirements",
      "Pricing, offer terms, or promotional copy rendered in-image — handled as post-production overlay per CampaignContract.OfferDefinition"
    ],

    "ConflictResolutions": [
      {
        "conflict": "AttentionPlan softens entity_03 (AF wall) via depth-of-field, but PreservationContract for entity_03 requires Critical/Close-Match recognizability of the 'AF' monogram",
        "resolution": "Resolved at Stage 6 via 'mild softening, monogram remains legible' — carried forward verbatim; no further resolution needed at Synthesis"
      }
    ],

    "EntitySummary": [
      {
        "entity_id": "entity_01",
        "role": "Primary subject",
        "description": "HKU-aged East Asian student, casual athletic wear (no third-party logos), mid-rep on the rack, focused downward/inward, not looking at camera. Natural skin texture, visible effort (slight sweat), no airbrushing.",
        "luminance_tier": "Brightest",
        "focus_tier": "Critical focus"
      },
      {
        "entity_id": "entity_02",
        "role": "Secondary — equipment in use",
        "description": "Silver Torque USA rack/bench loaded with green/grey/yellow/blue bumper plates, reproduced from reference_asset_02. Student actively using it.",
        "luminance_tier": "Mid",
        "focus_tier": "Critical focus",
        "reference": "reference_asset_02"
      },
      {
        "entity_id": "entity_03",
        "role": "Secondary — brand recognition anchor",
        "description": "Wood-paneled wall with white 'AF' monogram, black functional rig with 'ANYTIME FITNESS'-branded punching bag, purple rubber flooring, reproduced from reference_asset_03. Positioned midground, behind/beside the subject.",
        "luminance_tier": "Mid",
        "focus_tier": "Mild softening — monogram/wordmark must remain legible",
        "reference": "reference_asset_03"
      },
      {
        "entity_id": "entity_04",
        "role": "Supporting — environmental atmosphere",
        "description": "Industrial-chic gym floor: dark ceiling with exposed ductwork and recessed LED grid, black rubber tile flooring with hazard-stripe accents, treadmill row and Precor equipment receding into background. Style/atmosphere reference from reference_asset_01.",
        "luminance_tier": "Dimmest",
        "focus_tier": "Most softened — shapes recognizable, fine detail not legible",
        "reference": "reference_asset_01"
      }
    ],

    "LuminanceHierarchy": [
      "entity_01 — Brightest",
      "entity_02 — Mid",
      "entity_03 — Mid",
      "entity_04 — Dimmest"
    ],

    "PhysicalRendering": {
      "RealityModel": "Photographic, single continuous real-world gym space",
      "CameraSpecs": {
        "shot_type": "Medium shot, eye-level/slightly low, observational framing",
        "framing": "Vertical 4:5, subject off-center (rule of thirds)",
        "focal_length_mm": 35,
        "aperture_f_stop": "f/8",
        "depth_of_field_category": "Environmental Context"
      },
      "LightingPlan": {
        "key": "Overhead LED panel light, falling naturally across the subject",
        "fill": "Soft ambient bounce off rubber flooring/mirrors, low contrast",
        "accent": "Subtle warm (purple zone) vs cool (white LED main floor) separation between midground and background",
        "mood": "Even, slightly cool commercial-gym lighting — bright, safe, welcoming"
      },
      "MaterialPlan": {
        "human_skin_rendering": "Natural texture, visible pores, minor asymmetry, realistic sweat sheen — no airbrushing or beauty-filter smoothing",
        "metal": "Brushed/painted-steel reflectivity matching Torque USA rack finish",
        "rubber_flooring": "Matte, lightly textured, both black and purple zones",
        "fabric": "Natural wrinkling and slight sweat-darkening on athletic wear"
      },
      "OpticalPlan": {
        "bokeh_behavior": "Progressive depth-dependent falloff (35mm/f8): entity_01 + entity_02 critical focus, entity_03 mildly softened but legible, entity_04 most softened"
      },
      "AtmosphericPlan": {
        "air_quality": "Clean, no haze/fog/dust effects"
      }
    },

    "VisualFlow": {
      "entry_point": "Student's face/upper body",
      "path": "Face/torso -> hands/rack -> AF wall and rig (midground) -> gym floor (background)",
      "exit_point": "Soft background depth, no distracting bright edges"
    },

    "RenderingConstraints": {
      "single_subject_only": true,
      "no_invented_text": true,
      "no_competitor_branding": true,
      "natural_skin_rendering_required": true,
      "pose_variation_required": false
    },

    "PerceptualValidationAssertions": [
      "Skin Naturalism Assertion — natural texture/pores/asymmetry, no airbrushing",
      "Depth of Field Realism Assertion — progressive falloff per 35mm/f8, entity_03 remains legible",
      "Recognizability Assertion — entity_02 and entity_03 match reference_asset_02/03"
    ],

    "ReferenceAssetManifest": [
      {
        "prompt_reference_id": "reference_asset_01",
        "source_filename": "gym_photo_01.jpg",
        "entity_id": "entity_04",
        "preservation_priority": "Medium",
        "recognizability_requirement": "Approximate Match"
      },
      {
        "prompt_reference_id": "reference_asset_02",
        "source_filename": "gym_photo_02.jpg",
        "entity_id": "entity_02",
        "preservation_priority": "High",
        "recognizability_requirement": "Close Match"
      },
      {
        "prompt_reference_id": "reference_asset_03",
        "source_filename": "gym_photo_03.jpg",
        "entity_id": "entity_03",
        "preservation_priority": "Critical",
        "recognizability_requirement": "Close Match (Exact Match for 'AF' wordmark)"
      }
    ]
  }
}
```

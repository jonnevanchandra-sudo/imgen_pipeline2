# Synthesis Contract — FIT24 (Stage 7.1)

Framework: `7.1 Synthesis.md`
Inputs: All upstream contracts (Stages 0–6.1)
Decision Type: Communication Resolution — consolidates, resolves, prioritizes, suppresses. Introduces no new creative decisions.

```json
{
  "SynthesisContract": {

    "CoreMessage": "A single person runs steadily on a treadmill at FIT24, facing a floor-to-ceiling window wall with a green outdoor view — recognizable as this specific bright, open space, framed as a calm, energizing way to start the day.",

    "CommunicationPriorities": [
      { "rank": 1, "signal": "Genuine, calm, steady effort — the runner is present and at ease, mid-stride, not performing for the camera (a good start to the day, not a grind)" },
      { "rank": 2, "signal": "The bright, open window-wall space with a green outdoor view — FIT24's distinctive environment, clearly recognizable" },
      { "rank": 3, "signal": "FIT24 logo and treadmill row visible — modern, well-equipped, branded space" }
    ],

    "SuppressedSignals": [
      "Any signal of elite athleticism, sprinting-at-max, or competitive intensity — explicitly forbidden by StrategyContract.MeaningConstraints",
      "Any signal of group/community activity — single-subject only, per CampaignContract.MandatoryRequirements",
      "Empty real-estate/architectural framing devoid of human presence — forbidden as 'RealEstateShowcase' by StrategyContract.MeaningConstraints",
      "Pricing, offer terms, or promotional copy rendered in-image — handled as post-production overlay per CampaignContract.OfferDefinition"
    ],

    "ConflictResolutions": [
      {
        "conflict": "AttentionPlan softens the window wall/outdoor view via depth-of-field, but PreservationContract for entity_02 requires Critical/Close-Match recognizability of the FIT24 logo and window-wall structure",
        "resolution": "Resolved at Stage 6 via 'mild softening, logo and window-wall structure remain legible' — carried forward verbatim; no further resolution needed at Synthesis"
      },
      {
        "conflict": "HierarchyPlan requires Primary (runner) to be brightest, but the outdoor view through the window glass is a natural daylight light source and may render with high luminance",
        "resolution": "Resolved at Stage 6 by treating the outdoor view as supporting/atmospheric — its natural brightness as a light source does not override the runner's compositional and focal primacy"
      }
    ],

    "EntitySummary": [
      {
        "entity_id": "entity_01",
        "role": "Primary subject",
        "description": "Urban professional (late 20s–mid 30s), simple casual athletic wear (no third-party logos), running at a steady, calm pace on a treadmill, looking ahead toward the windows, not at camera. Natural skin texture, light realistic sweat sheen, no airbrushing.",
        "luminance_tier": "Brightest",
        "focus_tier": "Critical focus"
      },
      {
        "entity_id": "entity_02",
        "role": "Secondary — recognizable FIT24 environment",
        "description": "Floor-to-ceiling window wall with green outdoor view, circular blue-and-white FIT24 logo, row of black treadmills, black exposed ceiling with ductwork and AC units, polished tile flooring — reproduced from reference_asset_01. Surrounds the runner.",
        "luminance_tier": "Mid (interior elements); outdoor view through glass naturally bright as a light source",
        "focus_tier": "Mild softening on window wall/outdoor view — logo and window-wall structure must remain legible",
        "reference": "reference_asset_01"
      }
    ],

    "LuminanceHierarchy": [
      "entity_01 — Brightest",
      "entity_02 (interior elements: logo, treadmills, ceiling) — Mid",
      "Outdoor view through window glass — naturally bright as a light source, treated as supporting/atmospheric, not compositionally dominant"
    ],

    "PhysicalRendering": {
      "RealityModel": "Photographic, single continuous real-world gym space",
      "CameraSpecs": {
        "shot_type": "Medium shot, slight 3/4 angle from the side, observational framing",
        "framing": "Vertical 4:5, subject off-center (rule of thirds), window wall and FIT24 logo in frame",
        "focal_length_mm": 28,
        "aperture_f_stop": "f/8",
        "depth_of_field_category": "Environmental Context"
      },
      "LightingPlan": {
        "key": "Natural daylight through the window wall, lighting the runner from front/side",
        "fill": "Soft ambient bounce off polished tile flooring and interior surfaces, low contrast",
        "accent": "Cool daylight tone with subtle warm highlight where direct sun catches consoles/flooring",
        "mood": "Bright, airy, calm morning daylight — energizing but not harsh"
      },
      "MaterialPlan": {
        "human_skin_rendering": "Natural texture, visible pores, minor asymmetry, light realistic sweat sheen — no airbrushing or beauty-filter smoothing",
        "glass": "Realistic transparency and subtle reflections on the window wall",
        "metal_and_plastic": "Matte/satin black treadmill finishes matching the reference",
        "tile_flooring": "Polished, slightly reflective grey/dark tile",
        "fabric": "Natural movement and slight sweat-darkening on athletic wear"
      },
      "OpticalPlan": {
        "bokeh_behavior": "Progressive depth-dependent falloff (28mm/f8): entity_01 and nearest treadmills/FIT24 logo critical focus, window wall mildly softened but legible, outdoor greenery most softened"
      },
      "AtmosphericPlan": {
        "air_quality": "Clean, no haze/fog/dust effects"
      }
    },

    "VisualFlow": {
      "entry_point": "Runner's face/upper body",
      "path": "Face/torso -> treadmill console and FIT24 logo -> window wall and mullion lines -> outdoor greenery view",
      "exit_point": "Soft, bright outdoor greenery beyond the glass"
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
      "Depth of Field Realism Assertion — progressive falloff per 28mm/f8, FIT24 logo and window-wall structure remain legible",
      "Recognizability Assertion — entity_02 matches reference_asset_01 (window wall, green outdoor view, FIT24 logo, treadmill row, exposed ceiling)"
    ],

    "ReferenceAssetManifest": [
      {
        "prompt_reference_id": "reference_asset_01",
        "source_filename": "gym_photo_fit24_01.jpg",
        "entity_id": "entity_02",
        "preservation_priority": "Critical",
        "recognizability_requirement": "Close Match (Exact Match for 'FIT24' logo)"
      }
    ]
  }
}
```

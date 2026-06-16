```json
{
  "SceneContract": {
    "Metadata": {
      "brand": "CLEVER Protein",
      "campaign": "Clever Protein clear whey HK OL afternoon tea trial acquisition",
      "framework": "Scene Assembly v5.2.5",
      "stage": "5 — Scene Construction",
      "reference_images_provided": 4,
      "client_preference_contract_present": false,
      "generation_mode": "Partial Generation (reference-guided)",
      "default_assumptions_applied": [
        "Hero a single flavor (lemon clear protein) rather than a multi-flavor lineup — resolves ClientConfirmation 'Multi-flavor product lineup' to single hero.",
        "Human subject is generated as an HK OL persona, not a preserved talent identity — resolves ClientConfirmation 'Female model as recurring face' to flexible.",
        "Timing clock/educational motif treated as flexible and dropped — resolves ClientConfirmation 'Protein timing visual motif' to reference-only.",
        "Grape variant and dual-gender running motif excluded — off-concept for the office afternoon-tea scene."
      ]
    },

    "RealityModel": {
      "type": "Realistic",
      "coherence_rules": {
        "scale": "realistic",
        "perspective": "realistic",
        "anchoring": "required",
        "environmental_behavior": "realistic"
      },
      "rationale": "Art Direction calls for an everyday, achievable 3:30pm office moment — a believable lifestyle photograph, not a stylized or symbolic render."
    },

    "Entities": [
      {
        "id": "entity_01",
        "description": "Hong Kong office lady, healthy and naturally attractive young East Asian woman (approx. 25–32), seated at her desk during an afternoon work break, calm and lightly satisfied, holding/about to sip a clear protein drink. Recast persona of the target audience — not a preserved talent.",
        "roles": ["Identity-Bearing"],
        "source": "Generated"
      },
      {
        "id": "entity_02",
        "description": "CLEVER CLEAR PROTEIN lemon-flavor pouch (hero packshot): white pouch, large blue 'CLEAR PROTEIN' typography, yellow lemon-flavor accent strip and badges, CLEVER logo. Standing on the desk beside the drink.",
        "roles": ["Brand-Bearing", "Product"],
        "source": "Reference Asset",
        "asset_id": "asset_01",
        "prompt_reference_id": "reference_asset_01"
      },
      {
        "id": "entity_03",
        "description": "Transparent shaker bottle containing pale yellow, clear (non-milky) protein beverage with a fresh lemon slice, CLEVER logo on the bottle. The drinking vessel the OL holds — primary refreshment cue.",
        "roles": ["Brand-Bearing", "Product"],
        "source": "Reference Asset",
        "asset_id": "asset_01",
        "prompt_reference_id": "reference_asset_01"
      },
      {
        "id": "entity_04",
        "description": "CLEVER brand logo / wordmark as observed in clean layout reference (black CLEVER mark) plus the 'Made in Japan / 日本製' cue.",
        "roles": ["Brand-Bearing"],
        "source": "Reference Asset",
        "asset_id": "asset_04",
        "prompt_reference_id": "reference_asset_02"
      },
      {
        "id": "entity_05",
        "description": "Bright, clean, minimal Hong Kong office workspace at ~3:30pm: tidy desk, laptop, soft daylight, light/sky-blue and white tonality, a subtle afternoon-time cue (small desk clock reading ~3:30). Light airy 'calm desk sanctuary'.",
        "roles": ["Environmental"],
        "source": "Generated"
      }
    ],

    "Relationships": [
      { "subject": "entity_01", "relation": "holding", "object": "entity_03" },
      { "subject": "entity_03", "relation": "adjacent_to", "object": "entity_02" },
      { "subject": "entity_02", "relation": "resting_on", "object": "entity_05" },
      { "subject": "entity_04", "relation": "appears_on", "object": "entity_03" },
      { "subject": "entity_04", "relation": "appears_on", "object": "entity_02" },
      { "subject": "entity_01", "relation": "seated_within", "object": "entity_05" }
    ],

    "AnchorRelationships": [
      { "entity_id": "entity_01", "anchor_type": "seated_chair_anchored" },
      { "entity_id": "entity_02", "anchor_type": "desk_surface_anchored" },
      { "entity_id": "entity_03", "anchor_type": "hand_held_anchored" },
      { "entity_id": "entity_05", "anchor_type": "scene_environment" }
    ],

    "DepthStructure": {
      "foreground": ["entity_03", "entity_02"],
      "midground": ["entity_01"],
      "background": ["entity_05"]
    },

    "RelativeScale": [
      { "entity_id": "entity_03", "reference_entity": "entity_01", "scale_relationship": "Shaker is hand-sized, held by the OL; reads as a normal beverage bottle relative to her hand and face." },
      { "entity_id": "entity_02", "reference_entity": "entity_03", "scale_relationship": "Pouch is true protein-pouch scale, slightly taller than the shaker, standing on the desk beside it." },
      { "entity_id": "entity_01", "reference_entity": "entity_05", "scale_relationship": "Seated adult at true human scale within an ordinary office workspace." }
    ],

    "GenerationRequirements": {
      "required_entities": ["entity_01", "entity_02", "entity_03", "entity_04", "entity_05"],
      "required_supporting_objects": [
        "Transparent shaker with clear pale-yellow lemon drink (hero refreshment cue)",
        "CLEVER lemon-flavor pouch packshot (single hero flavor)",
        "Subtle afternoon-time cue (small desk clock ~3:30 or equivalent office-afternoon signal)"
      ],
      "required_environment_elements": [
        "Bright, clean, minimal office desk surface",
        "Light / sky-blue + white tonality consistent with brand visual system",
        "Soft daylight suggesting a calm afternoon work break"
      ],
      "reference_locked_entities": [
        {
          "entity_id": "entity_02",
          "asset_id": "asset_01",
          "prompt_reference_id": "reference_asset_01",
          "rule": "Reproduce CLEVER lemon-flavor pouch from reference image. Do not generate packaging from training data."
        },
        {
          "entity_id": "entity_03",
          "asset_id": "asset_01",
          "prompt_reference_id": "reference_asset_01",
          "rule": "Reproduce transparent shaker with clear pale-yellow drink and CLEVER logo from reference image. Drink must read clear/translucent, never opaque or milky. Do not generate from training data."
        },
        {
          "entity_id": "entity_04",
          "asset_id": "asset_04",
          "prompt_reference_id": "reference_asset_02",
          "rule": "Reproduce CLEVER logo / wordmark exactly from reference image. Do not redraw from memory."
        }
      ]
    },

    "PreservationContracts": [
      {
        "entity_id": "entity_01",
        "preservation_priority": "High",
        "recognizability_requirement": "Loose Match",
        "source": "Generated",
        "immutable_attributes": [
          "Young East Asian adult woman, naturally healthy and attractive, not hyper-muscular and not a gym/fitness archetype",
          "Office-appropriate, polished-casual wardrobe (light, clean, not athletic gym wear)",
          "Calm, lightly satisfied, guilt-free expression — quiet confidence, not performance"
        ],
        "flexible_attributes": [
          "Exact facial identity (generated persona, no preserved talent)",
          "Hairstyle and exact wardrobe details",
          "Exact pose and gaze direction (seated, holding/sipping)",
          "Lighting on the subject"
        ],
        "client_preference_influence": null
      },
      {
        "entity_id": "entity_02",
        "preservation_priority": "Critical",
        "recognizability_requirement": "Near Exact",
        "source": "Reference Asset",
        "asset_id": "asset_01",
        "prompt_reference_id": "reference_asset_01",
        "immutable_attributes": [
          "White pouch architecture with large blue 'CLEAR PROTEIN' typography",
          "Yellow lemon-flavor accent strip and badges",
          "CLEVER logo mark shape and orientation on the pack",
          "Lemon flavor as the single hero variant"
        ],
        "flexible_attributes": [
          "Scale relative to scene",
          "Rotation / viewing angle",
          "Placement on the desk",
          "Lighting on the pack surface"
        ],
        "generation_rule": "Use reference_asset_01 — do not generate packaging from training data"
      },
      {
        "entity_id": "entity_03",
        "preservation_priority": "Critical",
        "recognizability_requirement": "Near Exact",
        "source": "Reference Asset",
        "asset_id": "asset_01",
        "prompt_reference_id": "reference_asset_01",
        "immutable_attributes": [
          "Transparent shaker bottle showing the drink inside",
          "Clear, translucent pale-yellow beverage (never opaque, never milky)",
          "Fresh lemon slice / lemon refreshment cue",
          "CLEVER logo on the bottle"
        ],
        "flexible_attributes": [
          "Exact bottle shape variant",
          "Fill level",
          "Rotation and placement",
          "Held vs. resting (held by entity_01)"
        ],
        "generation_rule": "Use reference_asset_01 — clear drink mandatory; do not generate from training data"
      },
      {
        "entity_id": "entity_04",
        "preservation_priority": "High",
        "recognizability_requirement": "Exact Match",
        "source": "Reference Asset",
        "asset_id": "asset_04",
        "prompt_reference_id": "reference_asset_02",
        "immutable_attributes": [
          "CLEVER wordmark letterform and proportions",
          "'Made in Japan / 日本製' cue present somewhere legible"
        ],
        "flexible_attributes": [
          "Logo placement in the new layout",
          "Logo scale",
          "Background surface the logo sits on"
        ],
        "generation_rule": "Use reference_asset_02 — reproduce logo exactly; do not redraw from memory"
      },
      {
        "entity_id": "entity_05",
        "preservation_priority": "High",
        "recognizability_requirement": "Approximate Match",
        "source": "Generated",
        "immutable_attributes": [
          "Bright, clean, minimal indoor office workspace",
          "Light / sky-blue + white brand tonality",
          "Reads as an office afternoon (not a gym, not a home kitchen, not outdoors)"
        ],
        "flexible_attributes": [
          "Exact desk layout and furniture",
          "Window geometry and greenery",
          "Supporting desk objects",
          "Exact afternoon-time cue execution"
        ],
        "client_preference_influence": null
      }
    ]
  },

  "ReferenceAssetManifest": [
    {
      "asset_id": "asset_01",
      "filename": "reference_01.jpg",
      "type": "Brand-Bearing / Product",
      "prompt_reference_id": "reference_asset_01",
      "attach_to_api_call": true,
      "strictness": "Exact",
      "note": "Source of the lemon-flavor pouch AND the transparent clear-drink shaker. Human/gym context in this reference is NOT preserved — product and shaker only."
    },
    {
      "asset_id": "asset_04",
      "filename": "reference_04.jpg",
      "type": "Brand-Bearing",
      "prompt_reference_id": "reference_asset_02",
      "attach_to_api_call": true,
      "strictness": "Exact",
      "note": "Source of the CLEVER logo/wordmark and the clean sky-blue minimal brand layout language. Timing-clock graphic and specific model are NOT preserved."
    }
  ],

  "AssetsConsideredButNotAttached": [
    {
      "asset_id": "asset_02",
      "reason": "Grape variant + dual-gender outdoor running motif — off-concept for a single-hero lemon office afternoon scene."
    },
    {
      "asset_id": "asset_03",
      "reason": "Multi-flavor (three-pack) lineup. Excluded to keep a single hero flavor; attaching it risks the generator rendering three packs. Its clean sky-blue minimal style is already represented via reference_asset_02."
    }
  ]
}
```

```json
{
  "SceneContract": {
    "Metadata": {
      "brand": "CLEVER Protein",
      "campaign": "日本製輕盈美學 — HK OL afternoon tea trial acquisition",
      "framework": "Scene Assembly v5.2.5",
      "stage": "5 — Scene Construction",
      "reference_images_provided": 2,
      "reference_images_used": ["image1.png (reference_asset_01)", "image4.png (reference_asset_02)"],
      "client_preference_contract_present": false,
      "generation_mode": "Partial Generation — brand assets (pack, shaker, logo) reproduced from references; human subject and environment fully generated"
    },

    "RealityModel": {
      "type": "Realistic",
      "coherence_rules": {
        "scale": "realistic",
        "perspective": "realistic",
        "anchoring": "required",
        "environmental_behavior": "realistic"
      },
      "rationale": "Art Direction requires an everyday, believable lifestyle photograph — commercial realism with a photoshoot-set quality clean background."
    },

    "Entities": [
      {
        "id": "entity_01",
        "description": "Hong Kong office lady, naturally healthy and attractive, approximately 25–32 years old, East Asian, in light polished-casual office wear (not athletic or gym wear). Seated on break, calm and quietly confident, holding the clear protein shaker or setting it down. Fully generated persona.",
        "roles": ["Identity-Bearing"],
        "source": "Generated"
      },
      {
        "id": "entity_02",
        "description": "CLEVER CLEAR PROTEIN lemon-flavor pouch: white body, large dark-blue 'CLEAR PROTEIN' typography, bright yellow lemon flavor band at top with lemon imagery, functional badges (0脂·0膽固醇·O奶味·低糖 / 100%WPI). Resting on desk surface facing camera.",
        "roles": ["Brand-Bearing", "Product"],
        "source": "Reference Asset",
        "asset_id": "asset_01",
        "prompt_reference_id": "reference_asset_01"
      },
      {
        "id": "entity_03",
        "description": "Transparent shaker bottle with pale-yellow, clear (non-milky) protein drink inside, lemon slice visible. CLEVER logo on the bottle body. Held by entity_01 or placed on desk near her.",
        "roles": ["Brand-Bearing", "Product"],
        "source": "Reference Asset",
        "asset_id": "asset_01",
        "prompt_reference_id": "reference_asset_01"
      },
      {
        "id": "entity_04",
        "description": "CLEVER wordmark / logo mark (stylized C + CLEVER text) and legible 'Made in Japan / 日本製' cue appearing in the image — on the pack and/or on the shaker body.",
        "roles": ["Brand-Bearing"],
        "source": "Reference Asset",
        "asset_id": "asset_04",
        "prompt_reference_id": "reference_asset_02"
      },
      {
        "id": "entity_05",
        "description": "Clean, minimal office desk surface — near-empty, photoshoot-set quality. Sky-blue and white register. Only prop allowed: a small desk clock showing approximately 3:30pm. No other desk clutter, no stationery piles, no food, no papers. The desk reads as a curated, controlled surface.",
        "roles": ["Environmental"],
        "source": "Generated"
      },
      {
        "id": "entity_06",
        "description": "Background — clean, minimal, near-empty. Sky-blue to white gradient or flat sky-blue wall. No windows, no visible office furniture behind the subject, no visible people or plant life competing for attention. Think: clean photography studio cyclorama wall that reads as 'office' only through tonality and the desk surface, not through background detail.",
        "roles": ["Environmental"],
        "source": "Generated"
      }
    ],

    "Relationships": [
      { "subject": "entity_01", "relation": "seated_at", "object": "entity_05" },
      { "subject": "entity_03", "relation": "held_by_or_adjacent_to", "object": "entity_01" },
      { "subject": "entity_02", "relation": "resting_on", "object": "entity_05" },
      { "subject": "entity_02", "relation": "adjacent_to", "object": "entity_03" },
      { "subject": "entity_04", "relation": "appears_on", "object": "entity_02" },
      { "subject": "entity_04", "relation": "appears_on", "object": "entity_03" },
      { "subject": "entity_01", "relation": "positioned_in_front_of", "object": "entity_06" }
    ],

    "AnchorRelationships": [
      { "entity_id": "entity_01", "anchor_type": "seated_chair_anchored" },
      { "entity_id": "entity_02", "anchor_type": "desk_surface_anchored" },
      { "entity_id": "entity_03", "anchor_type": "hand_held_or_desk_anchored" },
      { "entity_id": "entity_05", "anchor_type": "scene_surface" },
      { "entity_id": "entity_06", "anchor_type": "scene_backdrop" }
    ],

    "DepthStructure": {
      "foreground": ["entity_02", "entity_03"],
      "midground": ["entity_01", "entity_05"],
      "background": ["entity_06"]
    },

    "RelativeScale": [
      { "entity_id": "entity_03", "reference_entity": "entity_01", "scale_relationship": "Hand-sized shaker, normal beverage bottle scale relative to the OL's hand." },
      { "entity_id": "entity_02", "reference_entity": "entity_03", "scale_relationship": "Protein pouch is slightly taller than the shaker; both near the camera in the foreground." },
      { "entity_id": "entity_05", "reference_entity": "entity_01", "scale_relationship": "Desk surface — normal adult-height desk; only the clean top surface is visible in frame." }
    ],

    "GenerationRequirements": {
      "required_entities": ["entity_01", "entity_02", "entity_03", "entity_04", "entity_05", "entity_06"],
      "required_supporting_objects": [
        "Small desk clock showing approximately 3:30 — the only desk prop beyond the pack and shaker"
      ],
      "required_environment_elements": [
        "Clean, near-empty desk surface — photoshoot-set quality, no visible clutter",
        "Sky-blue and white background register",
        "Soft daylight quality lighting consistent with an afternoon break"
      ],
      "explicitly_excluded_objects": [
        "No laptop or computer visible in frame",
        "No stationery, papers, cups, or food on the desk",
        "No plants or greenery",
        "No office furniture or shelving in the background",
        "No other people",
        "No windows or bright light sources in the background",
        "No floor-to-ceiling gym windows (image1.png background must NOT carry through)"
      ],
      "reference_locked_entities": [
        {
          "entity_id": "entity_02",
          "asset_id": "asset_01",
          "prompt_reference_id": "reference_asset_01",
          "rule": "Reproduce CLEVER lemon CLEAR PROTEIN pouch from image1.png. Product packaging only — ignore model and gym background."
        },
        {
          "entity_id": "entity_03",
          "asset_id": "asset_01",
          "prompt_reference_id": "reference_asset_01",
          "rule": "Reproduce transparent shaker with clear pale-yellow lemon drink and CLEVER logo from image1.png. Drink must read clear and translucent — never opaque or milky."
        },
        {
          "entity_id": "entity_04",
          "asset_id": "asset_04",
          "prompt_reference_id": "reference_asset_02",
          "rule": "Reproduce CLEVER logo/wordmark from image4.png. Use image4's minimal sky-blue aesthetic as the target visual register. Exclude timing-clock graphic and specific model."
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
          "Young East Asian adult woman, healthy and naturally attractive — not hyper-muscular, not gym archetype",
          "Light, polished-casual office wear (clean, not athletic)",
          "Calm, lightly satisfied, guilt-free expression and relaxed body language"
        ],
        "flexible_attributes": [
          "Exact facial identity (fully generated persona)",
          "Specific hairstyle and outfit details",
          "Exact pose — holding shaker or setting it down, soft smile or content composure"
        ]
      },
      {
        "entity_id": "entity_02",
        "preservation_priority": "Critical",
        "recognizability_requirement": "Near Exact",
        "source": "Reference Asset",
        "asset_id": "asset_01",
        "prompt_reference_id": "reference_asset_01",
        "immutable_attributes": [
          "White pouch body",
          "Large dark-blue 'CLEAR PROTEIN' typography across middle",
          "Bright yellow lemon-flavor accent band at top",
          "CLEVER logo on pack",
          "Functional badges (0脂·0膽固醇·O奶味·低糖 / 100%WPI)"
        ],
        "flexible_attributes": [
          "Scale relative to scene",
          "Viewing angle and rotation",
          "Desk placement",
          "Lighting on pack surface"
        ],
        "generation_rule": "Reproduce from reference_asset_01 — do not generate packaging from training data"
      },
      {
        "entity_id": "entity_03",
        "preservation_priority": "Critical",
        "recognizability_requirement": "Near Exact",
        "source": "Reference Asset",
        "asset_id": "asset_01",
        "prompt_reference_id": "reference_asset_01",
        "immutable_attributes": [
          "Transparent / clear shaker bottle body",
          "Clear, pale-yellow translucent liquid — light passes through; never opaque or milky",
          "Lemon slice visible inside or as garnish",
          "CLEVER logo on bottle"
        ],
        "flexible_attributes": [
          "Fill level",
          "Exact rotation and angle",
          "Held vs. resting on desk"
        ],
        "generation_rule": "Reproduce from reference_asset_01 — clear liquid mandatory; do not generate from training data"
      },
      {
        "entity_id": "entity_04",
        "preservation_priority": "High",
        "recognizability_requirement": "Exact Match",
        "source": "Reference Asset",
        "asset_id": "asset_04",
        "prompt_reference_id": "reference_asset_02",
        "immutable_attributes": [
          "CLEVER wordmark letterforms and proportions",
          "'Made in Japan / 日本製' legible in frame"
        ],
        "flexible_attributes": [
          "Logo placement in layout",
          "Logo scale",
          "Logo color variant (black on light background)"
        ],
        "generation_rule": "Reproduce CLEVER logo from reference_asset_02 — do not redraw from memory; exclude timing-clock and pricing from that reference"
      },
      {
        "entity_id": "entity_05",
        "preservation_priority": "Critical",
        "recognizability_requirement": "Approximate Match",
        "source": "Generated",
        "immutable_attributes": [
          "Near-empty desk surface — only the pack, shaker, and small clock visible; nothing else",
          "Sky-blue and white tonality",
          "Clean, photoshoot-set quality — no visible clutter, crumbs, papers, or random objects"
        ],
        "flexible_attributes": [
          "Exact desk material (white, light wood, or light grey surface)",
          "Small clock execution and exact position"
        ]
      },
      {
        "entity_id": "entity_06",
        "preservation_priority": "Critical",
        "recognizability_requirement": "Approximate Match",
        "source": "Generated",
        "immutable_attributes": [
          "Clean, uncluttered background — no furniture, no shelving, no plants, no windows behind subject",
          "Sky-blue or soft white register — feels like a controlled studio cyclorama or a clean painted wall",
          "No bright light sources in the background competing with the subject"
        ],
        "flexible_attributes": [
          "Exact background color — flat sky-blue or sky-blue-to-white gradient",
          "Degree of DoF softening applied to background"
        ]
      }
    ]
  },

  "ReferenceAssetManifest": [
    {
      "asset_id": "asset_01",
      "filename": "image1.png",
      "type": "Brand-Bearing",
      "prompt_reference_id": "reference_asset_01",
      "attach_to_api_call": true,
      "strictness": "Exact",
      "note": "Source of lemon CLEAR PROTEIN pouch and transparent shaker. Use product + bottle only; discard male model and gym background entirely."
    },
    {
      "asset_id": "asset_04",
      "filename": "image4.png",
      "type": "Brand-Bearing",
      "prompt_reference_id": "reference_asset_02",
      "attach_to_api_call": true,
      "strictness": "Exact",
      "note": "Source of CLEVER logo/wordmark and minimal sky-blue aesthetic register. Exclude timing-clock, model, and educational copy."
    }
  ]
}
```

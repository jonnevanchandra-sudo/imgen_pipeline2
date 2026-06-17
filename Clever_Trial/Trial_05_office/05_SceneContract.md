```json
{
  "SceneContract": {
    "Metadata": {
      "brand": "CLEVER Protein",
      "campaign": "日本製輕盈美學 — HK OL afternoon tea trial acquisition",
      "framework": "Scene Assembly v5.2.5",
      "stage": "5 — Scene Construction",
      "variant": "Trial_05_office — office desk setting, female model face from image 5.png, on-image ad typography",
      "reference_images_provided": 3,
      "reference_images_used": [
        "image1.png (reference_asset_01)",
        "image4.png (reference_asset_02)",
        "image 5.png (reference_asset_03)"
      ],
      "client_preference_contract_present": false,
      "generation_mode": "Partial Generation — brand assets (pack, shaker, logo) reproduced from image1/image4; human subject face reproduced from image 5.png; environment and typography overlay fully generated",
      "inherits_from": "Trial_04_office/05_SceneContract.md — only entity_01 and PreservationContract[entity_01] change"
    },

    "RealityModel": {
      "type": "Realistic",
      "coherence_rules": {
        "scale": "realistic",
        "perspective": "realistic",
        "anchoring": "required",
        "environmental_behavior": "realistic"
      },
      "rationale": "Art Direction requires an everyday, believable lifestyle advertisement — commercial realism with a photoshoot-set quality clean background and integrated ad typography."
    },

    "Entities": [
      {
        "id": "entity_01",
        "description": "Female model from image 5.png — East Asian, early-to-mid twenties, hair in a neat bun/updo, lean and naturally healthy build, bright natural complexion. Dressed in polished-casual office wear (clean blouse or fitted top — NOT the sports bra from the reference image). Seated at a near-empty desk on her afternoon break, calm, lightly satisfied, quietly confident. Holding or reaching for the transparent shaker of clear lemon protein drink. Face and look reproduced from reference_asset_03 (image 5.png).",
        "roles": ["Identity-Bearing"],
        "source": "Reference Asset",
        "asset_id": "asset_05",
        "prompt_reference_id": "reference_asset_03"
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
        "description": "Background — clean, minimal, near-empty. Sky-blue to white gradient or flat sky-blue wall. No windows, no visible office furniture behind the subject, no visible people or plant life. Think: clean photography studio cyclorama wall readable as 'office' only through tonality and the desk surface, not through background detail.",
        "roles": ["Environmental"],
        "source": "Generated"
      },
      {
        "id": "entity_07",
        "description": "On-image advertisement typography overlay — integrated into the sky-blue background plane. Headline: '告別3點3罪惡感！' in large, bold, clean modern sans-serif. Subtitle below: '日本製 · 清蛋白' in smaller text. Positioned in the upper portion of the frame, not overlapping the model's face or the product hero cluster. White or dark-blue text for maximum legibility against the background.",
        "roles": ["Typography-Overlay", "Campaign-Mandatory"],
        "source": "Generated",
        "preservation_priority": "Critical"
      }
    ],

    "Relationships": [
      { "subject": "entity_01", "relation": "seated_at", "object": "entity_05" },
      { "subject": "entity_03", "relation": "held_by_or_adjacent_to", "object": "entity_01" },
      { "subject": "entity_02", "relation": "resting_on", "object": "entity_05" },
      { "subject": "entity_02", "relation": "adjacent_to", "object": "entity_03" },
      { "subject": "entity_04", "relation": "appears_on", "object": "entity_02" },
      { "subject": "entity_04", "relation": "appears_on", "object": "entity_03" },
      { "subject": "entity_01", "relation": "positioned_in_front_of", "object": "entity_06" },
      { "subject": "entity_07", "relation": "overlaid_on", "object": "entity_06" }
    ],

    "AnchorRelationships": [
      { "entity_id": "entity_01", "anchor_type": "seated_chair_anchored" },
      { "entity_id": "entity_02", "anchor_type": "desk_surface_anchored" },
      { "entity_id": "entity_03", "anchor_type": "hand_held_or_desk_anchored" },
      { "entity_id": "entity_05", "anchor_type": "scene_surface" },
      { "entity_id": "entity_06", "anchor_type": "scene_backdrop" },
      { "entity_id": "entity_07", "anchor_type": "background_overlay" }
    ],

    "DepthStructure": {
      "foreground": ["entity_02", "entity_03"],
      "midground": ["entity_01", "entity_05"],
      "background": ["entity_06", "entity_07"]
    },

    "RelativeScale": [
      { "entity_id": "entity_03", "reference_entity": "entity_01", "scale_relationship": "Hand-sized shaker, normal beverage bottle scale relative to the model's hand." },
      { "entity_id": "entity_02", "reference_entity": "entity_03", "scale_relationship": "Protein pouch slightly taller than the shaker; both near the camera in the foreground." },
      { "entity_id": "entity_05", "reference_entity": "entity_01", "scale_relationship": "Desk surface — normal adult-height desk; only the clean top surface visible in frame." },
      { "entity_id": "entity_07", "reference_entity": "entity_06", "scale_relationship": "Typography occupies the upper background zone — headline legible on mobile; subtitle approximately half the headline size." }
    ],

    "GenerationRequirements": {
      "required_entities": ["entity_01", "entity_02", "entity_03", "entity_04", "entity_05", "entity_06", "entity_07"],
      "required_supporting_objects": [
        "Small desk clock showing approximately 3:30 — the only desk prop beyond the pack and shaker"
      ],
      "required_environment_elements": [
        "Clean, near-empty desk surface — photoshoot-set quality, no visible clutter",
        "Sky-blue and white background register",
        "Soft daylight quality lighting consistent with an afternoon break"
      ],
      "required_visual_overlays": [
        "On-image advertisement typography: bold modern sans-serif headline '告別3點3罪惡感！' in the upper background zone; subtitle '日本製 · 清蛋白' smaller below it. Positioned in the sky-blue background plane, above and clear of the model and product cluster. Campaign-mandatory — must be present and legible."
      ],
      "explicitly_excluded_objects": [
        "No laptop or computer visible in frame",
        "No stationery, papers, cups, or food on the desk",
        "No plants or greenery",
        "No office furniture or shelving in the background",
        "No other people",
        "No windows or bright light sources in the background",
        "No text or typography beyond the specified on-image ad copy ('告別3點3罪惡感！' + '日本製 · 清蛋白')",
        "Do not reproduce the sports bra, shaker, or outdoor mountain background from image 5.png — face and hair only"
      ],
      "reference_locked_entities": [
        {
          "entity_id": "entity_01",
          "asset_id": "asset_05",
          "prompt_reference_id": "reference_asset_03",
          "rule": "Reproduce the female model's face, neat hair bun, and look from image 5.png. Dress her in polished-casual office wear. Discard sports bra, shaker, and outdoor background from that image entirely."
        },
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
          "rule": "Reproduce transparent shaker with clear pale-yellow lemon drink and CLEVER logo from image1.png. Clear liquid mandatory."
        },
        {
          "entity_id": "entity_04",
          "asset_id": "asset_04",
          "prompt_reference_id": "reference_asset_02",
          "rule": "Reproduce CLEVER logo/wordmark from image4.png. Use image4's minimal sky-blue aesthetic as visual register. Exclude timing-clock and model."
        }
      ]
    },

    "PreservationContracts": [
      {
        "entity_id": "entity_01",
        "preservation_priority": "High",
        "recognizability_requirement": "Near Exact — face and hair must match the model in image 5.png",
        "source": "Reference Asset",
        "asset_id": "asset_05",
        "prompt_reference_id": "reference_asset_03",
        "immutable_attributes": [
          "East Asian female, early-to-mid twenties — do not alter ethnicity, age register, or gender",
          "Hair in a neat bun or updo — clean, polished office-ready styling",
          "Lean, naturally healthy build — not muscular",
          "Bright, natural complexion — warm light skin tone, natural texture",
          "Calm, lightly satisfied, guilt-free expression and relaxed body language"
        ],
        "flexible_attributes": [
          "Clothing — must be polished-casual office wear (blouse, fitted top), NOT the sports bra from the reference image",
          "Exact expression (may shift from subtle off-camera gaze to relaxed look toward the drink, or soft content composure)",
          "Exact head tilt and body angle"
        ],
        "generation_rule": "Reproduce this woman's face, neat hair bun, and overall look from reference_asset_03 (image 5.png). Dress her in polished-casual office wear in the generated scene. Discard sports bra, shaker, and mountain background from that image entirely."
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
        "flexible_attributes": ["Scale relative to scene", "Viewing angle and rotation", "Desk placement", "Lighting on pack surface"],
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
        "flexible_attributes": ["Fill level", "Exact rotation and angle", "Held vs. resting on desk"],
        "generation_rule": "Reproduce from reference_asset_01 — clear liquid mandatory. Do NOT use the shaker from image 5.png."
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
        "flexible_attributes": ["Logo placement in layout", "Logo scale", "Logo color variant"],
        "generation_rule": "Reproduce CLEVER logo from reference_asset_02 — do not redraw from memory"
      },
      {
        "entity_id": "entity_05",
        "preservation_priority": "Critical",
        "recognizability_requirement": "Approximate Match",
        "source": "Generated",
        "immutable_attributes": [
          "Near-empty desk surface — only the pack, shaker, and small clock visible; nothing else",
          "Sky-blue and white tonality",
          "Clean, photoshoot-set quality — no visible clutter"
        ],
        "flexible_attributes": ["Exact desk material", "Small clock execution and exact position"]
      },
      {
        "entity_id": "entity_06",
        "preservation_priority": "Critical",
        "recognizability_requirement": "Approximate Match",
        "source": "Generated",
        "immutable_attributes": [
          "Clean, uncluttered background — no furniture, shelving, plants, or windows behind subject",
          "Sky-blue or soft white register",
          "No bright light sources in the background"
        ],
        "flexible_attributes": ["Exact background color", "Degree of DoF softening"]
      },
      {
        "entity_id": "entity_07",
        "preservation_priority": "Critical",
        "recognizability_requirement": "Near Exact",
        "source": "Generated",
        "immutable_attributes": [
          "Headline text content: '告別3點3罪惡感！' — exact characters, no substitution",
          "Subtitle text content: '日本製 · 清蛋白' — exact characters",
          "Positioned in upper background zone, not overlapping model or product cluster",
          "Legible at mobile screen size"
        ],
        "flexible_attributes": [
          "Exact font weight and style (bold modern sans-serif preferred)",
          "Text color — white or dark-blue, whichever reads best against background",
          "Precise pixel position within upper zone"
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
      "note": "Source of lemon CLEAR PROTEIN pouch and transparent shaker. Product + bottle only; discard the model and gym background."
    },
    {
      "asset_id": "asset_04",
      "filename": "image4.png",
      "type": "Brand-Bearing",
      "prompt_reference_id": "reference_asset_02",
      "attach_to_api_call": true,
      "strictness": "Exact",
      "note": "Source of CLEVER logo/wordmark and minimal sky-blue aesthetic register. Exclude timing-clock, model, and copy."
    },
    {
      "asset_id": "asset_05",
      "filename": "image 5.png",
      "type": "Identity-Bearing",
      "prompt_reference_id": "reference_asset_03",
      "attach_to_api_call": true,
      "strictness": "Near Exact — face and hair only",
      "note": "Source of female model face and look. Extract only the person — discard sports bra, shaker, and outdoor mountain background. Dress model in office wear in the generated scene."
    }
  ]
}
```

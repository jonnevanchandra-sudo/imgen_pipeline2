```json
{
  "SceneContract": {
    "Metadata": {
      "brand": "CLEVER Protein",
      "campaign": "日本製清蛋白 · 輕盈恢復力 — male post-workout light recovery trial acquisition",
      "framework": "Scene Assembly v5.2.5",
      "stage": "5 — Scene Construction",
      "variant": "Trial_06_gym_male — bright window-lit studio, male model face from image7.png + image (1).png, on-image ad typography, generated from scratch",
      "reference_images_provided": 4,
      "reference_images_used": [
        "image1.png (reference_asset_01)",
        "image4.png (reference_asset_02)",
        "image7.png (reference_asset_03)",
        "image (1).png (reference_asset_04)"
      ],
      "client_preference_contract_present": false,
      "generation_mode": "Partial Generation — brand assets (pack, shaker, logo) reproduced from image1/image4; human subject face reproduced from image7.png + image (1).png; environment and typography overlay fully generated",
      "inherits_from": "None — this contract chain (01–08) was generated from scratch for Trial_06_gym_male, not inherited from Trial_04_gym or Trial_04_gym_male, to avoid carrying over the female-OL-coded Campaign/Strategy/Narrative/Art Direction language those variants were built on."
    },

    "RealityModel": {
      "type": "Realistic",
      "coherence_rules": {
        "scale": "realistic",
        "perspective": "realistic",
        "anchoring": "required",
        "environmental_behavior": "realistic"
      },
      "rationale": "Art Direction requires an everyday, believable lifestyle advertisement — commercial realism with a bright, clean window-lit studio backdrop and integrated ad typography."
    },

    "Entities": [
      {
        "id": "entity_01",
        "description": "Male model — East Asian, mid-twenties, short-to-medium dark hair swept back/upward, lean athletic build with visible muscle tone (toned, not bodybuilder-bulky), defined jawline. Face and look reproduced from reference_asset_03 (image7.png) and reference_asset_04 (image (1).png) — same person, two angles. Wearing a light athletic t-shirt (white or light blue, clean modern sportswear), NOT the dark tank top seen in the reference images. Post-workout cool-down — calm, quietly satisfied, holding the clear protein shaker or just having finished drinking.",
        "roles": ["Identity-Bearing"],
        "source": "Reference Asset",
        "asset_ids": ["asset_07", "asset_08"],
        "prompt_reference_ids": ["reference_asset_03", "reference_asset_04"]
      },
      {
        "id": "entity_02",
        "description": "CLEVER CLEAR PROTEIN lemon-flavor pouch: white body, large dark-blue 'CLEAR PROTEIN' typography, bright yellow lemon flavor band at top with lemon imagery, functional badges (0脂·0膽固醇·O奶味·低糖 / 100%WPI). Resting on the clean studio floor surface or a nearby low bench, facing the camera.",
        "roles": ["Brand-Bearing", "Product"],
        "source": "Reference Asset",
        "asset_id": "asset_01",
        "prompt_reference_id": "reference_asset_01"
      },
      {
        "id": "entity_03",
        "description": "Transparent shaker bottle with pale-yellow, clear (non-milky) protein drink inside, lemon slice visible. CLEVER logo on the bottle body. Held by entity_01 or placed on the floor beside him.",
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
        "description": "Clean studio floor surface — light wood planks or pale rubber flooring. Near-empty, photoshoot-set quality. The only prop visible on the floor is a rolled yoga/exercise mat placed to one side. No other gym clutter, no other people's water bottles or bags visible in this zone. The floor reads as a curated, controlled surface.",
        "roles": ["Environmental"],
        "source": "Generated"
      },
      {
        "id": "entity_06",
        "description": "Bright window-lit studio background — large floor-to-ceiling windows dominate the background, flooding the space with soft natural sky-blue daylight. The window light creates a bright, airy backdrop. Studio walls at the far edges are white or pale. No heavy gym equipment, no mirrored walls, no dark surfaces visible. The background reads as bright, open air — a private, elevated studio space.",
        "roles": ["Environmental"],
        "source": "Generated"
      },
      {
        "id": "entity_07",
        "description": "On-image advertisement typography overlay — a visual design element integrated into the bright window-light background plane. Headline: '日日飲，激發體能' in large, bold, clean modern sans-serif. Subtitle below: '日本製 · 清蛋白' in smaller text. Positioned in the upper portion of the frame, within the window-light background zone, not overlapping the model's face or the product hero cluster. Typography must read as a designed ad headline. White text for maximum legibility against the bright sky-blue/natural-light background.",
        "roles": ["Typography-Overlay", "Campaign-Mandatory"],
        "source": "Generated",
        "preservation_priority": "Critical"
      }
    ],

    "Relationships": [
      { "subject": "entity_01", "relation": "standing_on_or_beside", "object": "entity_05" },
      { "subject": "entity_03", "relation": "held_by_or_adjacent_to", "object": "entity_01" },
      { "subject": "entity_02", "relation": "resting_on", "object": "entity_05" },
      { "subject": "entity_02", "relation": "adjacent_to", "object": "entity_03" },
      { "subject": "entity_04", "relation": "appears_on", "object": "entity_02" },
      { "subject": "entity_04", "relation": "appears_on", "object": "entity_03" },
      { "subject": "entity_01", "relation": "positioned_in_front_of", "object": "entity_06" },
      { "subject": "entity_07", "relation": "overlaid_on", "object": "entity_06" }
    ],

    "AnchorRelationships": [
      { "entity_id": "entity_01", "anchor_type": "floor_standing_or_seated_anchored" },
      { "entity_id": "entity_02", "anchor_type": "floor_surface_anchored" },
      { "entity_id": "entity_03", "anchor_type": "hand_held_or_floor_anchored" },
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
      { "entity_id": "entity_03", "reference_entity": "entity_01", "scale_relationship": "Hand-sized shaker, normal beverage bottle scale relative to his hand." },
      { "entity_id": "entity_02", "reference_entity": "entity_03", "scale_relationship": "Protein pouch slightly taller than the shaker; both near the camera in the foreground." },
      { "entity_id": "entity_05", "reference_entity": "entity_01", "scale_relationship": "Studio floor — only the near, clean section of floor immediately around the model visible in frame." },
      { "entity_id": "entity_07", "reference_entity": "entity_06", "scale_relationship": "Typography occupies the upper window-light zone — headline large enough to be legible on a mobile screen; subtitle approximately half the headline size." }
    ],

    "GenerationRequirements": {
      "required_entities": ["entity_01", "entity_02", "entity_03", "entity_04", "entity_05", "entity_06", "entity_07"],
      "required_supporting_objects": [
        "Rolled yoga/exercise mat on the floor to one side of the model — the only prop beyond the pack and shaker"
      ],
      "required_environment_elements": [
        "Clean, near-empty studio floor surface — photoshoot-set quality, no visible clutter",
        "Large floor-to-ceiling windows letting in sky-blue natural daylight — dominant background element",
        "Bright, airy studio atmosphere consistent with a post-workout cool-down"
      ],
      "required_visual_overlays": [
        "On-image advertisement typography: bold modern sans-serif headline '日日飲，激發體能' in the upper window-light background zone; subtitle '日本製 · 清蛋白' smaller below it. Positioned in the bright background plane, above and clear of the model and product cluster. White text on sky-blue/bright-window background. Typography is a campaign-mandatory visual element — it must be present and legible."
      ],
      "explicitly_excluded_objects": [
        "No heavy dumbbells, barbells, or weight machines in any part of the frame",
        "No mirrored gym walls",
        "No other people in the scene",
        "No gym lockers or changing room elements",
        "No dark gym surfaces or harsh artificial spotlights",
        "No floor-to-ceiling gym mirrors (the background must be the window wall, not a mirror wall)",
        "No text or typography beyond the specified on-image ad copy ('日日飲，激發體能' + '日本製 · 清蛋白')",
        "No gym bags, other people's water bottles, or general gym clutter on the floor",
        "Do not reproduce the dark tank top, plank/standing poses, stability ball, houseplant, or window-interior backgrounds from image7.png or image (1).png — face, hair, and build only",
        "Do not reproduce the CLEVER logo styling, ad text, or notification/chat-bubble UI graphic baked into image (1).png — that image is used purely for facial identity, not as a layout or typography reference"
      ],
      "reference_locked_entities": [
        {
          "entity_id": "entity_01",
          "asset_ids": ["asset_07", "asset_08"],
          "prompt_reference_ids": ["reference_asset_03", "reference_asset_04"],
          "rule": "Reproduce the male model's face, hair, and lean athletic build using both image7.png and image (1).png as cross-referenced identity sources. Clothing shifts to a light athletic t-shirt in the CLEVER scene context. Discard pose, activity, wardrobe, background, and any baked-in text/logo/UI graphics from both source images entirely."
        },
        {
          "entity_id": "entity_02",
          "asset_id": "asset_01",
          "prompt_reference_id": "reference_asset_01",
          "rule": "Reproduce CLEVER lemon CLEAR PROTEIN pouch from image1.png. Product packaging only — ignore the model and background in that image."
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
          "rule": "Reproduce CLEVER logo/wordmark from image4.png. Use image4's minimal sky-blue aesthetic as supporting tone reference. Exclude the timing-clock graphic and model from that image."
        }
      ]
    },

    "PreservationContracts": [
      {
        "entity_id": "entity_01",
        "preservation_priority": "High",
        "recognizability_requirement": "Near Exact — face and hair must match the model in image7.png and image (1).png",
        "source": "Reference Asset",
        "asset_ids": ["asset_07", "asset_08"],
        "prompt_reference_ids": ["reference_asset_03", "reference_asset_04"],
        "immutable_attributes": [
          "East Asian male, mid-twenties — do not alter ethnicity, age register, or gender",
          "Short-to-medium dark hair, swept back/upward with natural volume",
          "Defined jawline and facial structure consistent across both reference images",
          "Lean, athletic build with visible muscle tone — toned, not bodybuilder-bulky",
          "Light-medium warm skin tone, natural texture"
        ],
        "flexible_attributes": [
          "Clothing — must be a light athletic t-shirt (white or light blue), NOT the dark tank top from the reference images",
          "Exact expression (plank exertion / neutral in references → calm, lightly satisfied post-workout ease in the generated scene)",
          "Exact head tilt and body angle"
        ],
        "generation_rule": "Reproduce this man's face, hair, and lean build from reference_asset_03 (image7.png) and reference_asset_04 (image (1).png) — treat both as the same identity. Dress him in a light athletic t-shirt in the generated scene. Discard pose, activity, wardrobe, background, and any baked-in text/logo/UI graphics from both source images entirely."
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
        "flexible_attributes": ["Scale relative to scene", "Viewing angle and rotation", "Floor placement", "Lighting on pack surface"],
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
        "flexible_attributes": ["Fill level", "Exact rotation and angle", "Held vs. resting on floor"],
        "generation_rule": "Reproduce from reference_asset_01 — clear liquid mandatory. Do NOT use any bottle visible in image7.png or image (1).png."
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
        "generation_rule": "Reproduce CLEVER logo from reference_asset_02 — do not redraw from memory, and do not copy the logo lockup style from image (1).png."
      },
      {
        "entity_id": "entity_05",
        "preservation_priority": "Critical",
        "recognizability_requirement": "Approximate Match",
        "source": "Generated",
        "immutable_attributes": [
          "Near-empty studio floor surface — only the pack, shaker, and rolled mat visible; nothing else",
          "Light wood or pale rubber flooring tone",
          "Clean, photoshoot-set quality — no visible clutter"
        ],
        "flexible_attributes": ["Exact floor material (wood vs rubber)", "Mat color", "Exact placement of mat"]
      },
      {
        "entity_id": "entity_06",
        "preservation_priority": "Critical",
        "recognizability_requirement": "Approximate Match",
        "source": "Generated",
        "immutable_attributes": [
          "Large floor-to-ceiling windows — dominant background element; sky-blue natural light flooding in",
          "No heavy gym equipment visible in background",
          "No mirrored walls — the background is window glass and bright exterior light",
          "Bright and airy, not dark"
        ],
        "flexible_attributes": ["Exact window framing", "Degree of sky-blue tint in the light", "Degree of DoF softening on the windows"]
      },
      {
        "entity_id": "entity_07",
        "preservation_priority": "Critical",
        "recognizability_requirement": "Near Exact",
        "source": "Generated",
        "immutable_attributes": [
          "Headline text content: '日日飲，激發體能' — exact characters, no substitution",
          "Subtitle text content: '日本製 · 清蛋白' — exact characters",
          "Positioned in upper window-light background zone, not overlapping model or product cluster",
          "Legible at mobile screen size",
          "White text color"
        ],
        "flexible_attributes": [
          "Exact font weight and style (bold modern sans-serif preferred)",
          "Precise pixel position within upper zone",
          "Slight softening from depth-of-field in background zone is acceptable provided legibility is maintained"
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
      "note": "Source of lemon CLEAR PROTEIN pouch and transparent shaker. Use product + bottle only; discard the male model and gym floor background from that image entirely."
    },
    {
      "asset_id": "asset_04",
      "filename": "image4.png",
      "type": "Brand-Bearing",
      "prompt_reference_id": "reference_asset_02",
      "attach_to_api_call": true,
      "strictness": "Exact",
      "note": "Source of CLEVER logo/wordmark and minimal sky-blue aesthetic register. Exclude timing-clock graphic and model."
    },
    {
      "asset_id": "asset_07",
      "filename": "image7.png",
      "type": "Identity-Bearing",
      "prompt_reference_id": "reference_asset_03",
      "attach_to_api_call": true,
      "strictness": "Near Exact — face, hair, and build only",
      "note": "Primary identity source — male model mid-plank exercise pose. Extract only the person — discard the pose, stability ball, and indoor background entirely."
    },
    {
      "asset_id": "asset_08",
      "filename": "image (1).png",
      "type": "Identity-Bearing",
      "prompt_reference_id": "reference_asset_04",
      "attach_to_api_call": true,
      "strictness": "Near Exact — face and hair only",
      "note": "Secondary identity angle — same model as image7.png, standing by a window. Extract only the person's face and hair — discard the standing pose, window background, dark tank top, CLEVER logo, on-image ad text, and notification UI graphic baked into this frame entirely."
    }
  ]
}
```

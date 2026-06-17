```json
{
  "SceneContract": {
    "Metadata": {
      "brand": "CLEVER Protein",
      "campaign": "日本製輕盈美學 — HK OL afternoon tea trial acquisition",
      "framework": "Scene Assembly v5.2.5",
      "stage": "5 — Scene Construction",
      "variant": "Trial_04_pantry — office pantry/kitchenette, active preparation ritual, on-image ad typography",
      "reference_images_provided": 2,
      "reference_images_used": ["image1.png (reference_asset_01)", "image4.png (reference_asset_02)"],
      "client_preference_contract_present": false,
      "generation_mode": "Partial Generation — brand assets (pack, shaker, logo) reproduced from references; human subject, pantry environment, and typography overlay fully generated"
    },

    "RealityModel": {
      "type": "Realistic",
      "coherence_rules": {
        "scale": "realistic",
        "perspective": "realistic",
        "anchoring": "required",
        "environmental_behavior": "realistic"
      },
      "rationale": "Art Direction requires an everyday, believable lifestyle advertisement set in a recognizable HK office pantry — commercial realism with a photoshoot-set quality clean counter and integrated ad typography."
    },

    "Entities": [
      {
        "id": "entity_01",
        "description": "Hong Kong office lady, naturally healthy and attractive, approximately 25–32 years old, East Asian, in light polished-casual office wear (business casual blouse with clean skirt or slacks — not athletic or gym wear). Standing at the clean pantry counter, actively shaking the transparent shaker or holding it ready to drink. Calm, purposeful, quietly confident — this is her deliberate ritual, not a rushed moment. Fully generated persona.",
        "roles": ["Identity-Bearing"],
        "source": "Generated"
      },
      {
        "id": "entity_02",
        "description": "CLEVER CLEAR PROTEIN lemon-flavor pouch: white body, large dark-blue 'CLEAR PROTEIN' typography, bright yellow lemon flavor band at top with lemon imagery, functional badges (0脂·0膽固醇·O奶味·低糖 / 100%WPI). Resting on clean pantry counter surface facing camera.",
        "roles": ["Brand-Bearing", "Product"],
        "source": "Reference Asset",
        "asset_id": "asset_01",
        "prompt_reference_id": "reference_asset_01"
      },
      {
        "id": "entity_03",
        "description": "Transparent shaker bottle with pale-yellow, clear (non-milky) protein drink inside, lemon slice visible. CLEVER logo on the bottle body. Held by entity_01 in an active shaking gesture or held ready to drink, or set on counter beside her.",
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
        "description": "Clean, near-empty pantry counter surface — light-colored (white, light wood tone, or light stone). Only the pack and shaker visible on the surface. No clutter, no snack wrappers, no cups, no food, no stationery. The counter reads as curated and purposefully clear — a photoshoot-set quality surface within the office pantry.",
        "roles": ["Environmental"],
        "source": "Generated"
      },
      {
        "id": "entity_06",
        "description": "Office pantry background — a soft-focused water dispenser or hot/cold water machine (partially visible, clearly out of focus) and clean light-colored walls (white, off-white, or very light sky-blue tiles or paint). A small window with natural light is optional. No visible snack shelves, no microwave in frame, no clutter. The background reads as 'clean, modern HK office pantry' through one or two minimal specific cues (the water dispenser silhouette, the wall color) rather than through clutter or detailed prop density.",
        "roles": ["Environmental"],
        "source": "Generated"
      },
      {
        "id": "entity_07",
        "description": "On-image advertisement typography overlay — a visual design element integrated into the background plane. Headline: '告別3點3罪惡感！' in large, bold, clean modern sans-serif. Subtitle below: '日本製 · 清蛋白' in smaller text. Positioned in the upper portion of the frame, within the background space above and behind the OL, not overlapping the OL's face or the product hero cluster. Typography must read as a designed ad headline, not a random watermark or caption. White text or dark-blue text to maximize legibility against the pantry background — whichever achieves highest contrast.",
        "roles": ["Typography-Overlay", "Campaign-Mandatory"],
        "source": "Generated",
        "preservation_priority": "Critical"
      }
    ],

    "Relationships": [
      { "subject": "entity_01", "relation": "standing_at", "object": "entity_05" },
      { "subject": "entity_03", "relation": "held_by_or_adjacent_to", "object": "entity_01" },
      { "subject": "entity_02", "relation": "resting_on", "object": "entity_05" },
      { "subject": "entity_02", "relation": "adjacent_to", "object": "entity_03" },
      { "subject": "entity_04", "relation": "appears_on", "object": "entity_02" },
      { "subject": "entity_04", "relation": "appears_on", "object": "entity_03" },
      { "subject": "entity_01", "relation": "positioned_in_front_of", "object": "entity_06" },
      { "subject": "entity_07", "relation": "overlaid_on", "object": "entity_06" }
    ],

    "AnchorRelationships": [
      { "entity_id": "entity_01", "anchor_type": "counter_standing_anchored" },
      { "entity_id": "entity_02", "anchor_type": "counter_surface_anchored" },
      { "entity_id": "entity_03", "anchor_type": "hand_held_or_counter_anchored" },
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
      { "entity_id": "entity_03", "reference_entity": "entity_01", "scale_relationship": "Hand-sized shaker, normal beverage bottle scale relative to the OL's hand." },
      { "entity_id": "entity_02", "reference_entity": "entity_03", "scale_relationship": "Protein pouch slightly taller than the shaker; both near the camera in the foreground on the counter." },
      { "entity_id": "entity_05", "reference_entity": "entity_01", "scale_relationship": "Counter surface at standing-height — only the clean top surface is visible in frame; entity_01 stands behind it." },
      { "entity_id": "entity_06", "reference_entity": "entity_01", "scale_relationship": "Background wall and water dispenser behind the OL — dispenser visible as a soft-focused form in the lower-mid background; wall fills the upper background zone where typography sits." },
      { "entity_id": "entity_07", "reference_entity": "entity_06", "scale_relationship": "Typography occupies the upper portion of the background zone — headline large enough to be legible on a mobile screen; subtitle approximately half the headline size." }
    ],

    "GenerationRequirements": {
      "required_entities": ["entity_01", "entity_02", "entity_03", "entity_04", "entity_05", "entity_06", "entity_07"],
      "required_supporting_objects": [
        "A soft-focused water dispenser or hot/cold water machine in the background — the single pantry-identifying prop, out of focus"
      ],
      "required_environment_elements": [
        "Clean, near-empty pantry counter surface — photoshoot-set quality, no visible clutter",
        "Light-colored walls or tiles (white, off-white, or very light sky-blue) in the background",
        "Bright high-key daylight quality or soft LED pantry lighting consistent with an afternoon break"
      ],
      "required_visual_overlays": [
        "On-image advertisement typography: bold modern sans-serif headline '告別3點3罪惡感！' in the upper background zone; subtitle '日本製 · 清蛋白' smaller below it. Positioned in the background plane above and clear of the OL and product cluster. Typography is a campaign-mandatory visual element — it must be present and legible."
      ],
      "explicitly_excluded_objects": [
        "No snack shelves or visible snack packaging in the background",
        "No microwave in frame",
        "No messy sink or dish rack",
        "No office desk or chair in frame",
        "No stationery, papers, or work materials",
        "No plants or greenery",
        "No other people in the pantry",
        "No windows behind the subject that create bright spots behind her head",
        "No floor-to-ceiling gym windows (image1.png background must NOT carry through — only product from that image)",
        "No text or typography beyond the specified on-image ad copy ('告別3點3罪惡感！' + '日本製 · 清蛋白')"
      ],
      "reference_locked_entities": [
        {
          "entity_id": "entity_02",
          "asset_id": "asset_01",
          "prompt_reference_id": "reference_asset_01",
          "rule": "Reproduce CLEVER lemon CLEAR PROTEIN pouch from image1.png. Product packaging only — ignore male model and gym background entirely."
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
          "rule": "Reproduce CLEVER logo/wordmark from image4.png. Use image4's minimal sky-blue and clean aesthetic as the target visual register. Exclude timing-clock graphic and specific model."
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
          "Light, polished-casual office wear (business casual blouse + clean skirt or slacks — not athletic wear)",
          "Standing posture at the counter — active and upright, not seated",
          "Calm, purposeful, quietly confident expression and body language — this is intentional, not rushed"
        ],
        "flexible_attributes": [
          "Exact facial identity (fully generated persona)",
          "Specific hairstyle and outfit details within business casual register",
          "Exact pose — actively shaking the bottle, holding it ready, or about to take the first sip"
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
        "flexible_attributes": ["Scale relative to scene", "Viewing angle and rotation", "Counter placement", "Lighting on pack surface"],
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
        "flexible_attributes": ["Fill level", "Exact rotation and angle", "Held in active shaking motion vs. held ready to drink vs. resting on counter"],
        "generation_rule": "Reproduce from reference_asset_01 — clear liquid mandatory"
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
          "Near-empty counter surface — only the pack and shaker visible; nothing else on the surface",
          "Light color (white, light wood, or light stone) — no dark countertops",
          "Clean, photoshoot-set quality — no visible clutter of any kind"
        ],
        "flexible_attributes": ["Exact counter material", "Counter edge visible or not", "Subtle counter surface texture"]
      },
      {
        "entity_id": "entity_06",
        "preservation_priority": "Critical",
        "recognizability_requirement": "Approximate Match",
        "source": "Generated",
        "immutable_attributes": [
          "Clean, uncluttered background — no snack shelves, microwave, mess, or other people visible",
          "Light-colored walls (white, off-white, or very light sky-blue)",
          "Water dispenser or similar pantry fixture is present but soft-focused in background",
          "No bright light sources directly behind the subject's head"
        ],
        "flexible_attributes": ["Exact background color", "Whether a small window is present", "Degree of DoF softening on dispenser"]
      },
      {
        "entity_id": "entity_07",
        "preservation_priority": "Critical",
        "recognizability_requirement": "Near Exact",
        "source": "Generated",
        "immutable_attributes": [
          "Headline text content: '告別3點3罪惡感！' — exact characters, no substitution",
          "Subtitle text content: '日本製 · 清蛋白' — exact characters",
          "Positioned in upper background zone, not overlapping OL or product cluster",
          "Legible at mobile screen size"
        ],
        "flexible_attributes": [
          "Exact font weight and style (bold modern sans-serif preferred)",
          "Text color — white or dark-blue, whichever reads best against the specific pantry background",
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
      "note": "Source of lemon CLEAR PROTEIN pouch and transparent shaker. Use product + bottle only; discard male model and gym floor/window background entirely."
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

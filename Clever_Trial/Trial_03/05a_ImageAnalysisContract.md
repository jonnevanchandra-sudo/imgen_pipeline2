```json
{
  "ImageAnalysisContract": {
    "Metadata": {
      "brand": "CLEVER Protein",
      "campaign": "日本製輕盈美學 — HK OL afternoon tea trial acquisition",
      "framework": "Image Analysis Framework v1.0",
      "stage": "5.0 — Asset Extraction",
      "reference_images_provided": 4,
      "generation_mode": "Partial Generation (reference-guided for brand assets; human identity fully generated)"
    },

    "AssetInventory": [
      {
        "asset_id": "asset_01",
        "filename": "image1.png",
        "classification": ["Brand-Bearing", "Product / Equipment Asset", "Style Reference Asset"],
        "entity_assignment": "entity_product_lemon",
        "client_intent": "Brand asset reference: preserve CLEVER lemon CLEAR PROTEIN pouch, transparent shaker with clear pale-yellow drink and lemon cue, and CLEVER logo mark. Male model and gym environment are style inspiration only — do not preserve or replicate."
      },
      {
        "asset_id": "asset_02",
        "filename": "image2.png",
        "classification": ["Style Reference Asset"],
        "entity_assignment": null,
        "client_intent": "Style inspiration only. Grape flavor + outdoor running motif — excluded from new campaign. Use as reference for blue-sky color energy and dual-subject dynamic lifestyle; do not lock any element."
      },
      {
        "asset_id": "asset_03",
        "filename": "image3.png",
        "classification": ["Style Reference Asset"],
        "entity_assignment": null,
        "client_intent": "Style inspiration only. Multi-flavor product lineup, spring promotion pricing, and cherry blossom motif are excluded. Female model and minimal sky-blue background register as aesthetic direction; do not lock human identity or pricing copy."
      },
      {
        "asset_id": "asset_04",
        "filename": "image4.png",
        "classification": ["Brand-Bearing", "Product / Equipment Asset", "Style Reference Asset"],
        "entity_assignment": "entity_logo",
        "client_intent": "Brand asset reference: preserve CLEVER logo/wordmark and the clean minimal sky-blue layout language. Preserve lemon pack and shaker (same product as asset_01). Timing-clock graphic, specific female model identity, and 'Timing' copy are not preserved — style reference only."
      }
    ],

    "VisualObservations": {
      "image1_observed": [
        "CLEVER logo: stylized 'C' mark followed by 'CLEVER' wordmark in cyan-teal on white. Logo positioned top-left.",
        "Large '清蛋白' Chinese headline in white, sky-blue background.",
        "CLEVER CLEAR PROTEIN lemon pouch: white body, large dark-blue 'CLEAR PROTEIN' typography across middle, bright yellow lemon-flavor band at top with lemon imagery, 'Level Up 運動成效' badge, '0脂·0膽固醇·O奶味·低糖' claims, '100%WPI' callout.",
        "Transparent shaker bottle: clear body, CLEVER logo on side, pale-yellow clear liquid inside, lemon slice visible, rounded cap.",
        "Lemon slices as loose fruit prop beside shaker.",
        "'一搖一清 0負擔' text on image.",
        "'美味しい！創新清蛋白粉' in yellow cursive Japanese.",
        "Male model — plank on exercise ball, gym setting with floor-to-ceiling windows — style reference only.",
        "Overall palette: light sky-blue + white + yellow accent."
      ],
      "image2_observed": [
        "Grape flavor pouch: same white-body/CLEAR PROTEIN architecture, purple flavor band and grape imagery.",
        "Two runners (male + female) — outdoor, blue sky background — style reference only.",
        "Lower purple color panel with white headline typography.",
        "Same CLEVER logo system."
      ],
      "image3_observed": [
        "Female model: white mesh crop top, light yellow sports bra and leggings — style reference only.",
        "Three CLEAR PROTEIN pouches: lemon (blue accent), peach/pink, grape (purple) — multi-flavor lineup, inspiration only.",
        "Spring promotion banner (春日優惠) with cherry blossom illustration — not preserved.",
        "'日本製造' badge top-right.",
        "Clean flat sky-blue background — key aesthetic reference.",
        "Transparent shaker: same as image1 style, pale-yellow clear drink."
      ],
      "image4_observed": [
        "Cleanest, most minimal layout of the four: near-empty sky-blue background.",
        "CLEVER CLEAR PROTEIN lemon pouch (same as image1) as hero, larger scale.",
        "'補充蛋白時機 Timing' text with clock arc graphic — not preserved in new campaign.",
        "Same female model as image3 drinking from clear shaker — identity reference only.",
        "Strong visual breathing room / whitespace — key aesthetic cue for Trial_03.",
        "CLEVER logo top-right in black."
      ]
    },

    "PreservationContracts": [
      {
        "asset_id": "asset_01",
        "entity_id": "entity_product_lemon",
        "classification": "Brand-Bearing + Product / Equipment",
        "preservation_priority": "Critical",
        "recognizability_requirement": "Near Exact",

        "immutable_attributes": [
          {
            "attribute": "CLEAR PROTEIN lemon pouch — white body, large dark-blue 'CLEAR PROTEIN' typography across middle, bright yellow lemon-flavor accent band at top, functional claim badges (0脂·0膽固醇·O奶味·低糖 / 100%WPI / Level Up)",
            "confidence": null,
            "notes": "Core pack identity; generate must reproduce this architecture exactly"
          },
          {
            "attribute": "Transparent shaker bottle — clear/translucent body, CLEVER logo on side, pale-yellow clear drink visible inside, lemon slice cue",
            "confidence": null,
            "notes": "Primary refreshment cue; drink must read clear and translucent, never opaque or milky"
          },
          {
            "attribute": "Sky-blue and white brand color system",
            "confidence": 0.95,
            "notes": "Dominant across all four reference images"
          }
        ],

        "flexible_attributes": [
          { "attribute": "Male model identity, face, pose, and gym environment", "reason": "Style inspiration only; fully replaced by generated HK OL persona and clean desk setting." },
          { "attribute": "Exact scale, rotation, and placement of pack and shaker in scene", "reason": "Adapts to new composition." },
          { "attribute": "Lemon slices as loose prop", "reason": "May include as subtle refreshment cue but not mandatory at exact image1 position." }
        ],

        "generation_instruction": "Reproduce the CLEVER lemon CLEAR PROTEIN pouch and the transparent shaker with clear pale-yellow lemon drink from image1.png. Ignore the male model, gym environment, and all background context from that image. Product and shaker only."
      },

      {
        "asset_id": "asset_04",
        "entity_id": "entity_logo",
        "classification": "Brand-Bearing",
        "preservation_priority": "High",
        "recognizability_requirement": "Exact Match",

        "immutable_attributes": [
          {
            "attribute": "CLEVER wordmark: stylized 'C' mark + 'CLEVER' text — letterforms, color (cyan-teal or black depending on background), and proportional format",
            "confidence": null,
            "notes": "Logo must not be redrawn from training data"
          },
          {
            "attribute": "Made in Japan / 日本製 cue legible somewhere in the image",
            "confidence": 0.95,
            "notes": "Mandatory branding requirement from brief"
          },
          {
            "attribute": "Clean, minimal, near-empty sky-blue background aesthetic of image4 as the target visual register",
            "confidence": 0.9,
            "notes": "image4 is the clearest single reference for the desired minimalist photoshoot-set look"
          }
        ],

        "flexible_attributes": [
          { "attribute": "Timing-clock graphic and 'Timing' copy", "reason": "Excluded — off-concept for office afternoon tea campaign." },
          { "attribute": "Specific female model identity and pose from image4", "reason": "Style reference only; generated HK OL persona used instead." },
          { "attribute": "Logo scale and exact placement", "reason": "Adapts to new layout." }
        ],

        "generation_instruction": "Reproduce the CLEVER logo/wordmark exactly from image4.png. Use image4's clean minimal sky-blue background aesthetic as the visual register target. Ignore the timing-clock graphic and the specific model."
      }
    ],

    "StyleInspirationNotes": {
      "from_image2": "Sky-blue upper + strong color-panel lower layout; energetic lifestyle feel. Not reproduced structurally — used to confirm sky-blue + flavor-accent as dominant color language.",
      "from_image3": "Female subject holding shaker with confident, natural expression; spring-season cleanliness. Confirms the target 'healthy, natural, confident young East Asian woman' persona and the minimal sky-blue background register."
    },

    "SceneAssemblyHandoff": {
      "entity_source_map": [
        {
          "entity_id": "entity_product_lemon",
          "source": "Reference Asset",
          "asset_id": "asset_01",
          "prompt_reference_id": "reference_asset_01",
          "generation_mode": "Reproduce pack + shaker from image1.png; human and gym excluded"
        },
        {
          "entity_id": "entity_logo",
          "source": "Reference Asset",
          "asset_id": "asset_04",
          "prompt_reference_id": "reference_asset_02",
          "generation_mode": "Reproduce CLEVER logo from image4.png; timing graphic and model excluded"
        },
        {
          "entity_id": "entity_ol_subject",
          "source": "Generated",
          "asset_id": null,
          "generation_mode": "Generate from campaign context: HK OL persona, 25–32, healthy natural-looking, light office wear, calm and quietly confident"
        },
        {
          "entity_id": "entity_environment",
          "source": "Generated",
          "asset_id": null,
          "generation_mode": "Generate: clean, minimal, near-empty photoshoot-set quality office backdrop — sky-blue and white register from image4"
        }
      ]
    }
  }
}
```

```json
{
  "ImageAnalysisContract": {
    "Metadata": {
      "brand": "CLEVER Protein",
      "campaign": "Clever Protein clear whey HK OL afternoon tea trial acquisition",
      "framework": "Image Analysis Framework v1.0",
      "stage": "5.0 — Asset Extraction",
      "reference_images_provided": 4,
      "generation_mode": "Partial Generation (reference-guided)"
    },

    "AssetInventory": [
      {
        "asset_id": "asset_01",
        "filename": "reference_01.jpg",
        "classification": ["Identity-Bearing", "Product / Equipment Asset", "Brand-Bearing", "Environmental Asset", "Style Reference Asset"],
        "entity_assignment": "entity_01",
        "client_intent": "Default assumption: preserve model identity loosely, product packaging and brand marks strictly; use environment and overall style as reference."
      },
      {
        "asset_id": "asset_02",
        "filename": "reference_02.jpg",
        "classification": ["Identity-Bearing", "Product / Equipment Asset", "Brand-Bearing", "Environmental Asset", "Style Reference Asset"],
        "entity_assignment": "entity_02",
        "client_intent": "Default assumption: preserve runner pair identity loosely, product packaging and brand marks strictly; use environment/composition/style as reference."
      },
      {
        "asset_id": "asset_03",
        "filename": "reference_03.jpg",
        "classification": ["Identity-Bearing", "Product / Equipment Asset", "Brand-Bearing", "Style Reference Asset"],
        "entity_assignment": "entity_03",
        "client_intent": "Default assumption: preserve female model identity loosely, product packaging and brand system strictly; use layout and style as reference."
      },
      {
        "asset_id": "asset_04",
        "filename": "reference_04.jpg",
        "classification": ["Identity-Bearing", "Product / Equipment Asset", "Brand-Bearing", "Style Reference Asset"],
        "entity_assignment": "entity_03",
        "client_intent": "Default assumption: same female model as asset_03; preserve loosely, lock product/brand; treat sky-blue style and composition as reference."
      }
    ],

    "PreservationContracts": [
      {
        "asset_id": "asset_01",
        "entity_id": "entity_01",
        "classification": "Identity-Bearing + Product / Equipment + Brand-Bearing + Environmental",
        "preservation_priority": "Critical",
        "recognizability_requirement": "Close Match",

        "observations": [
          "Indoor gym-like environment with large floor-to-ceiling windows and visible greenery outside.",
          "Male-presenting subject performing plank with hands on a grey exercise ball.",
          "Subject appears as a fit, muscular young adult with short dark hair styled to the side.",
          "Wearing a sleeveless white athletic top with dark shoulder/side panels and light-colored athletic pants.",
          "Dominant image colors: light sky blue, white, and soft grey.",
          "Packshot of CLEVER clear protein lemon flavor in lower right: white pouch with large blue 'CLEAR PROTEIN' typography and yellow lemon accent strip and badges.",
          "Two transparent shaker bottles with lemon slices and pale yellow drink, each with CLEVER logo mark.",
          "Brand logo and large Chinese characters for product category across top on sky-blue banner.",
          "On-image text band in middle with white typography on blue background; key '0' highlighted in yellow with lemon ring detail."
        ],

        "immutable_attributes": [
          {
            "attribute": "CLEVER logo mark shape and orientation on pack and shaker",
            "confidence": null,
            "notes": "direct brand asset observation"
          },
          {
            "attribute": "White pouch packaging architecture with large blue 'CLEAR PROTEIN' typography and lemon-flavor yellow accent strip",
            "confidence": null,
            "notes": "core packshot identity"
          },
          {
            "attribute": "Transparent shaker with visible pale yellow drink and lemon slices",
            "confidence": null,
            "notes": "refreshing clear beverage cue"
          },
          {
            "attribute": "Overall light sky-blue and white color palette in background and typography",
            "confidence": 0.9,
            "notes": "dominant brand visual system"
          }
        ],

        "flexible_attributes": [
          {
            "attribute": "Exact face and identity of the male model",
            "reason": "Default assumption is style/lifestyle reference rather than mandatory talent reuse."
          },
          {
            "attribute": "Specific gym environment layout and window geometry",
            "reason": "Space can vary as long as it feels like a bright indoor training environment."
          },
          {
            "attribute": "Exact Chinese/Japanese copy content and layout positions",
            "reason": "Copy will change for new campaign while maintaining brand typography style."
          },
          {
            "attribute": "Exact pose with exercise ball",
            "reason": "Any athletic contextual activity may be acceptable."
          }
        ],

        "uncertainties": [
          {
            "attribute": "Whether this specific male talent must reappear in new creatives",
            "confidence": 0.55,
            "recommended_action": "Clarify if talent identity is required or if a similar athletic male is sufficient."
          },
          {
            "attribute": "Exact lemon flavor variant details and badges on pack (small text)",
            "confidence": 0.7,
            "recommended_action": "If regulatory or claim-level accuracy is critical, provide vector/pack files instead of relying on this raster reference."
          }
        ],

        "generation_instruction": "Preserve CLEVER lemon-flavor pack architecture, logo, shaker-with-lemon clear drink, and light blue/white refreshment aesthetic. Treat male athlete, pose, and exact gym as flexible lifestyle references unless client elevates them to locked status."
      },

      {
        "asset_id": "asset_02",
        "entity_id": "entity_02",
        "classification": "Identity-Bearing + Product / Equipment + Brand-Bearing + Environmental",
        "preservation_priority": "Critical",
        "recognizability_requirement": "Close Match",

        "observations": [
          "Outdoor running scene under bright sky with two subjects: front female runner and rear male runner.",
          "Both subjects appear young, fit, and athletic.",
          "Female runner wears a black sports bra and dark running shorts with colored accents; ponytail hairstyle.",
          "Male runner wears athletic top and shorts, running behind her.",
          "Dominant upper background is blue sky; lower background shows light-colored running surface.",
          "Lower half of creative is purple panel with white headline text and yellow handwritten-style subtext.",
          "Packshot of CLEVER clear protein grape flavor: white pouch with large blue 'CLEAR PROTEIN' typography, purple flavor band, grapes image, and purple shaker with purple drink and grape pieces.",
          "Grapes cluster and transparent shaker with purple liquid placed alongside packshot.",
          "Brand logo and product name at top left on sky-blue banner; headline copy at top right in purple."
        ],

        "immutable_attributes": [
          {
            "attribute": "CLEVER clear protein grape-flavor pouch: white base, blue 'CLEAR PROTEIN' text, purple flavor strip and grape imagery",
            "confidence": null,
            "notes": "core product identity for grape variant"
          },
          {
            "attribute": "Transparent shaker containing purple clear drink with grape pieces, plus loose grape fruit imagery",
            "confidence": null,
            "notes": "flavor and refreshment cue"
          },
          {
            "attribute": "Use of sky-blue and grape-purple as main background and lower-panel colors",
            "confidence": 0.9,
            "notes": "flavor-linked color system"
          }
        ],

        "flexible_attributes": [
          {
            "attribute": "Exact facial identity and body proportions of the two runners",
            "reason": "Assumed to be lifestyle reference; runners can be recast while keeping demographic and fitness cues."
          },
          {
            "attribute": "Exact running pose, spacing, and camera angle",
            "reason": "Any dynamic outdoor movement that suggests running/endurance is acceptable."
          },
          {
            "attribute": "Specific purple panel layout and headline wording",
            "reason": "Hierarchy can be adapted to new message while preserving general brand structure."
          }
        ],

        "uncertainties": [
          {
            "attribute": "Requirement to show both male and female subjects together vs. single subject for new campaign",
            "confidence": 0.6,
            "recommended_action": "Confirm if dual-gender running motif is strategic or incidental."
          }
        ],

        "generation_instruction": "Preserve grape flavor packshot, shaker with purple clear drink and grape fruit, and blue–purple refreshment palette. Treat runners’ identities, apparel colors, and exact environment as flexible; maintain an energetic outdoor running feel if aligned with new brief."
      },

      {
        "asset_id": "asset_03",
        "entity_id": "entity_03",
        "classification": "Identity-Bearing + Product / Equipment + Brand-Bearing + Style Reference",
        "preservation_priority": "High",
        "recognizability_requirement": "Close Match for product; Reference Only for human identity",

        "observations": [
          "Large, mostly flat sky-blue background with promotional text and pricing in white and pink.",
          "Rectangle banner with pink background and white Chinese/Japanese text indicating a spring promotion, decorated with small cherry blossom illustrations.",
          "Black CLEVER logo at top left; small '日本製造' label at top right.",
          "Hero text block in white and pink emphasizing 'WPI Clear' and price in large numerals.",
          "Row of three CLEVER clear protein pouches (different flavors) at bottom left, each white with blue/pink/purple accent strips.",
          "Female-presenting subject on right, drinking pale yellow clear beverage from a transparent shaker with CLEVER logo.",
          "Subject wears a white mesh short-sleeve crop top over light yellow sports bra and matching yellow bottoms.",
          "Background and overall style are bright, flat, minimal, and high-key."
        ],

        "immutable_attributes": [
          {
            "attribute": "White pouch packaging family with large 'CLEAR PROTEIN' typography and flavor-colored top bands (blue, pink, purple)",
            "confidence": null,
            "notes": "represents product line system"
          },
          {
            "attribute": "Transparent shaker with pale yellow drink and CLEVER logo",
            "confidence": null,
            "notes": "key refreshment and brand asset"
          },
          {
            "attribute": "Use of light sky-blue as primary background color with clean, minimal environment",
            "confidence": 0.9,
            "notes": "brand visual backdrop"
          },
          {
            "attribute": "Cherry blossom and spring-sale banner visual motif as example of seasonal-Japanese cue",
            "confidence": 0.85,
            "notes": "supports 'Made in Japan' and seasonal feeling; may inspire but not strictly required"
          }
        ],

        "flexible_attributes": [
          {
            "attribute": "Exact face and identity of the female model",
            "reason": "Assumed lifestyle reference; any similar young East Asian female can substitute."
          },
          {
            "attribute": "Exact promotional price and discount copy",
            "reason": "Campaign-dependent and likely to change."
          },
          {
            "attribute": "Exact cherry blossom artwork and banner dimensions",
            "reason": "Seasonal styling; can be reinterpreted."
          },
          {
            "attribute": "Mesh crop top design and exact yellow outfit tone",
            "reason": "Wardrobe can change as long as it remains light, sporty, and clean."
          }
        ],

        "uncertainties": [
          {
            "attribute": "Whether all three flavor packs must be shown together vs. a single hero flavor for new creative",
            "confidence": 0.65,
            "recommended_action": "Clarify if multi-flavor lineup display is a mandatory pattern."
          }
        ],

        "generation_instruction": "Lock the CLEVER pack architecture and transparent shaker with clear drink as primary product assets; maintain light sky-blue minimal background and soft Japanese seasonal cues as style. Treat the specific female model, her outfit, and price/banner details as adaptable."
      },

      {
        "asset_id": "asset_04",
        "entity_id": "entity_03",
        "classification": "Identity-Bearing + Product / Equipment + Brand-Bearing + Style Reference",
        "preservation_priority": "High",
        "recognizability_requirement": "Close Match for product; Reference Only for human identity",

        "observations": [
          "Light sky-blue background with large CLEVER logo in black at top right.",
          "Hero packshot of lemon flavor CLEVER CLEAR PROTEIN pouch at top left, consistent with asset_01 lemon variant.",
          "Yellow typographic treatment 'Timing' with a clock arc graphic near packshot, plus Chinese text about protein timing.",
          "Large vertical dividing line and bottom-left text area in deeper blue indicating exercise phases (before/during/after).",
          "Female-presenting subject at lower right, drinking pale yellow clear beverage from transparent shaker with CLEVER logo.",
          "Subject appears to be same as in asset_03: similar hairstyle, outfit (white mesh crop top, light yellow sports bra and leggings), and pose facing upward.",
          "Overall composition is cleaner and more minimal than asset_03, with strong emphasis on packshot + model + headline timing concept."
        ],

        "immutable_attributes": [
          {
            "attribute": "CLEVER lemon flavor CLEAR PROTEIN pouch design (white pack, blue 'CLEAR PROTEIN', yellow flavor band and badges)",
            "confidence": null,
            "notes": "core product representation"
          },
          {
            "attribute": "Transparent shaker with pale yellow drink and CLEVER logo",
            "confidence": null,
            "notes": "reinforces clear beverage and brand"
          },
          {
            "attribute": "Sky-blue minimal background with strong cleanliness and whitespace",
            "confidence": 0.9,
            "notes": "key brand atmosphere"
          }
        ],

        "flexible_attributes": [
          {
            "attribute": "Specific 'timing' clock graphic and exact text phrasing",
            "reason": "Conceptual element demonstrating educational angle; can be redesigned for other messages."
          },
          {
            "attribute": "Exact identity and pose of female model",
            "reason": "Assumed to be lifestyle reference; body orientation and gaze direction may change while preserving healthy, confident feel."
          },
          {
            "attribute": "Vertical divider and layout segmentation proportions",
            "reason": "Composition can be adjusted for new content while keeping clear hierarchy."
          }
        ],

        "uncertainties": [
          {
            "attribute": "Whether the same female model from asset_03 must be reused consistently across creatives",
            "confidence": 0.7,
            "recommended_action": "Confirm if she is a recurring brand ambassador or simply a campaign model."
          }
        ],

        "generation_instruction": "Preserve lemon flavor packshot, clear yellow drink in branded shaker, and clean sky-blue minimal background. Treat timing graphics, layout details, and the specific female model as flexible guidance for educational but light-feeling compositions."
      }
    ],

    "SceneAssemblyHandoff": {
      "entity_source_map": [
        {
          "entity_id": "entity_01",
          "source": "Reference Asset",
          "asset_id": "asset_01",
          "generation_mode": "Preserve — product and brand elements; human identity flexible"
        },
        {
          "entity_id": "entity_02",
          "source": "Reference Asset",
          "asset_id": "asset_02",
          "generation_mode": "Preserve — product and brand elements; human identities flexible"
        },
        {
          "entity_id": "entity_03",
          "source": "Reference Asset",
          "asset_id": "asset_03 / asset_04",
          "generation_mode": "Preserve — pack system and shaker; human identity flexible"
        },
        {
          "entity_id": "entity_04",
          "source": "Generated",
          "asset_id": null,
          "generation_mode": "Generate from campaign context (e.g., new HK OL office scenario)"
        }
      ],
      "partial_generation_note": "All CLEVER clear protein packshots, transparent beverage shakers, logo marks, and light sky-blue clean aesthetic must align with these PreservationContracts. Human subjects, precise poses, copy, and seasonal graphics are style references unless client upgrades them to immutable."
    },

    "ClientConfirmationRequired": [
      {
        "asset_id": "asset_01",
        "attribute": "Male athlete talent identity",
        "question": "Should the exact male model from the gym scene be reused and recognizably matched, or is a similar athletic male sufficient?",
        "blocking": false
      },
      {
        "asset_id": "asset_02",
        "attribute": "Dual-gender running pair",
        "question": "Is it important to feature both a male and female runner together, or can the new creative focus on a single subject while keeping an endurance-running context?",
        "blocking": false
      },
      {
        "asset_id": "asset_03",
        "attribute": "Multi-flavor product lineup",
        "question": "Do you need all three flavor variants visible in new assets, or can we hero a single flavor that best matches the HK OL afternoon-tea concept?",
        "blocking": false
      },
      {
        "asset_id": "asset_03",
        "attribute": "Female model as recurring face",
        "question": "Is the female model in assets_03 and _04 a designated brand ambassador whose likeness must be preserved, or can we depict a similar HK OL target persona instead?",
        "blocking": false
      },
      {
        "asset_id": "asset_04",
        "attribute": "Protein timing visual motif",
        "question": "Should the clock/timing concept be preserved explicitly in new creatives, or is it only an example of educational messaging layout?",
        "blocking": false
      }
    ]
  }
}
```
```json
{
  "ImageAnalysisContract": {
    "Metadata": {
      "brand": "CLEVER Protein",
      "campaign": "日本製輕盈美學 — office variant, model face reference",
      "framework": "Image Analysis v5.0",
      "stage": "5a — Pre-Scene Assembly Asset Extraction",
      "variant": "Trial_05_office — female model face from image 5.png, office desk setting",
      "source_image": "image 5.png",
      "analysis_date": "2026-06-16"
    },

    "ClientIntentDeclaration": {
      "image_ref": "image 5.png",
      "purpose": "Lock the female model's face, hair, and overall look as the protagonist (entity_01) for the office desk scene. The model appears in workout wear in this image — in the generated scene she will be dressed in polished-casual office wear instead.",
      "what_to_lock": ["Face and facial features", "Hair style — neat bun/updo", "Overall build type (lean, naturally healthy)", "Skin tone and complexion register"],
      "lock_strictness": "Near-Exact for face and hair. Approximate for build.",
      "what_to_exclude": [
        "The sports bra and workout clothing — the model will be in polished-casual office wear in the generated scene",
        "The shaker/bottle in the image — product comes from reference_asset_01 (image1.png)",
        "The drink/liquid in the image",
        "The outdoor mountain/sky background — environment is a clean office desk setting"
      ]
    },

    "AssetClassification": {
      "type": "Identity-Bearing",
      "sub_type": "Human Subject — Female Model Face Reference",
      "confidence": 1.0
    },

    "ObservationLog": [
      {
        "attribute": "Ethnicity and age",
        "status": "Observable",
        "value": "East Asian female, estimated 21–26 years old",
        "confidence": 0.95
      },
      {
        "attribute": "Hair",
        "status": "Observable",
        "value": "Hair gathered into a neat, clean bun or updo. Smooth, put-together styling — not messy or casual. This hairstyle translates naturally to an office-ready look.",
        "confidence": 0.95
      },
      {
        "attribute": "Build",
        "status": "Observable",
        "value": "Lean, naturally healthy — not muscular. Slim shoulders and neck visible. Fits the 'light beauty' aesthetic of the campaign.",
        "confidence": 0.90
      },
      {
        "attribute": "Skin and complexion",
        "status": "Observable",
        "value": "Bright, naturally clear complexion. Warm light skin tone. Natural makeup or minimal makeup appearance. Not heavily retouched — natural pore texture visible.",
        "confidence": 0.90
      },
      {
        "attribute": "Expression",
        "status": "Observable",
        "value": "Subtle upward gaze or looking slightly off-camera. Calm, lightly pleased expression — not smiling broadly, not posed stiffly. Natural and relaxed.",
        "confidence": 0.85
      },
      {
        "attribute": "Clothing in image",
        "status": "Observable — EXCLUDED",
        "value": "Light blue strappy sports bra / workout top. Excluded — in the generated scene she wears polished-casual office wear (blouse or clean top appropriate for HK office environment).",
        "confidence": 1.0
      },
      {
        "attribute": "Shaker/bottle in image",
        "status": "Observable — EXCLUDED",
        "value": "Purple/pink shaker bottle. NOT CLEVER branded. Excluded — product reference comes from image1.png.",
        "confidence": 1.0
      },
      {
        "attribute": "Background in image",
        "status": "Observable — EXCLUDED",
        "value": "Outdoor setting with mountains, sky, and open-air light. Excluded — office desk environment is fully generated.",
        "confidence": 1.0
      }
    ],

    "PreservationContract": {
      "entity_id": "entity_01",
      "asset_id": "asset_05",
      "prompt_reference_id": "reference_asset_03",
      "preservation_priority": "High",
      "recognizability_requirement": "Near Exact — face and hair",
      "source": "Reference Asset",
      "immutable_attributes": [
        "East Asian female, early-to-mid twenties — do not alter ethnicity, age register, or gender",
        "Hair in a neat bun or updo — clean, office-ready styling",
        "Lean, naturally healthy build — not muscular",
        "Bright, natural complexion — warm light skin tone, natural texture",
        "Calm, lightly pleased, natural expression"
      ],
      "flexible_attributes": [
        "Clothing — replaced with polished-casual office wear (blouse, clean top) in the generated scene",
        "Exact expression (subtle off-camera gaze may become relaxed downward gaze at the drink, or soft smile)",
        "Exact head tilt and body angle"
      ],
      "generation_rule": "Reproduce this woman's face, hair bun, and overall look from reference_asset_03 (image 5.png). Dress her in polished-casual office wear in the CLEVER scene. Discard the sports bra, shaker, and outdoor background from that image entirely."
    },

    "EntitySourceMap": [
      {
        "entity_id": "entity_01",
        "source_image": "image 5.png",
        "asset_id": "asset_05",
        "prompt_reference_id": "reference_asset_03",
        "extraction_scope": "Face, hair bun, build type, complexion — exclude clothing, shaker, and outdoor background"
      }
    ]
  }
}
```

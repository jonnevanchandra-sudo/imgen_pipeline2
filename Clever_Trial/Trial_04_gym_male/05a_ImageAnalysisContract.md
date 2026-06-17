```json
{
  "ImageAnalysisContract": {
    "Metadata": {
      "brand": "CLEVER Protein",
      "campaign": "日本製輕盈美學 — gym variant, male model",
      "framework": "Image Analysis v5.0",
      "stage": "5a — Pre-Scene Assembly Asset Extraction",
      "variant": "Trial_04_gym_male — male model face reference from image 6.png",
      "source_image": "image 6.png",
      "analysis_date": "2026-06-16"
    },

    "ClientIntentDeclaration": {
      "image_ref": "image 6.png",
      "purpose": "Lock the male model's face, hair, and physical build type as the protagonist for entity_01 in the gym scene. This image provides the identity reference for the human subject only.",
      "what_to_lock": ["Face and facial features", "Hair style and color", "Overall physical build type (lean, not muscular)", "Skin tone and texture register"],
      "lock_strictness": "Near-Exact for face and hair. Approximate for build (general body type only, not exact proportions).",
      "what_to_exclude": [
        "The shaker/bottle in the image — product comes from reference_asset_01 (image1.png)",
        "The drink/liquid in the image — product comes from reference_asset_01",
        "The outdoor background and sky — environment comes from entity_06 (gym studio)",
        "Any branding on the shaker in this image"
      ]
    },

    "AssetClassification": {
      "type": "Identity-Bearing",
      "sub_type": "Human Subject — Male Model Face Reference",
      "confidence": 1.0
    },

    "ObservationLog": [
      {
        "attribute": "Ethnicity and age",
        "status": "Observable",
        "value": "East Asian male, estimated 24–28 years old",
        "confidence": 0.95
      },
      {
        "attribute": "Hair",
        "status": "Observable",
        "value": "Short dark hair, slightly swept/tousled, appears lightly damp or post-exercise. Natural texture, no heavy styling product.",
        "confidence": 0.95
      },
      {
        "attribute": "Build",
        "status": "Observable",
        "value": "Lean, naturally healthy — not muscular, not bulky. Visible neck and shoulder lean without gym archetype physique.",
        "confidence": 0.90
      },
      {
        "attribute": "Skin",
        "status": "Observable",
        "value": "Light warm skin tone, natural texture, no heavy retouching visible. Pores and subtle tone variation present.",
        "confidence": 0.90
      },
      {
        "attribute": "Expression and pose",
        "status": "Observable",
        "value": "Eyes closed in a natural, relaxed drinking motion. Lips against bottle. Calm, post-effort ease. Not straining, not performing.",
        "confidence": 0.95
      },
      {
        "attribute": "Clothing",
        "status": "Observable",
        "value": "Light blue textured athletic t-shirt — moisture-wicking weave pattern visible. Form-fitting but not tight. Clean, modern athletic aesthetic.",
        "confidence": 0.95
      },
      {
        "attribute": "Shaker/product in image",
        "status": "Observable — EXCLUDED",
        "value": "Clear translucent shaker with pink/light-colored contents and white lid. NOT CLEVER branded. Excluded entirely — product reference comes from image1.png.",
        "confidence": 1.0
      },
      {
        "attribute": "Background in image",
        "status": "Observable — EXCLUDED",
        "value": "Bright outdoor sky, blue. Excluded — gym studio environment comes from entity_06 generated context.",
        "confidence": 1.0
      }
    ],

    "PreservationContract": {
      "entity_id": "entity_01",
      "asset_id": "asset_06",
      "prompt_reference_id": "reference_asset_03",
      "preservation_priority": "High",
      "recognizability_requirement": "Near Exact — face and hair",
      "source": "Reference Asset",
      "immutable_attributes": [
        "East Asian male, mid-to-late twenties — do not alter ethnicity, age register, or gender",
        "Short dark hair, slightly damp/tousled post-workout texture",
        "Lean, naturally healthy build — not muscular, not bulky",
        "Natural skin texture — visible pores, warm light skin tone, no airbrushing",
        "Calm, post-workout ease expression — relaxed, not straining"
      ],
      "flexible_attributes": [
        "Exact expression (eyes-closed drinking from image may become eyes-open holding shaker post-drink)",
        "Exact clothing color (light blue in image → may remain blue or shift to white/neutral athletic t-shirt in CLEVER scene)",
        "Exact head tilt or body angle"
      ],
      "generation_rule": "Reproduce this man's face and overall look from reference_asset_03 (image 6.png). Use only the person — discard the shaker, drink, and background from that image entirely."
    },

    "EntitySourceMap": [
      {
        "entity_id": "entity_01",
        "source_image": "image 6.png",
        "asset_id": "asset_06",
        "prompt_reference_id": "reference_asset_03",
        "extraction_scope": "Face, hair, build type — exclude shaker and background"
      }
    ]
  }
}
```

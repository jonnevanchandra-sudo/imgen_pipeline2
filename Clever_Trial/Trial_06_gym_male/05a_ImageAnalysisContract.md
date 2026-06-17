```json
{
  "ImageAnalysisContract": {
    "Metadata": {
      "brand": "CLEVER Protein",
      "campaign": "日本製清蛋白 · 輕盈恢復力 — male post-workout light recovery trial acquisition",
      "framework": "Image Analysis v5.0",
      "stage": "5a — Pre-Scene Assembly Asset Extraction",
      "variant": "Trial_06_gym_male — male model face reference from image7.png and image (1).png (same model, two angles)",
      "source_images": ["image7.png", "image (1).png"],
      "analysis_date": "2026-06-17"
    },

    "ClientIntentDeclaration": {
      "image_refs": ["image7.png", "image (1).png"],
      "purpose": "Lock the male model's face, hair, and physical build type as the protagonist for entity_01. Both images show the same person from two different angles/moments — together they give a stronger, cross-checked identity reference than either alone.",
      "what_to_lock": ["Face and facial features", "Hair style and color", "Overall physical build type (lean, athletic, not bodybuilder-bulky)", "Skin tone and texture register"],
      "lock_strictness": "Near-Exact for face and hair, cross-validated across both images. Approximate for build (general body type only, not exact proportions).",
      "what_to_exclude": [
        "image7.png: the plank/push-up pose, the stability ball, the indoor plant, and the exact tank-top wardrobe — pose and wardrobe are not locked",
        "image (1).png: the standing-by-window pose, the CLEVER logo, the '日日飲，激發體能'-style on-image ad text, the small notification/chat-bubble UI graphic, and the exact tank-top wardrobe visible in that frame — these are existing creative/UI elements baked into that image, not attributes of the person, and must not be reproduced or treated as scene content",
        "Any background, room, or window detail from either image — environment for entity_06 is fully generated separately"
      ]
    },

    "AssetClassification": {
      "type": "Identity-Bearing",
      "sub_type": "Human Subject — Male Model Face Reference (dual-image cross-reference)",
      "confidence": 1.0
    },

    "ObservationLog": [
      {
        "attribute": "Ethnicity and age",
        "status": "Observable",
        "value": "East Asian male, estimated mid-twenties. Consistent across both images.",
        "confidence": 0.95
      },
      {
        "attribute": "Hair",
        "status": "Observable",
        "value": "Short-to-medium dark hair, swept back/upward with natural volume at the front. Same hairstyle visible in both images.",
        "confidence": 0.95
      },
      {
        "attribute": "Face",
        "status": "Observable",
        "value": "Defined jawline, straight brows, narrow nose bridge. Facial structure consistent across both reference images, confirming same identity.",
        "confidence": 0.93
      },
      {
        "attribute": "Build",
        "status": "Observable",
        "value": "Lean, athletic build with visible muscle tone (image7.png shows toned arms/shoulders in a plank position) — toned, not bodybuilder-bulky. Image (1).png shows the same lean frame standing.",
        "confidence": 0.88
      },
      {
        "attribute": "Skin",
        "status": "Observable",
        "value": "Light-medium warm skin tone, natural texture, no heavy retouching visible in either source image.",
        "confidence": 0.85
      },
      {
        "attribute": "Expression and pose — image7.png",
        "status": "Observable — EXCLUDED (pose not locked)",
        "value": "Mid-plank/push-up exercise pose, hand on a stability ball, focused exertion expression. Excluded as a locked attribute — the generated scene is a post-workout cool-down, not mid-exercise.",
        "confidence": 0.95
      },
      {
        "attribute": "Expression and pose — image (1).png",
        "status": "Observable — EXCLUDED (pose not locked)",
        "value": "Standing, three-quarter angle, looking off-camera, neutral-confident expression, against large windows. Useful as a secondary face/profile angle only.",
        "confidence": 0.9
      },
      {
        "attribute": "Wardrobe in source images",
        "status": "Observable — EXCLUDED",
        "value": "Dark athletic tank top in both images. Excluded — wardrobe for the generated scene is specified separately (light athletic t-shirt, CLEVER scene register).",
        "confidence": 0.9
      },
      {
        "attribute": "Background and overlays in image (1).png",
        "status": "Observable — EXCLUDED",
        "value": "Bright window-lit interior background, a white 'CLEVER' wordmark, on-image ad-style text, and a small rounded notification/chat-bubble graphic in the upper right — all pre-existing creative/UI elements from the source frame, not attributes of the person. Fully excluded from extraction; the new typography and brand lockup are defined fresh in this contract chain.",
        "confidence": 1.0
      },
      {
        "attribute": "Background in image7.png",
        "status": "Observable — EXCLUDED",
        "value": "Indoor room with a houseplant and soft window light. Excluded — environment for entity_06 is generated separately.",
        "confidence": 0.9
      }
    ],

    "PreservationContract": {
      "entity_id": "entity_01",
      "asset_ids": ["asset_07", "asset_08"],
      "prompt_reference_ids": ["reference_asset_03", "reference_asset_04"],
      "preservation_priority": "High",
      "recognizability_requirement": "Near Exact — face and hair, cross-validated across both reference images",
      "source": "Reference Asset",
      "immutable_attributes": [
        "East Asian male, mid-twenties — do not alter ethnicity, age register, or gender",
        "Short-to-medium dark hair, swept back/upward with natural volume",
        "Defined jawline and facial structure as shown in both reference images",
        "Lean, athletic build with visible muscle tone — toned, not bodybuilder-bulky",
        "Light-medium warm skin tone, natural texture"
      ],
      "flexible_attributes": [
        "Exact expression (plank exertion / neutral-confident in references → calm, lightly satisfied post-workout ease in the generated scene)",
        "Exact pose and body angle",
        "Clothing (dark tank top in both references → light athletic t-shirt in the generated CLEVER scene)"
      ],
      "generation_rule": "Reproduce this man's face, hair, and lean athletic build using both image7.png and image (1).png as cross-referenced identity sources. Use only the person from each image — discard all poses, activities, backgrounds, and any pre-existing text/logo/UI overlays visible in either source image."
    },

    "EntitySourceMap": [
      {
        "entity_id": "entity_01",
        "source_images": ["image7.png", "image (1).png"],
        "asset_ids": ["asset_07", "asset_08"],
        "prompt_reference_ids": ["reference_asset_03", "reference_asset_04"],
        "extraction_scope": "Face, hair, build type only — exclude pose, activity, wardrobe, background, and (for image (1).png) the pre-existing CLEVER logo, ad text, and notification UI graphic baked into that frame"
      }
    ]
  }
}
```

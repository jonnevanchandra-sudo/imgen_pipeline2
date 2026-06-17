```json
{
  "VisualPrompt": {
    "CRITICAL": {
      "subjects": "One East Asian woman, early-to-mid twenties, hair in a neat clean bun, lean and naturally healthy build. Face and look reproduced from reference_asset_03 (image 5.png). Wearing polished-casual office wear — clean blouse or fitted top, NOT athletic wear. Seated at a near-empty desk on her afternoon break, calm, lightly satisfied, quietly confident. Holding or reaching for a transparent shaker of clear, pale-yellow lemon protein drink with a lemon slice inside. The drink is the hero: visibly clear and translucent, light passing through it, never opaque or milky.",
      "emotion": "Calm, lightly satisfied, quietly confident — a small guilt-free moment of self-care at 3:30pm. No strain, no dieting anxiety, no performance."
    },
    "HIGH": {
      "brand": "A CLEVER 'CLEAR PROTEIN' lemon-flavor pouch stands on the desk facing the camera, clearly legible. CLEVER logo visible on the shaker. A 'Made in Japan / 日本製' cue is legible in frame.",
      "setting": "A near-empty, clean, minimal desk — sky-blue and white register. Only three things on the surface: the pouch, the shaker, and one small desk clock reading approximately 3:30. The background is a clean, smooth, uncluttered sky-blue plane — no windows, no plants, no office furniture or shelving behind the subject.",
      "typography": "Bold modern sans-serif headline '告別3點3罪惡感！' in the upper background zone above and behind the model. Subtitle '日本製 · 清蛋白' smaller below it. White or dark-blue text — whichever reads most legibly against the sky-blue background. Fully legible at mobile screen size."
    },
    "FORMAT": "Square 1:1 for an Instagram/Facebook feed post. No faces, brand elements, or critical text in the top 12% or bottom 12% of the frame.",
    "LIGHTING": "Soft, bright high-key daylight. The clear drink and pouch get the cleanest, most direct light — a gentle specular glint on the glass makes the drink look crisp and refreshing. The model is lit a touch softer. The background is evenly lit as a smooth flat plane — no shadows pooling in corners, no bright spots behind the subject. Skin warm-neutral, never orange.",
    "CAMERA": "Eye-level near medium shot at desk distance. 85mm at f/4: foreground pack and shaker are crisply sharp; the model sharp to gently soft by depth; the already-clean background softens further into a smooth, even sky-blue plane. Typography in the background zone slightly softened by depth but fully legible. Progressive bokeh falloff — no flat uniform blur.",
    "AUTHENTICITY": {
      "human_authenticity": "Reproduce the female model's face and natural complexion from reference_asset_03 — visible pores, fine lines, subtle tone variation, natural asymmetry. Candid, relaxed expression. No beauty filter, no smoothing.",
      "environmental_authenticity": "The desk is intentionally minimal and clean — a curated photoshoot-set surface. Only natural material imperfections (subtle desk surface reflections) are acceptable; no props, clutter, or everyday objects beyond the pack, shaker, and small clock.",
      "material_authenticity": "Believable glass and liquid optics — light passing through the clear drink, light condensation on the shaker, matte pouch surface vs. glossy bottle body.",
      "imperfection_rule": "Credibility over perfection for skin and material behavior. The desk and background, however, must be genuinely clean and pristine."
    },
    "SCENE": "The pack and shaker sit in the foreground, nearer the camera than the model's face. The small clock is on the desk surface to one side — the only other object. The background behind her is a single clean sky-blue plane with the typography in the upper zone.",
    "BRAND_ASSETS": [
      {
        "asset_ref": "reference_asset_01",
        "instruction": "reference_asset_01 is image1.png — it contains the CLEVER lemon 'CLEAR PROTEIN' pouch and the transparent shaker with clear pale-yellow lemon drink. Reproduce the pouch exactly: white body, large dark-blue 'CLEAR PROTEIN' typography, bright yellow lemon-flavor band at top, CLEVER logo, and functional badges — same shapes, colors, and proportions, do not redraw from memory. Reproduce the shaker and its CLEVER logo exactly; keep the drink clear and translucent, never opaque. Use only the product and bottle from this image — discard the male model and gym background from image1.png entirely."
      },
      {
        "asset_ref": "reference_asset_02",
        "instruction": "reference_asset_02 is image4.png — it contains the CLEVER wordmark and a clean, minimal sky-blue layout. Reproduce the CLEVER logo exactly: same letterforms, same color, same proportions, do not redraw from memory. Use image4's clean minimal sky-blue aesthetic as the target visual register for the background and overall feel. Exclude the timing-clock graphic, any pricing, and the specific model from that image."
      },
      {
        "asset_ref": "reference_asset_03",
        "instruction": "reference_asset_03 is image 5.png — it contains the female model whose face and look must be reproduced as the human subject. Reproduce her face, neat hair bun, and lean natural build exactly. In the reference she wears a blue sports bra — in the generated scene she wears polished-casual office wear (blouse or fitted top) instead. Also discard the purple/pink shaker and the outdoor mountain background from image 5.png entirely — only the person's face, hair, and overall look carry through."
      }
    ],
    "NEGATIVE": "No thick, opaque, or milky shake. No gym, dumbbells, muscular posing, or athletic staging. No sports bra or workout clothing on the model. No black supplement tubs. No before/after or weighing scale. No junk food or snack clutter on the desk. No grape variant or multi-pack lineup. No outdoor or mountain background. No windows, plants, office shelving, or furniture visible in the background. No background clutter of any kind. No blown-out bright spots behind the subject. No smoothed AI skin. No invented marketing slogans or text beyond the specified headline and subtitle. Do not carry through the sports bra, shaker, or outdoor background from image 5.png."
  },
  "ReferenceAssetManifest": [
    {
      "asset_id": "asset_01",
      "filename": "image1.png",
      "type": "Brand-Bearing",
      "prompt_reference_id": "reference_asset_01",
      "attach_to_api_call": true,
      "strictness": "Exact"
    },
    {
      "asset_id": "asset_04",
      "filename": "image4.png",
      "type": "Brand-Bearing",
      "prompt_reference_id": "reference_asset_02",
      "attach_to_api_call": true,
      "strictness": "Exact"
    },
    {
      "asset_id": "asset_05",
      "filename": "image 5.png",
      "type": "Identity-Bearing",
      "prompt_reference_id": "reference_asset_03",
      "attach_to_api_call": true,
      "strictness": "Near Exact — face and hair only"
    }
  ]
}
```

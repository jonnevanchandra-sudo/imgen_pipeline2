```json
{
  "VisualPrompt": {
    "CRITICAL": {
      "subjects": "One Hong Kong office woman, mid-to-late twenties, naturally healthy and attractive East Asian, in light polished-casual office wear — not gym clothes. Seated at a near-empty desk on her afternoon break, holding or reaching for a transparent shaker of clear, pale-yellow lemon protein drink with a lemon slice inside. The drink is the hero: visibly clear and translucent, light passing through it, never opaque or milky.",
      "emotion": "Calm, lightly satisfied, quietly confident — a small guilt-free moment of self-care. No strain, no dieting anxiety, no performance."
    },
    "HIGH": {
      "brand": "A CLEVER 'CLEAR PROTEIN' lemon-flavor pouch stands on the desk facing the camera, clearly legible. CLEVER logo visible on the shaker. A 'Made in Japan / 日本製' cue is legible in frame.",
      "setting": "A near-empty, clean, minimal desk — sky-blue and white register. Only three things on the surface: the pouch, the shaker, and one small desk clock reading approximately 3:30. The background is a clean, smooth, uncluttered sky-blue plane — no windows, no plants, no office furniture or shelving behind the subject. The desk and background together read as a purposeful, curated photoshoot set, not a lived-in workspace."
    },
    "LOW": {
      "style": "Clean, bright lifestyle product photography for social commerce — polished and minimal, with the quality of a controlled studio shoot."
    },
    "FORMAT": "Square 1:1 for an Instagram/Facebook feed post. No faces, brand elements, or critical visual information in the top 12% or bottom 12% of the frame.",
    "LIGHTING": "Soft, bright high-key daylight. The clear drink and pouch get the cleanest, most direct light — a gentle specular glint on the glass and liquid makes the drink look crisp and refreshing. The woman is lit a touch softer. The background is evenly lit as a smooth flat plane — no shadows pooling in corners, no window highlights or practical light sources behind the subject. Nothing in the background is brighter than the hero product cluster. Skin warm-neutral, never orange.",
    "CAMERA": "Eye-level near medium shot at desk distance. 85mm at f/4: foreground pack and shaker are crisply sharp; the woman sharp to gently soft by depth; the already-clean background softens further into a smooth, even sky-blue plane. Smooth progressive bokeh falloff — no flat uniform blur, no busy ring bokeh.",
    "AUTHENTICITY": {
      "human_authenticity": "Real skin — visible pores, fine lines, subtle tone variation, natural asymmetry. Candid unposed expression, relaxed shoulders.",
      "environmental_authenticity": "The desk is intentionally minimal and clean — a curated photoshoot-set surface, not a real cluttered office. Only natural material imperfections (subtle desk surface reflections) are acceptable; no props, clutter, or everyday objects beyond the pack, shaker, and small clock.",
      "material_authenticity": "Believable glass and liquid optics — light passing through the clear drink, light condensation on the shaker, matte pouch surface vs. glossy bottle body.",
      "imperfection_rule": "Credibility over perfection for skin and material behavior. The desk and background, however, must be genuinely clean and pristine — clutter or shadow in those areas works against the intended concept."
    },
    "SCENE": "The pack and shaker sit in the foreground, nearer the camera than the woman's face. The small clock is on the desk surface to one side — the only other object. The background behind her is a single clean sky-blue plane.",
    "BRAND_ASSETS": [
      {
        "asset_ref": "reference_asset_01",
        "instruction": "reference_asset_01 is image1.png — it contains the CLEVER lemon 'CLEAR PROTEIN' pouch and the transparent shaker with clear pale-yellow lemon drink. Reproduce the pouch exactly: white body, large dark-blue 'CLEAR PROTEIN' typography, bright yellow lemon-flavor band at top, CLEVER logo, and functional badges — same shapes, colors, and proportions, do not redraw from memory. Reproduce the shaker and its CLEVER logo exactly; keep the drink clear and translucent, never opaque. Use only the product and bottle from this image — discard the male model and gym background entirely."
      },
      {
        "asset_ref": "reference_asset_02",
        "instruction": "reference_asset_02 is image4.png — it contains the CLEVER wordmark and a clean, minimal sky-blue layout. Reproduce the CLEVER logo exactly: same letterforms, same color, same proportions, do not redraw from memory. Use image4's clean minimal sky-blue aesthetic as the target visual register for the background and overall feel. Exclude the timing-clock graphic, any pricing, and the specific model from that image."
      }
    ],
    "NEGATIVE": "No thick, opaque, or milky shake. No gym, dumbbells, muscular posing, or athletic staging. No black supplement tubs. No before-after or weighing scale. No junk food or snack clutter on the desk. No grape variant or multi-pack lineup. No outdoor running scene or timing-clock infographic. No windows, plants, office shelving, or furniture visible in the background. No background clutter of any kind — the surface and backdrop must be near-empty. No blown-out bright spots behind the subject. No smoothed AI skin. No invented marketing slogans or text paragraphs."
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
    }
  ]
}
```

```json
{
  "VisualPrompt": {
    "CRITICAL": {
      "subjects": "One Hong Kong woman, mid-to-late twenties, naturally healthy and attractive East Asian, in a white mesh/crochet crop top and pastel lemon-yellow workout shorts. Seated on the edge of a rolled yoga mat or standing in a relaxed post-workout posture in a bright modern yoga/fitness studio. Holding or drinking from a transparent shaker of clear, pale-yellow lemon protein drink with a lemon slice inside. The drink is the hero: visibly clear and translucent, light physically passing through it, never opaque or milky.",
      "emotion": "Calm, lightly satisfied post-workout release. Quiet confidence — she's done the work, and this is the light, deserved reward. Not strained, not sweaty, not performative."
    },
    "HIGH": {
      "brand": "A CLEVER 'CLEAR PROTEIN' lemon-flavor pouch rests on the clean gym floor facing the camera, clearly legible. CLEVER logo visible on the shaker. A 'Made in Japan / 日本製' cue is legible in frame.",
      "setting": "A bright modern yoga/pilates studio — large floor-to-ceiling windows dominate the background, flooding the space with soft natural sky-blue daylight. Clean light wood or pale rubber flooring. A rolled yoga mat to one side is the only floor prop. No heavy gym equipment, no mirrors, no dark surfaces.",
      "typography": "Bold modern sans-serif headline '告別運動後重裝感！' in the upper window-light background zone. Subtitle '日本製 · 清蛋白' smaller below it. White text against the bright sky-blue window background. Fully legible at mobile screen size."
    },
    "FORMAT": "Square 1:1 for an Instagram/Facebook feed post. No faces, brand elements, or critical text in the top 12% or bottom 12% of the frame.",
    "LIGHTING": "Bright natural daylight from large gym windows — high-key, soft, directional. The clear shaker and pack receive the cleanest, most direct light; a gentle specular glint on the glass makes the drink look crisp and refreshing. Skin warm-neutral with a light healthy flush — never orange. Background window zone is bright and luminous but controlled, not blown out — white ad text must remain readable against it. No harsh artificial spotlights.",
    "CAMERA": "Eye-level near medium shot. 85mm at f/4. Progressive depth-dependent bokeh: foreground pack and shaker crisply sharp; the woman sharp to softly diffuse by depth; the gym windows in the background soften to a smooth glowing sky-blue plane — typography in this zone is slightly softened but fully legible. No flat uniform blur.",
    "AUTHENTICITY": {
      "human_authenticity": "Real skin — visible pores, fine lines, subtle tone variation, light post-workout flush, natural asymmetry. Candid, relaxed expression. No beauty filter, no smoothing.",
      "material_authenticity": "Believable glass and liquid physics — light passing through the clear drink, light condensation on the shaker, matte pouch surface vs. glossy bottle body. Mesh fabric texture on crop top.",
      "imperfection_rule": "Credibility over perfection for skin and the drink's liquid behavior. The gym floor and background must be genuinely clean — clutter or harsh shadows work against the concept."
    },
    "SCENE": "The pack and shaker sit in the foreground, closer to the camera than the woman's face. The rolled yoga mat rests to one side on the floor. The background is the bright gym window plane with the typography overlay in the upper zone. Only three objects in the foreground/midground cluster: the woman, the pack, the shaker.",
    "BRAND_ASSETS": [
      {
        "asset_ref": "reference_asset_01",
        "instruction": "reference_asset_01 is image1.png — it contains the CLEVER lemon 'CLEAR PROTEIN' pouch and the transparent shaker with clear pale-yellow lemon drink. Reproduce the pouch exactly: white body, large dark-blue 'CLEAR PROTEIN' typography, bright yellow lemon-flavor band at top, CLEVER logo, and functional badges — same shapes, colors, and proportions, do not redraw from memory. Reproduce the shaker and its CLEVER logo exactly; keep the drink clear and translucent, never opaque. Use only the product and bottle from this image — discard the male model and gym floor background entirely."
      },
      {
        "asset_ref": "reference_asset_02",
        "instruction": "reference_asset_02 is image4.png — it contains the CLEVER wordmark and a clean, minimal sky-blue layout. Reproduce the CLEVER logo exactly: same letterforms, same color, same proportions, do not redraw from memory. Use image4's clean minimal sky-blue tone as the target register for the overall bright atmosphere. Exclude the timing-clock graphic, any pricing, and the specific model from that image."
      }
    ],
    "NEGATIVE": "No thick, opaque, or milky shake. No heavy dumbbells, barbells, weight machines, or weightlifting staging. No dark gym surfaces or harsh artificial spotlights. No mirrored gym walls. No sweating, straining, or muscular posing. No other people in the scene. No black supplement tubs. No before/after comparisons or weighing scales. No cluttered gym floor or gym bags. No grape variant or multi-pack lineup. No invented typography or slogans beyond the specified headline and subtitle. No smoothed AI skin or beauty filter. No gym locker room or changing room elements."
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

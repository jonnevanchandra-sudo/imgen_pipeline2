```json
{
  "VisualPrompt": {
    "CRITICAL": {
      "subjects": "One East Asian man, mid-twenties, short-to-medium dark hair swept back/upward, lean and athletic build with visible muscle tone — toned, not bodybuilder-bulky. Face and look reproduced from reference_asset_03 (image7.png) and reference_asset_04 (image (1).png) — same person, two cross-referenced angles. Light athletic t-shirt (white or light blue, clean sportswear), not a dark tank top. Post-workout cool-down in a bright modern studio, holding or just having finished drinking from a transparent shaker of clear, pale-yellow lemon protein drink with a lemon slice inside. The drink is the hero: visibly clear and translucent, light physically passing through it, never opaque or milky.",
      "emotion": "Calm, lightly satisfied post-workout release. Quiet, body-smart confidence — he's done the work, and this clear, light drink is the deserved reward. Not strained, not sweaty, not performative, not muscle-flexing."
    },
    "HIGH": {
      "brand": "A CLEVER 'CLEAR PROTEIN' lemon-flavor pouch rests on the clean studio floor facing the camera, clearly legible. CLEVER logo visible on the shaker. A 'Made in Japan / 日本製' cue is legible in frame.",
      "setting": "A bright modern fitness studio — large floor-to-ceiling windows dominate the background, flooding the space with soft natural sky-blue daylight. Clean light wood or pale rubber flooring. A rolled yoga/exercise mat to one side is the only floor prop. No heavy gym equipment, no mirrors, no dark surfaces.",
      "typography": "Bold modern sans-serif headline '日日飲，激發體能' in the upper window-light background zone. Subtitle '日本製 · 清蛋白' smaller below it. White text against the bright sky-blue window background. Fully legible at mobile screen size."
    },
    "FORMAT": "Square 1:1 for an Instagram/Facebook feed post. No faces, brand elements, or critical text in the top 12% or bottom 12% of the frame.",
    "LIGHTING": "Bright natural daylight from large studio windows — high-key, soft, directional. The clear shaker and pack receive the cleanest, most direct light; a gentle specular glint on the glass makes the drink look crisp and refreshing. Skin warm-neutral with a light healthy flush — never orange. Background window zone is bright and luminous but controlled, not blown out — white ad text must remain readable against it. No harsh artificial spotlights.",
    "CAMERA": "Eye-level near medium shot. 85mm at f/4. Progressive depth-dependent bokeh: foreground pack and shaker crisply sharp; the man sharp to softly diffuse by depth; the studio windows soften to a smooth glowing sky-blue plane — typography in this zone slightly softened but fully legible. No flat uniform blur.",
    "AUTHENTICITY": {
      "human_authenticity": "Reproduce the male model's face and natural skin texture from both reference_asset_03 and reference_asset_04 (same person, cross-referenced) — visible pores, natural asymmetry, light post-workout flush. Candid, relaxed expression. No beauty filter, no smoothing.",
      "material_authenticity": "Believable glass and liquid physics — light passing through the clear pale-yellow drink, light condensation on the shaker, matte pouch surface vs. glossy bottle body. Lightweight athletic fabric texture on t-shirt.",
      "imperfection_rule": "Credibility over perfection for skin and the drink's liquid behavior. Studio floor and background must be genuinely clean — clutter or harsh shadows work against the concept."
    },
    "SCENE": "The pack and shaker sit in the foreground, closer to the camera than the man's face. The rolled mat rests to one side on the floor. The background is the bright studio window plane with the typography overlay in the upper zone. Only three objects in the foreground/midground cluster: the man, the pack, the shaker.",
    "BRAND_ASSETS": [
      {
        "asset_ref": "reference_asset_01",
        "instruction": "reference_asset_01 is image1.png — it contains the CLEVER lemon 'CLEAR PROTEIN' pouch and the transparent shaker with clear pale-yellow lemon drink. Reproduce the pouch exactly: white body, large dark-blue 'CLEAR PROTEIN' typography, bright yellow lemon-flavor band at top, CLEVER logo, and functional badges — same shapes, colors, and proportions, do not redraw from memory. Reproduce the shaker and its CLEVER logo exactly; keep the drink clear and translucent, never opaque. Use only the product and bottle from this image — discard the model and background from image1.png entirely."
      },
      {
        "asset_ref": "reference_asset_02",
        "instruction": "reference_asset_02 is image4.png — it contains the CLEVER wordmark and a clean, minimal sky-blue layout. Reproduce the CLEVER logo exactly: same letterforms, same color, same proportions, do not redraw from memory. Use image4's clean minimal sky-blue tone as the target register for the overall bright atmosphere. Exclude the timing-clock graphic, any pricing, and the specific model from that image."
      },
      {
        "asset_ref": "reference_asset_03",
        "instruction": "reference_asset_03 is image7.png — it contains the male model whose face, hair, and build must be reproduced as the human subject, in a mid-plank exercise pose. Reproduce his face, short-to-medium dark hair, and lean athletic build exactly. Discard the plank pose, stability ball, houseplant, and indoor background from image7.png entirely — only the person's face, hair, and physical build carry through. Cross-reference against reference_asset_04 to confirm this is the same identity."
      },
      {
        "asset_ref": "reference_asset_04",
        "instruction": "reference_asset_04 is image (1).png — it shows the same male model as reference_asset_03 from a different angle, standing by a window. Use it only to reinforce the same facial identity and hairstyle. This image has a pre-existing white 'CLEVER' wordmark, on-image ad-style text, and a small notification/chat-bubble UI graphic baked into the frame, plus a dark tank top and a standing pose — discard all of that entirely. Do not reproduce the logo styling, text layout, UI graphic, pose, wardrobe, or background from this image; extract face and hair only."
      }
    ],
    "NEGATIVE": "No thick, opaque, or milky shake. No heavy dumbbells, barbells, weight machines, or weightlifting staging. No dark surfaces or harsh artificial spotlights. No mirrored walls. No outdoor sky or rooftop background — set is an indoor studio. No sweating, straining, or muscle-flexing/bodybuilder posing. No other people. No black supplement tubs. No before/after comparisons or weighing scales. No cluttered floor or gym bags. No invented typography beyond the specified headline and subtitle. No smoothed AI skin or beauty filter. No locker room elements. Do not carry through the pose, stability ball, plant, dark tank top, or backgrounds from image7.png or image (1).png. Do not reproduce the CLEVER logo styling, ad text, or notification/chat-bubble UI graphic baked into image (1).png."
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
      "asset_id": "asset_07",
      "filename": "image7.png",
      "type": "Identity-Bearing",
      "prompt_reference_id": "reference_asset_03",
      "attach_to_api_call": true,
      "strictness": "Near Exact — face, hair, and build only"
    },
    {
      "asset_id": "asset_08",
      "filename": "image (1).png",
      "type": "Identity-Bearing",
      "prompt_reference_id": "reference_asset_04",
      "attach_to_api_call": true,
      "strictness": "Near Exact — face and hair only"
    }
  ]
}
```

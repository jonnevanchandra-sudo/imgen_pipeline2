```json
{
  "_note": "v2 variant — upstream contracts (01–07) are identical to Trial_04_office/. Only change: CRITICAL.text asks the generator to find the natural compositional space for the typography rather than fixing it to the upper background zone.",

  "VisualPrompt": {
    "CRITICAL": {
      "subjects": "Hong Kong OL, mid-to-late twenties, East Asian, polished-casual office wear. Seated on her afternoon break at a near-empty desk, reaching for a transparent shaker of clear pale-yellow lemon protein drink — visibly translucent, light passing through, never opaque or milky.",
      "emotion": "Calm, lightly satisfied, quietly confident — guilt-free self-care, no strain, no diet anxiety.",
      "text": "Integrate on-image ad copy as a designed layout element — headline '告別3點3罪惡感！' in bold modern sans-serif, subtitle '日本製 · 清蛋白' smaller directly below. Position the typography in whichever area of the sky-blue background gives the cleanest, most natural reading space — upper-left, right side, or wherever the composition breathes most. The text must not overlap the OL's face or the product cluster; beyond that, let the visual flow guide placement so it feels designed into the image, not imposed on top of it. Both lines legible at mobile screen size."
    },
    "HIGH": {
      "brand": "CLEVER 'CLEAR PROTEIN' lemon-flavor pouch on the desk, facing the camera, clearly legible. CLEVER logo visible on the shaker. '日本製 / Made in Japan' readable in frame.",
      "setting": "Near-empty desk, sky-blue and white register — only the pouch, the shaker, and one small clock at ~3:30 on the surface. Background: smooth uncluttered sky-blue plane, no windows, plants, furniture, or shelving. Reads like a photography studio cyclorama, not a real office."
    },
    "LOW": {
      "style": "Clean, bright controlled lifestyle advertising photography."
    },
    "FORMAT": "Square 1:1 for Instagram/Facebook. No faces, brand elements, or text in the top 12% or bottom 12% of the frame.",
    "LIGHTING": "Soft high-key daylight. Clear drink and pouch get the most direct light — gentle specular glint on glass, liquid looks crisp and cold. OL softer, skin warm-neutral, never orange. Background evenly exposed as a flat plane — no pooling shadows, nothing behind the subject outshines the hero cluster.",
    "CAMERA": "Eye-level near medium shot at desk distance. 85mm at f/4 — foreground pack and shaker sharp, OL sharp to gently soft by depth, background fades to a smooth even plane. Progressive bokeh falloff; no flat uniform blur.",
    "AUTHENTICITY": {
      "human_authenticity": "Real skin — pores, fine lines, subtle tone variation, natural asymmetry. Candid unposed expression. No beauty filter, no airbrushing.",
      "material_authenticity": "Light condensation on the shaker; matte pouch surface against the glossy bottle body. Credibility over perfection for skin and materials."
    },
    "SCENE": "Pack and shaker in the foreground, nearer to the camera than the OL's face.",
    "BRAND_ASSETS": [
      {
        "asset_ref": "reference_asset_01",
        "instruction": "reference_asset_01 is image1.png — it contains the CLEVER lemon 'CLEAR PROTEIN' pouch and the transparent shaker with clear pale-yellow lemon drink. Reproduce the pouch exactly: white body, large dark-blue 'CLEAR PROTEIN' typography, bright yellow lemon-flavor band at top, CLEVER logo, and functional badges — same shapes, colors, and proportions; do not redraw from memory. Reproduce the shaker and its CLEVER logo exactly; keep the drink clear and translucent, never opaque. Use only the product and bottle — discard the male model and gym background entirely."
      },
      {
        "asset_ref": "reference_asset_02",
        "instruction": "reference_asset_02 is image4.png — it contains the CLEVER wordmark and a clean minimal sky-blue layout. Reproduce the CLEVER logo exactly: same letterforms, color, and proportions; do not redraw from memory. Use image4's clean minimal sky-blue aesthetic as the target visual register for the background. Exclude the timing-clock graphic, any pricing, and the specific model from that image."
      }
    ],
    "NEGATIVE": "No opaque or milky shake. No gym, dumbbells, or muscular posing. No before-after imagery or weighing scales. No windows, plants, or furniture in background. No desk clutter beyond the pack, shaker, and small clock. No text or typography beyond '告別3點3罪惡感！' and '日本製 · 清蛋白'. No smoothed AI skin. No blown-out bright spots behind the subject."
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

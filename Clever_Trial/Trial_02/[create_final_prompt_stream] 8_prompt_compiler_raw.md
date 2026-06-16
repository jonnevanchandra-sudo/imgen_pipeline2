```json
{
  "VisualPrompt": {
    "CRITICAL": {
      "subjects": "One Hong Kong office woman, late twenties, healthy and natural, in light polished-casual office wear — not gym clothes. Seated at her desk on an afternoon break, holding a transparent shaker of clear, pale-yellow lemon protein drink with a lemon slice. The drink is the hero: visibly clear and translucent, light passing through it.",
      "emotion": "Calm, lightly satisfied, quietly confident — a guilt-free moment, no strain or dieting anxiety."
    },
    "HIGH": {
      "brand": "A CLEVER 'CLEAR PROTEIN' lemon pouch stands on the desk beside the shaker, facing camera and clearly legible; the CLEVER logo reads on the bottle; a 'Made in Japan / 日本製' cue is legible in frame.",
      "setting": "A bright, clean, minimal office desk — light sky-blue and white, tidy and airy. A subtle afternoon cue like a small desk clock near 3:30."
    },
    "LOW": {
      "style": "Clean, bright lifestyle product photography — polished but credible, not a sterile studio packshot."
    },
    "FORMAT": "Square 1:1 feed post. Keep faces, brand elements, and product clear of the top and bottom 12% for caption overlays.",
    "LIGHTING": "Soft, bright high-key daylight. The drink and pouch get the cleanest, brightest light with a gentle specular glint on glass and liquid; the woman a touch softer; the office behind her exposed down so no window outshines the hero. Skin warm-neutral, never orange. No studio flatness.",
    "CAMERA": "Eye-level near medium shot at desk distance, peer-level. 50mm at f/4: foreground drink and pouch crisply sharp, the woman sharp to gently soft by depth, office softening progressively with distance — the desk clock stays semi-legible, far wall softer. Smooth gentle bokeh, no flat uniform blur.",
    "AUTHENTICITY": {
      "human_authenticity": "Real skin — visible pores, fine lines, subtle tone variation, natural asymmetry; candid unposed expression, relaxed shoulders.",
      "environmental_authenticity": "A lived-in but tidy desk with natural reflections and everyday detail, not an empty CGI set.",
      "material_authenticity": "Believable glass and liquid optics, light condensation on the shaker, true fabric behavior.",
      "imperfection_rule": "Credibility over perfection — no plastic, over-smoothed or beauty-filtered rendering."
    },
    "SCENE": "She holds the shaker in the foreground; the pouch stands on the desk just beside it, both nearer the camera than her face.",
    "BRAND_ASSETS": [
      {
        "asset_ref": "reference_asset_01",
        "instruction": "reference_asset_01 contains the CLEVER lemon-flavor 'CLEAR PROTEIN' pouch and the transparent shaker bottle with clear pale-yellow drink and lemon. Reproduce the pouch exactly — white body, large blue 'CLEAR PROTEIN' typography, yellow lemon flavor strip and badges, CLEVER logo — same shapes, colors, and proportions. Reproduce the shaker and its CLEVER logo, and keep the drink clear and translucent, never opaque or milky. Use only the product and bottle from this image; ignore its gym background and any person in it. Do not redraw the packaging or logo from memory."
      },
      {
        "asset_ref": "reference_asset_02",
        "instruction": "reference_asset_02 contains the CLEVER logo / wordmark and the 'Made in Japan / 日本製' cue in a clean sky-blue layout. Reproduce the CLEVER wordmark exactly — same letterforms, color, and proportions — and include a legible 'Made in Japan / 日本製' cue. Do not reproduce the timing-clock graphic, pricing, or the specific model from this image. Do not redraw the logo from memory."
      }
    ],
    "NEGATIVE": "No thick, opaque or milky shake. No gym, dumbbells, or muscular posing. No black supplement tubs. No before-after or weighing scale. No junk food. No grape variant, multi-pack lineup, outdoor running, or timing infographic. No blown-out window. No smoothed AI skin. No invented slogans or paragraphs."
  },
  "ReferenceAssetManifest": [
    {
      "asset_id": "asset_01",
      "filename": "reference_01.jpg",
      "type": "Brand-Bearing",
      "prompt_reference_id": "reference_asset_01",
      "attach_to_api_call": true,
      "strictness": "Exact"
    },
    {
      "asset_id": "asset_04",
      "filename": "reference_04.jpg",
      "type": "Brand-Bearing",
      "prompt_reference_id": "reference_asset_02",
      "attach_to_api_call": true,
      "strictness": "Exact"
    }
  ]
}
```

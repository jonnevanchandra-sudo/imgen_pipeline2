```json
{
  "VisualPrompt": {
    "CRITICAL": {
      "subjects": "One East Asian woman in her twenties, wearing polished-casual office wear — clean blouse or fitted top, NOT athletic wear. Face must match reference_asset_03 (image 5.png) exactly — use that face as the model. Seated at a near-empty desk on her afternoon break, calm, lightly satisfied, quietly confident. Holding or reaching for a transparent shaker of clear, pale-yellow lemon protein drink with a lemon slice inside. The drink is visibly clear and translucent — never opaque or milky.",
      "emotion": "Calm, lightly satisfied, quietly confident — a small guilt-free self-care moment at 3:30pm. No strain, no dieting anxiety."
    },
    "HIGH": {
      "brand": "CLEVER 'CLEAR PROTEIN' lemon-flavor pouch on desk facing camera, clearly legible. CLEVER logo visible on the shaker. 'Made in Japan / 日本製' cue legible in frame.",
      "setting": "A real but spotlessly styled office desk. Near-empty surface: the CLEVER pouch, the shaker, and one empty white ceramic mug (the old habit, quietly set aside) — nothing else. Background: a soft cream or white office wall with natural daylight falling from the side. Real office atmosphere, commercial photoshoot quality — recognizably an office, but clean, minimal, and deliberate. No shelving, no plants, no stacks of files, no clutter visible behind the subject.",
      "typography": "Bold modern sans-serif headline '告別3點3罪惡感！' in the upper background zone above the model. Subtitle '日本製 · 清蛋白' smaller below it. Dark navy blue text against the cream/white wall — consistent with CLEVER's brand dark-blue. Fully legible at mobile screen size."
    },
    "FORMAT": "Square 1:1 for Instagram/Facebook feed. No faces, brand elements, or critical text in the top or bottom 12% of frame.",
    "LIGHTING": "Soft natural daylight from one side — warm, directional, not harsh. Clear drink and pouch get the cleanest, most direct light with a gentle specular glint on the glass. Model lit softly by the same window source. Background wall carries the warm-soft window light but stays calm and uncluttered — no blown-out bright spots. Skin warm-neutral.",
    "CAMERA": "Eye-level near medium shot at desk distance. 85mm at f/4. Foreground pack and shaker crisply sharp; model sharp to gently soft by depth; background wall softens into a smooth, warm, diffused cream tone. Typography in the wall zone slightly softened but fully legible. Progressive bokeh falloff — no flat uniform blur.",
    "AUTHENTICITY": "Natural skin texture — visible pores, subtle tone variation, no beauty filter, no smoothing. Match the model's natural complexion from reference_asset_03. Believable glass and liquid optics — light passing through the clear drink, light condensation on shaker. The cream wall and natural light should feel like a real office, not a studio set.",
    "SCENE": "Pack and shaker in foreground, nearer the camera than the model's face. Empty white ceramic mug on the desk surface beside or behind the product cluster — the only other desk object. Cream/white office wall behind her with typography in the upper zone.",
    "BRAND_ASSETS": [
      {
        "asset_ref": "reference_asset_01",
        "instruction": "reference_asset_01 is image1.png — reproduce the CLEVER lemon CLEAR PROTEIN pouch and transparent shaker exactly. White pouch body, large dark-blue 'CLEAR PROTEIN' text, yellow lemon flavor band at top, CLEVER logo, functional badges — same shapes, colors, and proportions. Keep the drink clear and translucent, never opaque. Use only the product and bottle from this image; discard the male model and gym background entirely."
      },
      {
        "asset_ref": "reference_asset_02",
        "instruction": "reference_asset_02 is image4.png — reproduce the CLEVER wordmark exactly: same letterforms, color, proportions, do not redraw from memory. Use image4's clean minimal sky-blue aesthetic as the target visual register for the background. Exclude the timing-clock graphic and the model in that image."
      },
      {
        "asset_ref": "reference_asset_03",
        "instruction": "reference_asset_03 is image 5.png — use the face in this image as the model's face. Keep her hair (neat bun) and overall build. In the photo she wears a sports bra — replace with polished-casual office wear (blouse or fitted top) in the generated scene. Discard the outdoor mountain background and the shaker from image 5.png entirely. Only the face and hair carry through."
      }
    ],
    "NEGATIVE": "No thick, opaque, or milky shake. No gym, dumbbells, or athletic staging. No sports bra or workout clothing on the model. No outdoor or mountain background. No black supplement tubs. No desk clutter beyond the pack, shaker, and ceramic mug. No shelving, plants, stacks of files, or busy furniture visible in the background. No pure photography-studio cyclorama — background must read as a real office wall, not a blank colored backdrop. No smoothed AI skin. No text beyond the specified headline and subtitle."
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

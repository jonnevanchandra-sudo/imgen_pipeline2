```yaml
# Prompt Compiler v2.3 (8.1.1) — flat prose VisualPrompt with inline brand asset reproduction
# Source: SynthesisContract Trial_03 + ReferenceAssetManifest (Scene Assembly 5.2.5)
# Target: flat-prose generators (Midjourney / DALL-E / Flux)

VisualPrompt: "A clean, bright lifestyle advertising photograph of a Hong Kong office woman in her mid-to-late twenties taking her afternoon break at a near-empty desk — healthy and naturally attractive East Asian, in light polished-casual office wear, not gym clothes. She sits relaxed and quietly confident, lightly satisfied, holding or reaching for a transparent shaker of clear, pale-yellow lemon protein drink with a lemon slice inside; the drink is the undisputed hero of the image and must read as genuinely clear and translucent with light passing through it — never opaque, never milky. Her expression is calm and guilt-free, a small moment of self-care with no strain, no dieting anxiety, and no performance energy.

On the desk just beside the shaker, nearer the camera than her face, stands a CLEVER 'CLEAR PROTEIN' lemon-flavor pouch, facing the camera and clearly legible — white body, large dark-blue 'CLEAR PROTEIN' typography across the middle, bright yellow lemon-flavor accent band at the top, CLEVER logo, and functional benefit badges. The pouch and shaker both come from a reference image: this is reference_asset_01 — reproduce the pouch exactly: same white body, same blue 'CLEAR PROTEIN' typography, same yellow lemon band, same logo and badges, same shapes, colors, and proportions; reproduce the shaker and its CLEVER logo exactly, keep the drink clear and translucent; use only the product and bottle from this reference image and discard the male model and gym background entirely; do not redraw the packaging or logo from memory.

The CLEVER wordmark also appears in the frame alongside a legible 'Made in Japan / 日本製' cue: this is reference_asset_02 — reproduce the CLEVER logo exactly: same letterforms, same color, same proportions, do not redraw from memory; use image4's clean minimal sky-blue aesthetic as the target visual register for the background and overall feel; exclude the timing-clock graphic, any pricing, and the specific model from that reference image.

The desk surface holds only three objects: the CLEVER lemon pouch, the transparent shaker, and one small desk clock reading approximately 3:30. Nothing else is on the desk — no stationery, no food, no laptop, no other props. The surface is clean and minimal, like a curated photoshoot set, not a lived-in workspace. The background behind her is a clean, smooth, uncluttered sky-blue plane — no windows, no plants, no office furniture or shelving, no competing visual information of any kind. The desk and background together communicate intentionality and lightness; their emptiness is the point.

Light the scene with soft, bright, high-key daylight: the clear drink and pouch receive the cleanest, most direct light with a gentle specular glint on the glass and liquid so the drink looks crisp and refreshing; the woman is lit a touch softer, skin warm-neutral and never orange; the background is evenly lit as a smooth flat plane with no shadow pooling and no bright practical light sources behind the subject — nothing in the background outshines the product hero. Shoot at eye level, a near medium shot at desk distance so the viewer feels seated across from her at peer level, with an 85mm lens at f/4: the foreground pack and shaker are crisply sharp, the woman is sharp to gently soft by depth, and the already-clean background softens further into a smooth, even sky-blue plane with smooth progressive bokeh falloff and no flat uniform blur. Render the woman's skin with visible pores, fine lines, subtle tone variation, and natural asymmetry — a candid unposed expression, relaxed shoulders, no beauty filter, no airbrushing, no plastic or AI-perfect rendering. Render believable glass and liquid optics with light condensation on the shaker and a matte pouch surface contrasting against the glossy bottle body. The desk and background must remain genuinely clean and pristine — no shadows or imperfections in those areas. Avoid any thick, opaque, or milky shake; any gym, dumbbells, or muscular posing; any before-after or weighing scale; any background clutter, windows, plants, or office furniture behind the subject; any grape variant, multi-pack lineup, outdoor running, or timing-clock infographic; any smoothed AI skin; any invented marketing slogans or text paragraphs in the image."

ReferenceAssetManifest:
  - asset_id: asset_01
    filename: "image1.png"
    type: Brand-Bearing
    prompt_reference_id: reference_asset_01
    attach_to_api_call: true
    strictness: Exact
  - asset_id: asset_04
    filename: "image4.png"
    type: Brand-Bearing
    prompt_reference_id: reference_asset_02
    attach_to_api_call: true
    strictness: Exact
```

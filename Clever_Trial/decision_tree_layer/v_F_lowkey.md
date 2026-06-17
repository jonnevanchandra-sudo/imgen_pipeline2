# Visual Prompt — CLEVER Clear Protein (Decision Tree — v_F: low-key)

Source base: `Clever_Trial/decision_tree_layer/08_base.md`
Framework: `8.1.1 Prompt_Compiler.md` v2.3
Taxonomy change: `F_exposure` → `low_key`

## Variant

This is a copy of `08_base.md` with **F — Exposure/Shadow** swapped from `high_key` to `low_key`:

> low-key exposure, deep shadows, dramatic high-contrast mood

All other parameters carry from the base unchanged: style (clean lifestyle), angle (eye-level), distance (near medium shot), lighting direction (front), subject (office woman), camera specs (50mm, f/4), and all brand references.

**Exposure consequence — overall character:** The base is airy, bright, and lifestyle-polished. Low-key flips this entirely — the scene emerges from darkness, deep shadows dominate, and the office behind her falls into dramatic contrast. The sky-blue and white tones remain the underlying setting but are rendered dim and shadowed rather than bright and airy.

**Exposure consequence — clear drink:** A focused pool of directional light on the clear drink against a dark background makes the translucent pale-yellow liquid and the glass specular dramatically vivid. Low-key actually strengthens the clear-drink hero read — the product glows against darkness rather than sitting in a uniformly bright frame.

**Exposure consequence — pouch legibility:** The CLEVER pouch must still be legible. The directional light pool that hits the drink extends to the pouch beside it — both products are within the lit zone while everything else falls dark.

**Exposure consequence — opening line:** "bright" removed from the opening descriptor since low-key is by definition not a bright image.

```yaml
VisualPrompt: "A dramatic, low-key lifestyle advertising photograph of a Hong Kong office woman in her late twenties taking an afternoon break at her desk — healthy and natural-looking, in light, polished-casual office wear, not gym clothes. She sits relaxed and quietly confident, lightly satisfied, holding a transparent shaker bottle of clear, pale-yellow lemon protein drink with a lemon slice inside; the drink is the hero of the image and must read as genuinely clear and translucent with light passing through it, never opaque or milky. Her expression is calm and guilt-free — a small moment of light self-care, no strain, no dieting anxiety, no performance. The transparent shaker, its clear pale-yellow lemon drink, and the CLEVER logo on the bottle come from a reference image: this is reference_asset_01 — reproduce it exactly: same bottle, same clear translucent drink, same lemon cue, same logo shape, color and proportions; do not redraw from memory, and use only the product and bottle from that image while ignoring its gym background and any person in it. On the desk just beside the shaker, nearer the camera than her face, stands a CLEVER 'CLEAR PROTEIN' lemon-flavor pouch, facing the camera and clearly legible — white pouch body, large blue 'CLEAR PROTEIN' typography, yellow lemon-flavor accent strip and badges; this is also reference_asset_01 — reproduce the packaging exactly: same shapes, same colors, same proportions, do not redraw from memory. The CLEVER wordmark and a legible 'Made in Japan / 日本製' cue also appear in the frame: this is reference_asset_02 — reproduce the logo exactly: same letterforms, same color, same proportions, do not redraw from memory, and do not copy the timing-clock graphic, pricing, or specific model from that reference. The setting is a clean, minimal office desk — sky-blue and white in tone but rendered dark and dramatic, deep shadows falling across the desk surface and the office behind her, the scene emerging from darkness — with a subtle afternoon cue such as a small desk clock reading near 3:30 dimly visible in the surrounding shadow. Light it with low-key dramatic lighting: deep shadows and high contrast throughout; the clear drink and pouch sit within a focused pool of directional light — the pale-yellow lemon liquid catching a sharp specular glint and glowing with internal clarity against the surrounding darkness, the CLEVER pouch branding clearly legible within the same lit zone; the woman is lit with the same directional contrast, light sculpting her face while deep shadow falls to one side; the office behind her falls into deep, dark contrast so that nothing in the background competes with the hero products. Skin stays warm-neutral, never orange, with no studio flatness. Shoot at eye level, a near medium shot at desk distance so the viewer feels seated across from her, peer-level, with a 50mm lens at f/4: the foreground drink and pouch are crisply sharp, the woman is sharp to gently soft depending on her depth, and the dark office softens progressively with distance — smooth, gentle, depth-dependent bokeh and no flat uniform blur layer. Render real human skin with visible pores, fine lines, subtle tone variation and natural asymmetry, a candid unposed expression and relaxed shoulders; render believable glass and liquid optics with sharp specular highlights where the directional light catches the glass, light condensation on the shaker, and true fabric behavior on her clothing. Credibility takes priority over perfection — no plastic, over-smoothed, beauty-filtered or 'AI-perfect' look. Avoid any thick, opaque or milky shake, any gym, dumbbells or muscular posing, any black supplement tubs, any before-after or weighing-scale weight-loss framing, any junk food or snack clutter, any grape variant, multi-pack lineup, outdoor running scene or clock/timing infographic, any blown-out window behind her, and any invented marketing slogans or paragraphs of text."

ReferenceAssetManifest:
  - asset_id: asset_01
    filename: "reference_01.jpg"
    type: Brand-Bearing
    prompt_reference_id: reference_asset_01
    attach_to_api_call: true
    strictness: Exact
  - asset_id: asset_04
    filename: "reference_04.jpg"
    type: Brand-Bearing
    prompt_reference_id: reference_asset_02
    attach_to_api_call: true
    strictness: Exact
```

---

## Compile Notes

- **F swapped** — base's "soft, bright, high-key daylight... gentle fill that minimizes harsh shadow" replaced with `low_key`: "low-key dramatic lighting: deep shadows and high contrast... focused pool of directional light... office behind her falls into deep, dark contrast" per `taxonomy.json F_exposure.low_key`.
- **A / B / C / D / E unchanged** — subject, style, angle, distance, lighting direction all carry from base verbatim.
- **Opening line adjusted** — "A clean, bright lifestyle advertising photograph" → "A dramatic, low-key lifestyle advertising photograph." "Bright" removed since low-key is by definition dim overall.
- **Setting rebuilt** — "bright, clean, minimal office desk in light sky-blue and white tones, tidy and airy" → "clean, minimal office desk — sky-blue and white in tone but rendered dark and dramatic, deep shadows falling across the desk surface and the office behind her, the scene emerging from darkness." Same setting, opposite exposure character.
- **Lighting rebuilt** — "soft, bright, high-key daylight: the clear drink and pouch receive the cleanest, brightest light... the office behind her is exposed slightly down" → "low-key dramatic lighting: deep shadows and high contrast; the clear drink and pouch sit within a focused pool of directional light... the office behind her falls into deep, dark contrast."
- **Drink interaction called out** — "the pale-yellow lemon liquid catching a sharp specular glint and glowing with internal clarity against the surrounding darkness." Low-key with a clear translucent drink creates a striking visual: the liquid glows against dark surroundings.
- **Pouch legibility preserved** — "the CLEVER pouch branding clearly legible within the same lit zone" added explicitly since low-key could otherwise let the pouch fall into shadow.
- **Clock** — "small desk clock reading near 3:30" retained as "dimly visible in the surrounding shadow" — present as a subtle cue, not blown out by brightness as in the base.
- **ReferenceAssetManifest** — carried verbatim from base.

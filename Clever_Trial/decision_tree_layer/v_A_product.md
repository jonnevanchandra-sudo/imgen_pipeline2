# Visual Prompt — CLEVER Clear Protein (Decision Tree — v_A: product)

Source base: `Clever_Trial/decision_tree_layer/08_base.md`
Framework: `8.1.1 Prompt_Compiler.md` v2.3
Taxonomy change: `A_subject` → `product`

## Variant

This is a copy of `08_base.md` with **A — Subject** swapped from `human` to `product`:

> product-focused still life, clean object presentation, no human

The office woman is removed entirely. The CLEVER shaker bottle and CLEAR PROTEIN lemon pouch become the sole subjects, arranged on the desk. All brand references, reference assets, setting (office desk, sky-blue, 3:30 clock), camera specs (eye-level, 50mm, f/4, near medium shot), and lighting (soft high-key daylight) carry over unchanged from the base.

**Subject consequence:** All human-related language (expression, skin rendering, posture, outfit, human authenticity) is removed. Product authenticity (glass optics, liquid translucency, condensation, material surface) takes its place as the primary credibility requirement. A lemon wedge is added as a natural product cue supporting the lemon flavor.

```yaml
VisualPrompt: "A clean, bright lifestyle product photograph for an Instagram feed, square 1:1, photorealistic — product-focused still life, clean object presentation, no human. On a bright, clean, minimal office desk in light sky-blue and white tones, tidy and airy — a small calm island representing an afternoon workday moment — the CLEVER transparent shaker bottle and CLEAR PROTEIN lemon-flavor pouch are arranged together as the sole subjects, both facing the camera. The transparent shaker holds a clear, pale-yellow lemon protein drink with a lemon slice inside; the drink is the hero of the image and must read as genuinely clear and translucent with light passing through it, never opaque or milky. The transparent shaker, its clear pale-yellow lemon drink, and the CLEVER logo on the bottle come from a reference image: this is reference_asset_01 — reproduce it exactly: same bottle, same clear translucent drink, same lemon cue, same logo shape, color and proportions; do not redraw from memory, and use only the product and bottle from that image while ignoring its gym background and any person in it. Beside the shaker stands the CLEVER 'CLEAR PROTEIN' lemon-flavor pouch, facing the camera and clearly legible — white pouch body, large blue 'CLEAR PROTEIN' typography, yellow lemon-flavor accent strip and badges; this is also reference_asset_01 — reproduce the packaging exactly: same shapes, same colors, same proportions, do not redraw from memory. The CLEVER wordmark and a legible 'Made in Japan / 日本製' cue also appear in the frame: this is reference_asset_02 — reproduce the logo exactly: same letterforms, same color, same proportions, do not redraw from memory, and do not copy the timing-clock graphic, pricing, or specific model from that reference. A fresh lemon wedge and a subtle afternoon cue such as a small desk clock reading near 3:30 are placed casually beside the products as natural supporting elements. Light it with soft, bright, high-key daylight: the clear drink and pouch receive the cleanest, brightest light with a gentle specular glint on the glass and liquid surface; nothing in the frame outshines the hero products. Shoot at eye level, a near medium shot at desk distance with a 50mm lens at f/4: the drink and pouch are crisply sharp in the foreground, and the office desk surface and background soften progressively with distance — the desk clock stays semi-legible while the far wall falls softer — with smooth, gentle, depth-dependent bokeh and no flat uniform blur layer. The desk stays tidy and minimal, like a clean photoshoot surface. Render believable glass and liquid optics with light condensation on the shaker, a precise specular glint on the clear liquid, and real material surface quality on the pouch and desk. Credibility takes priority over perfection — no over-rendered or artificially perfect product CGI. Avoid any thick, opaque or milky shake, any gym, dumbbells or athletic context, any black supplement tubs, any before-after or weighing-scale framing, any junk food or snack clutter, any grape variant, multi-pack lineup, outdoor running scene or clock/timing infographic, any blown-out window, and any invented marketing slogans or paragraphs of text."

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

- **A swapped** — `human` → `product` per `taxonomy.json A_subject.product`: "product-focused still life, clean object presentation, no human."
- **B / C / D / E / F unchanged** — style, angle, distance, lighting, exposure all carry from base verbatim.
- **Human language removed** — expression, skin rendering, outfit, posture, human authenticity all removed. "Render real human skin..." replaced with "Render believable glass and liquid optics..."
- **Product arrangement** — "she holds the shaker" → "the shaker and pouch are arranged together as the sole subjects, both facing the camera." The spatial logic (shaker in foreground, pouch beside it) is preserved as a product composition.
- **Lemon wedge added** — natural product cue to fill the human's role as a scene anchor and support the lemon flavor read.
- **Desk changed** — base's "lived-in but tidy with natural reflections and everyday detail" → "tidy and minimal, like a clean photoshoot surface." Product still life favors a cleaner surface than a human lifestyle scene.
- **Prohibition updated** — "gym, dumbbells or muscular posing" → "gym, dumbbells or athletic context" since there's no human to pose.

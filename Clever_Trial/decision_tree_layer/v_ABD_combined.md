# Visual Prompt — CLEVER Clear Protein (Decision Tree — v_ABD: product + editorial + full shot)

Source base: `Clever_Trial/decision_tree_layer/08_base.md`
Framework: `8.1.1 Prompt_Compiler.md` v2.3
Taxonomy changes: `A_subject` → `product` + `B_style` → `editorial` + `D_distance` → `full_shot`

## Variant

This is a copy of `08_base.md` with **three taxonomy dimensions swapped simultaneously**:

| Layer | Base | This variant |
|---|---|---|
| A — Subject | human | **product** — no human, bottle + pouch as sole subjects |
| B — Style | clean lifestyle advertising | **editorial** — editorial magazine photography, styled and directional, high-fashion aesthetic |
| D — Distance | near medium shot | **full shot** — entire scene in frame |
| C / E / F | eye-level / soft front / high-key | unchanged |

**Combined consequence:** A product-focused editorial still life that shows the full desk environment — no human, shot at editorial magazine quality with directional precision, the camera pulled back to show the complete desk, surrounding office, and all product elements within a wide, deliberately composed frame.

**Interaction between A and D:** With no human subject, "full shot" no longer means full body — it means the full scene: the complete desk surface, the surrounding office space, the floor, and any ambient context. The bottle and pouch are arranged as the compositional anchors within this wider environment.

**Interaction between A and B:** Editorial style applied to a product still life pushes toward a high-fashion product campaign — think magazine double-page spread product placement rather than lifestyle advertising. Precise, graphic, deliberately lit and composed.

**Interaction between B and D:** Editorial + full shot together means the wider office environment is intentionally styled and precisely lit throughout — not just the desk, but the surrounding space is treated as a composed backdrop.

```yaml
VisualPrompt: "A crisp editorial magazine product photograph for an Instagram feed, square 1:1, photorealistic — editorial magazine photography, styled and directional, high-fashion aesthetic, product-focused still life with no human. The full scene is in frame: a deliberately styled, minimal office desk and the surrounding office environment — the complete desk surface, chair, floor, and surrounding walls — in light sky-blue and white, clean geometry, precise editorial placement, every element intentional. The CLEVER transparent shaker bottle and CLEAR PROTEIN lemon-flavor pouch are the compositional anchors of the scene, both positioned on the desk facing the camera. The transparent shaker holds a clear, pale-yellow lemon protein drink with a lemon slice inside; the drink is the hero and must read as genuinely clear and translucent with light passing through it, never opaque or milky. The transparent shaker, its clear pale-yellow lemon drink, and the CLEVER logo on the bottle come from a reference image: this is reference_asset_01 — reproduce it exactly: same bottle, same clear translucent drink, same lemon cue, same logo shape, color and proportions; do not redraw from memory, and use only the product and bottle from that image while ignoring its gym background and any person in it. Beside the shaker stands the CLEVER 'CLEAR PROTEIN' lemon-flavor pouch, facing the camera and clearly legible — white pouch body, large blue 'CLEAR PROTEIN' typography, yellow lemon-flavor accent strip and badges; this is also reference_asset_01 — reproduce the packaging exactly: same shapes, same colors, same proportions, do not redraw from memory. The CLEVER wordmark and a legible 'Made in Japan / 日本製' cue also appear in the frame: this is reference_asset_02 — reproduce the logo exactly: same letterforms, same color, same proportions, do not redraw from memory, and do not copy the timing-clock graphic, pricing, or specific model from that reference. A fresh lemon wedge and a small desk clock reading near 3:30 are placed as deliberate compositional elements beside the products — not casual props but precisely positioned editorial details. The broader office around them — chair, floor, walls — is styled with the same intentional minimalism: clean lines, airy sky-blue and white, nothing unstaged. Light it with directional, editorial-quality daylight: controlled and precise, with intentional contrast throughout the full scene; the clear drink and pouch receive the crispest, most precisely lit surface with a sharp specular glint on the glass and liquid; the wider office environment is lit with the same directional control, falling slightly dimmer than the hero products so nothing outshines them. Shoot at eye level, a full shot of the complete desk and surrounding office environment with a 50mm lens at f/4: the drink and pouch are crisply sharp in the foreground, and the broader office space — desk surface, chair, floor, walls — softens progressively with distance in smooth, intentional, depth-dependent bokeh with no flat uniform blur. The entire scene reads as a precisely composed, wide editorial frame. Render believable glass and liquid optics with a precise, high-quality specular and light condensation on the shaker; real material surface quality on the pouch, desk, chair, and floor. Credibility and editorial visual authority take priority. Avoid any thick, opaque or milky shake, any gym, dumbbells or athletic context, any black supplement tubs, any before-after or weighing-scale framing, any junk food or snack clutter, any grape variant, multi-pack lineup, outdoor running scene or clock/timing infographic, any blown-out window, and any invented marketing slogans or paragraphs of text."

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

- **Three dimensions swapped simultaneously** — A (`human` → `product`), B (`lifestyle` → `editorial`), D (`medium_shot` → `full_shot`). C / E / F unchanged from base.
- **A×D interaction resolved** — "full shot" with no human = full scene (complete desk, chair, floor, walls) rather than full body. The bottle and pouch serve as compositional anchors within the wider frame.
- **A×B interaction resolved** — editorial style on a product still life pushes toward a high-fashion product campaign register — precise, graphic, deliberately composed — rather than warm lifestyle editorial.
- **B×D interaction resolved** — editorial + full shot means the entire wider office environment is deliberately styled and lit, not just the desk surface. Every visible element is treated as intentional.
- **Human language fully removed** — expression, skin, posture, outfit, human authenticity all removed. Product material quality (glass optics, condensation, liquid translucency, surface precision) is the primary credibility requirement.
- **Lemon wedge + desk clock** — retained from v_A_product as natural product cues; reframed as "deliberately positioned editorial details" rather than casual props, consistent with the editorial register.
- **Lighting rebuilt** — base's "soft, bright, high-key daylight, gentle fill" → "directional, editorial-quality daylight: controlled and precise, with intentional contrast throughout the full scene."
- **Camera rebuilt** — "near medium shot at desk distance, peer-level" → "full shot of the complete desk and surrounding office environment." Eye-level and 50mm/f4 preserved exactly.
- **Closing** — "Credibility and editorial visual authority take priority."
- **ReferenceAssetManifest** — carried verbatim from base, unchanged.

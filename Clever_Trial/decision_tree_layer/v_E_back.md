# Visual Prompt — CLEVER Clear Protein (Decision Tree — v_E: backlighting)

Source base: `Clever_Trial/decision_tree_layer/08_base.md`
Framework: `8.1.1 Prompt_Compiler.md` v2.3
Taxonomy change: `E_lighting` → `back`

## Variant

This is a copy of `08_base.md` with **E — Lighting direction** swapped from `front` to `back`:

> backlighting, rim-lit silhouette, glowing edges

All other parameters carry from the base unchanged: style (clean lifestyle), angle (eye-level), distance (near medium shot), exposure (high-key), subject (office woman), camera specs (50mm, f/4), and all brand references.

**Lighting consequence — clear drink:** Backlighting is the single best lighting condition for a clear, translucent liquid. Light passing through the pale-yellow lemon drink from behind makes it glow luminously — this directly amplifies the hero product's key visual claim (clear, not opaque or milky). This is called out explicitly in the prompt.

**Lighting consequence — subject:** Her hair and shoulder edges are rim-lit with warm glowing light. Her face is in partial shadow from the front — soft ambient fill is required to keep her expression legible without killing the backlighting drama.

**Lighting consequence — pouch legibility:** The CLEVER pouch faces the camera but the front of it is away from the backlight source. Soft front fill must keep the CLEAR PROTEIN text and branding readable — this is flagged explicitly.

**Lighting consequence — background:** The light source sits behind her, so the office background is brighter than the base (window/light source behind). The background must be controlled — not blown out — so the rim-lit subject stays the hero.

```yaml
VisualPrompt: "A clean, bright lifestyle advertising photograph of a Hong Kong office woman in her late twenties taking an afternoon break at her desk — healthy and natural-looking, in light, polished-casual office wear, not gym clothes. She sits relaxed and quietly confident, lightly satisfied, holding a transparent shaker bottle of clear, pale-yellow lemon protein drink with a lemon slice inside; the drink is the hero of the image and must read as genuinely clear and translucent — backlit so the pale-yellow liquid glows luminously with transmitted light, never opaque or milky. Her expression is calm and guilt-free — a small moment of light self-care, no strain, no dieting anxiety, no performance. The transparent shaker, its clear pale-yellow lemon drink, and the CLEVER logo on the bottle come from a reference image: this is reference_asset_01 — reproduce it exactly: same bottle, same clear translucent drink, same lemon cue, same logo shape, color and proportions; do not redraw from memory, and use only the product and bottle from that image while ignoring its gym background and any person in it. On the desk just beside the shaker, nearer the camera than her face, stands a CLEVER 'CLEAR PROTEIN' lemon-flavor pouch, facing the camera and clearly legible — white pouch body, large blue 'CLEAR PROTEIN' typography, yellow lemon-flavor accent strip and badges; this is also reference_asset_01 — reproduce the packaging exactly: same shapes, same colors, same proportions, do not redraw from memory. The CLEVER wordmark and a legible 'Made in Japan / 日本製' cue also appear in the frame: this is reference_asset_02 — reproduce the logo exactly: same letterforms, same color, same proportions, do not redraw from memory, and do not copy the timing-clock graphic, pricing, or specific model from that reference. The setting is a bright, clean, minimal office desk in light sky-blue and white tones, tidy and airy — a small calm island in the workday — with a subtle afternoon cue such as a small desk clock reading near 3:30. Light it with backlighting — the primary light source positioned behind the woman and the products: the edges of her hair and shoulders glow with warm rim light; the clear drink is lit from behind, the pale-yellow lemon liquid glowing luminously with transmitted light — the backlighting makes the clear, translucent drink the most visually striking element in the frame. Provide soft ambient fill from the front to keep her expression and the CLEVER pouch branding clearly legible — fill is subtle, the rim light and the glowing clear liquid dominate. Skin stays warm-neutral, never orange, with no studio flatness. Shoot at eye level, a near medium shot at desk distance so the viewer feels seated across from her, peer-level, with a 50mm lens at f/4: the foreground drink and pouch are crisply sharp, the woman is sharp to gently soft depending on her depth, and the office softens progressively with distance — smooth, gentle, depth-dependent bokeh and no flat uniform blur layer. The light source behind her is controlled — not blown out, kept as a bright but defined backdrop so the rim-lit subject remains the hero. Render real human skin with visible pores, fine lines, subtle tone variation and natural asymmetry, a candid unposed expression and relaxed shoulders; render believable glass and liquid optics — the backlighting produces a glowing, luminous quality in the clear liquid, with light condensation on the shaker exterior visible in the front fill; true fabric behavior on her clothing with rim light catching the fabric edges. Credibility takes priority over perfection — no plastic, over-smoothed, beauty-filtered or 'AI-perfect' look. Avoid any thick, opaque or milky shake — the drink must glow with clear translucency under the backlight; avoid any gym, dumbbells or muscular posing, any black supplement tubs, any before-after or weighing-scale weight-loss framing, any junk food or snack clutter, any grape variant, multi-pack lineup, outdoor running scene or clock/timing infographic, any blown-out or overexposed background behind her, and any invented marketing slogans or paragraphs of text."

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

- **E swapped** — base's "soft, bright, high-key daylight... gentle fill that minimizes harsh shadow" replaced with `back` lighting: "backlighting — the primary light source positioned behind the woman and the products... rim light... glowing luminously with transmitted light" per `taxonomy.json E_lighting.back`.
- **A / B / C / D / F unchanged** — subject, style, angle, distance, exposure all carry from base verbatim.
- **Clear drink elevated** — "must read as genuinely clear and translucent with light passing through it" rewritten to "backlit so the pale-yellow liquid glows luminously with transmitted light." Backlighting is the optimal condition for the clear-protein hero claim and is called out explicitly.
- **Fill light added** — "Provide soft ambient fill from the front to keep her expression and the CLEVER pouch branding clearly legible." Without front fill, a backlit subject's face and the front-facing pouch label would be unreadably dark — this is a necessary addition, not a style choice.
- **Background control added** — "The light source behind her is controlled — not blown out, kept as a bright but defined backdrop." The base fences blown-out windows; backlit setups need an explicit version of this same fence.
- **Prohibition updated** — "any blown-out window behind her" (base) → "any blown-out or overexposed background behind her" since with backlighting the entire background plane is the light source risk.
- **Drink prohibition strengthened** — "Avoid any thick, opaque or milky shake" prefaced with "the drink must glow with clear translucency under the backlight" to reinforce the backlighting–transparency interaction.
- **ReferenceAssetManifest** — carried verbatim from base.

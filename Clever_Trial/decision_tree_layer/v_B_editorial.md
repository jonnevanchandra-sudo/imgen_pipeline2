# Visual Prompt — CLEVER Clear Protein (Decision Tree — v_B: editorial)

Source base: `Clever_Trial/decision_tree_layer/08_base.md`
Framework: `8.1.1 Prompt_Compiler.md` v2.3
Taxonomy change: `B_style` → `editorial`

## Variant

This is a copy of `08_base.md` with **B — Style** swapped from `clean lifestyle advertising` to `editorial`:

> editorial magazine photography, styled and directional, high-fashion aesthetic

The office woman, CLEVER products, setting, camera specs (eye-level, 50mm, f/4, near medium shot), and all brand references carry over unchanged. The style character — opening register, lighting treatment, the woman's expression, desk presentation, and overall tone — shifts from warm candid lifestyle to a precise, deliberate, editorial magazine aesthetic.

**Style consequence — lighting:** Base's "soft, bright, high-key daylight with gentle fill" shifts to directional, editorial-controlled light — intentional contrast, precise specular on the glass, more graphic than warm.

**Style consequence — the moment:** Base's "calm and guilt-free — a small moment of light self-care" becomes "poised and quietly self-assured — composed, the editorial equivalent of a private afternoon moment." The subject is still private and unperformed but with editorial composure rather than candid warmth.

**Style consequence — desk:** Base's "lived-in but tidy" becomes deliberately styled and precisely placed — editorial photography treats props as intentional compositional elements.

```yaml
VisualPrompt: "A crisp editorial magazine photograph for an Instagram feed, square 1:1, photorealistic — editorial magazine photography, styled and directional, high-fashion aesthetic. A Hong Kong office woman in her late twenties sits at her desk, healthy and composed, in light polished-casual office wear rendered with the precise intentionality of a styled editorial shoot — clean lines, deliberate presentation. She holds a transparent shaker bottle of clear, pale-yellow lemon protein drink with a lemon slice inside; the drink is the hero and must read as genuinely clear and translucent with light passing through it, never opaque or milky. Her expression is poised and quietly self-assured — composed and present, the editorial equivalent of a private afternoon moment, not a posed campaign smile. The transparent shaker, its clear pale-yellow lemon drink, and the CLEVER logo on the bottle come from a reference image: this is reference_asset_01 — reproduce it exactly: same bottle, same clear translucent drink, same lemon cue, same logo shape, color and proportions; do not redraw from memory, and use only the product and bottle from that image while ignoring its gym background and any person in it. On the desk just beside the shaker, nearer the camera than her face, stands a CLEVER 'CLEAR PROTEIN' lemon-flavor pouch, facing the camera and clearly legible — white pouch body, large blue 'CLEAR PROTEIN' typography, yellow lemon-flavor accent strip and badges; this is also reference_asset_01 — reproduce the packaging exactly: same shapes, same colors, same proportions, do not redraw from memory. The CLEVER wordmark and a legible 'Made in Japan / 日本製' cue also appear in the frame: this is reference_asset_02 — reproduce the logo exactly: same letterforms, same color, same proportions, do not redraw from memory, and do not copy the timing-clock graphic, pricing, or specific model from that reference. The setting is a deliberately styled, minimal office desk in light sky-blue and white — clean geometry, editorial placement, a carefully curated afternoon tableau — with a desk clock reading near 3:30 as a precise compositional element. Light it with directional, editorial-quality daylight: controlled and intentional, with graphic contrast; the clear drink and pouch receive the crispest, most precisely lit surface with a sharp specular glint on the glass and liquid; the woman is lit with the same directional control; the office behind her recedes into a clean, graphic backdrop. Skin stays warm-neutral, never orange, rendered with editorial precision and no studio flatness. Shoot at eye level, a near medium shot at desk distance, peer-level, with a 50mm lens at f/4: the foreground drink and pouch are crisply sharp, the woman rendered with editorial sharpness and precision, and the office softening progressively with distance — smooth, intentional bokeh, no flat uniform blur. Render skin with visible pores and natural tone variation but with the composed precision of editorial photography — no candid softness, no over-smoothed AI skin; render believable glass and liquid optics with a precise, high-quality specular; true fabric behavior on her clothing with deliberate editorial intentionality. Credibility and visual authority take priority over casual warmth. Avoid any thick, opaque or milky shake, any gym, dumbbells or muscular posing, any black supplement tubs, any before-after or weighing-scale weight-loss framing, any junk food or snack clutter, any grape variant, multi-pack lineup, outdoor running scene or clock/timing infographic, any blown-out window behind her, and any invented marketing slogans or paragraphs of text."

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

- **B swapped** — base's clean lifestyle advertising style → `editorial` per `taxonomy.json B_style.editorial`: "editorial magazine photography, styled and directional, high-fashion aesthetic."
- **A / C / D / E / F unchanged** — subject (human), angle, distance, camera specs, exposure all carry from base verbatim.
- **Opening rebuilt** — "A clean, bright lifestyle advertising photograph" → "A crisp editorial magazine photograph... styled and directional, high-fashion aesthetic."
- **Expression rebuilt** — "calm and guilt-free — a small moment of light self-care, no strain" → "poised and quietly self-assured — composed and present, the editorial equivalent of a private afternoon moment." Private and unperformed is preserved; warm/candid is replaced with composed/editorial.
- **Lighting rebuilt** — "soft, bright, high-key daylight... gentle fill that minimizes shadow" → "directional, editorial-quality daylight: controlled and intentional, with graphic contrast... precise specular glint." More directional and precise, less warm.
- **Desk rebuilt** — "lived-in but tidy with natural reflections and everyday detail" → "deliberately styled... clean geometry, editorial placement, a carefully curated afternoon tableau." Editorial photography treats every element as intentional.
- **Skin note updated** — natural texture preserved; "candid unposed expression" → "composed precision of editorial photography — no candid softness, no over-smoothed AI skin."
- **Closing tone** — "Credibility takes priority over perfection" → "Credibility and visual authority take priority over casual warmth."
- **Brand references and ReferenceAssetManifest** — carried verbatim from base, unchanged.

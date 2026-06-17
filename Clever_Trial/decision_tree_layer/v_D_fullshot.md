# Visual Prompt — CLEVER Clear Protein (Decision Tree — v_D: full shot)

Source base: `Clever_Trial/decision_tree_layer/08_base.md`
Framework: `8.1.1 Prompt_Compiler.md` v2.3
Taxonomy change: `D_distance` → `full_shot`

## Variant

This is a copy of `08_base.md` with **D — Distance** swapped from `medium_shot` (near medium, desk distance) to `full_shot`:

> full shot, entire subject in frame

The camera pulls back to show the woman's complete figure — from head to feet — along with the full desk, chair, and surrounding office floor and walls. All other parameters carry from the base unchanged: style (clean lifestyle), angle (eye-level), lighting (soft high-key daylight), camera lens (50mm, f/4), subject (office woman), and all brand references.

**Distance consequence — framing:** The full body, chair, desk legs, and the broader office space are all within the frame. The CLEVER bottle and pouch are still present on the desk but appear smaller within the wider environmental context.

**Distance consequence — product legibility:** At full-shot distance the bottle and pouch are less dominant than in the medium-shot base. The brand text (CLEAR PROTEIN, Made in Japan) must still be legible — positioned facing camera and placed at a distance where the wide shot allows them to still read clearly.

**Distance consequence — environment:** The office environment takes on greater compositional weight. The surrounding office — floor, walls, ceiling hints — become part of the image rather than soft background detail.

```yaml
VisualPrompt: "A clean, bright lifestyle advertising photograph for an Instagram feed, square 1:1, photorealistic. A Hong Kong office woman in her late twenties takes an afternoon break at her desk — healthy and natural-looking, in light, polished-casual office wear, not gym clothes. She sits relaxed and quietly confident, lightly satisfied, holding a transparent shaker bottle of clear, pale-yellow lemon protein drink with a lemon slice inside; the drink is the hero of the image and must read as genuinely clear and translucent with light passing through it, never opaque or milky. Her expression is calm and guilt-free — a small moment of light self-care, no strain, no dieting anxiety, no performance. The transparent shaker, its clear pale-yellow lemon drink, and the CLEVER logo on the bottle come from a reference image: this is reference_asset_01 — reproduce it exactly: same bottle, same clear translucent drink, same lemon cue, same logo shape, color and proportions; do not redraw from memory, and use only the product and bottle from that image while ignoring its gym background and any person in it. On the desk just beside the shaker stands a CLEVER 'CLEAR PROTEIN' lemon-flavor pouch, facing the camera and clearly legible — white pouch body, large blue 'CLEAR PROTEIN' typography, yellow lemon-flavor accent strip and badges; this is also reference_asset_01 — reproduce the packaging exactly: same shapes, same colors, same proportions, do not redraw from memory. The CLEVER wordmark and a legible 'Made in Japan / 日本製' cue also appear in the frame: this is reference_asset_02 — reproduce the logo exactly: same letterforms, same color, same proportions, do not redraw from memory, and do not copy the timing-clock graphic, pricing, or specific model from that reference. The setting is a bright, clean, minimal office — the full desk surface, the chair she sits in, her feet on the floor, and the surrounding office walls are all visible within the frame, in light sky-blue and white tones, tidy and airy — with a subtle afternoon cue such as a small desk clock on the desk reading near 3:30. Light it with soft, bright, high-key daylight: the clear drink and pouch receive the cleanest, brightest light with a gentle specular glint on the glass and liquid, the woman is lit a touch softer, and the broader office environment is exposed slightly down so that no window or background outshines the hero product; the office looks tidy, clean, and minimalistic. Skin stays warm-neutral, never orange, with no studio flatness. Shoot at eye level, a full shot of the woman's entire figure seated at her desk — her complete body from head to feet visible, the chair fully in frame, the desk surface and legs visible, the surrounding office floor and walls present — with a 50mm lens at f/4: the foreground drink and pouch are crisply sharp, the woman is sharp to gently soft depending on her depth, and the broader office environment softens progressively with distance — smooth, gentle, depth-dependent bokeh and no flat uniform blur layer. Render real human skin with visible pores, fine lines, subtle tone variation and natural asymmetry, a candid unposed expression, relaxed shoulders and natural body posture in the chair; render believable glass and liquid optics with light condensation on the shaker and true fabric behavior on her clothing and the chair. Credibility takes priority over perfection — no plastic, over-smoothed, beauty-filtered or 'AI-perfect' look. Avoid any thick, opaque or milky shake, any gym, dumbbells or muscular posing, any black supplement tubs, any before-after or weighing-scale weight-loss framing, any junk food or snack clutter, any grape variant, multi-pack lineup, outdoor running scene or clock/timing infographic, any blown-out window behind her, and any invented marketing slogans or paragraphs of text."

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

- **D swapped** — `medium_shot` ("near medium shot at desk distance... showing her upper body") → `full_shot` per `taxonomy.json D_distance.full_shot`: "full shot, entire subject in frame."
- **A / B / C / E / F unchanged** — subject (human), style, angle (eye-level), lighting, exposure all carry from base verbatim.
- **Camera description rebuilt** — "near medium shot at desk distance so the viewer feels seated across from her, peer-level, with a 50mm lens at f/4" → "full shot of the woman's entire figure seated at her desk — her complete body from head to feet visible, the chair fully in frame, the desk surface and legs visible, the surrounding office floor and walls present — with a 50mm lens at f/4." Eye-level and 50mm/f4 preserved exactly; only framing changes.
- **Setting expanded** — base's "bright, clean, minimal office desk" → "bright, clean, minimal office — the full desk surface, the chair she sits in, her feet on the floor, and the surrounding office walls are all visible within the frame." The environment becomes a visible element rather than a soft backdrop.
- **Skin/posture note updated** — "relaxed shoulders" → "relaxed shoulders and natural body posture in the chair" since the full body is now visible.
- **Product nearer/farther note** — "nearer the camera than her face" removed from pouch description; at full-shot distance the spatial hierarchy of face vs. product changes and the phrase no longer applies in the same way.
- **Brand references and ReferenceAssetManifest** — carried verbatim from base, unchanged.
- **Prohibitions** — carried verbatim from base.

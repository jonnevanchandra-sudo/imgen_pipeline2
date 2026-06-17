# Visual Prompt — Natural Protein Powder (Stage 8.1.1, flat YAML, Trial_03 — Style Variant v10 (emotionally raw))

Framework: `8.1.1 Prompt_Compiler.md` v2.3 (flat prose string, Luminance Hierarchy translation)
Input: SynthesisContract (Stage 7.1, Trial_03) — `Protein_Trial/Trial_03/07_SynthesisContract.md`
Style source: `taxonomy.json` → `B_style.emotionally_raw` (angle, distance retained from base)

## Style Variant (this version)

This is a copy of `08a_VisualPrompt.md` (base) with the **Style** swapped to `emotionally_raw`, keeping the base **Angle** (eye_level, frontal, straight-on) and **Distance** (medium_shot, waist-up, 85mm at f/4):

> emotionally raw, intimate documentary feel, unpolished authenticity

This replaces the base's `commercial_fashion`-adjacent style ("bright, crisp, high-end lifestyle-campaign... 8k and photorealistic"). The angle, distance, and camera specs (85mm/f4, frontal, eye-level, waist-up) carry over unchanged. All entity_01–04 Critical preservation attributes are retained (genuine unguarded savoring, glass at lips, gaze not on camera, real smoothie texture, matte kraft pouch with no legible text, recognizable real ingredients, natural skin texture).

**Style consequence — opening character:** "Bright, crisp, high-end lifestyle-campaign" and "8k" are removed entirely. The image is no longer a polished aspirational product. It is a documentary photograph — emotionally present, intimate, unpolished.

**Style consequence — lighting:** The base's "bright, soft, and broadly even, with gentle fill that minimizes harsh shadow — a crisp, polished, aspirational-lifestyle look" is replaced with warm, available, naturally uneven indoor daylight. No studio fill. Honest shadows are present and intentional.

**Style consequence — setting:** The base's "bright, clean, aspirational home kitchen" becomes a real, lived-in domestic space — the same kitchen, but not idealized. The counter has the small signs of daily use. The window light is real and directional, not perfectly even.

**Style consequence — the moment:** The base's "candid moment of genuine, unperformed enjoyment" deepens — emotionally raw means the private interior of the moment is more exposed, more visible. The gaze-on-glass and softened eyes carry more emotional weight at this register.

**Style consequence — imperfections:** The base "keeps small honest imperfections." Emotionally raw **embraces** them — they are not incidental, they are the point.

**LuminanceHierarchy note:** entity_01 (Subject) remains the sharpest, most present point in the frame — available light falls naturally on her face, making her the clearest point. entity_02/03/04 (glass, pouch, ingredients) lit naturally alongside her, a touch dimmer. entity_05 (Dimmest) — the kitchen — a warm, softened domestic presence behind her, not competing.

No `ReferenceAssetManifest` exists for this run — output is a single `VisualPrompt` YAML key, no manifest appended.

```yaml
VisualPrompt: "An emotionally raw, intimate documentary photograph for an Instagram feed, vertical 4:5 or square 1:1, photorealistic. A woman in her early thirties stands at her kitchen counter, photographed in a frontal, eye-level, waist-up medium shot on an 85mm lens at f/4 — straight-on, neutral camera height, balanced mid distance, natural undistorted proportions, showing her upper body and face. She wears a soft knit top, caught in the private moment just after a sip of a thick, creamy smoothie — her gaze stays down on the glass at her lips, eyes briefly closed or softened, an unguarded half-smile, the glass held close to her body at chest height. Even though the camera sits squarely in front of her, her attention never goes to the lens: this is a candid, emotionally present moment — fully private, fully unguarded, not a posed campaign smile. She is the sharpest, most present point in the frame, available light falling naturally on her face. The smoothie is visibly thick and blended from real food — a pale oat-vanilla tone with a faint berry swirl, texture clinging to the inside of the glass, rendered with honest, unpolished clarity. Beside her on the counter, within the same waist-up frame, sits an open matte kraft-paper protein powder pouch with a clean, minimal label that carries no legible text or logo, with a scoop dusted with powder resting against it, and nearby a peeled banana, a small scatter of rolled oats, a few fresh berries, and a split vanilla pod — each individually recognizable as real food, casually placed with the honest, unstaged disorder of a real morning, not a styled flat-lay. The glass, pouch, scoop, and ingredients are all rendered with honest clarity alongside her, lit naturally but a touch dimmer than her face. Behind her is a real, lived-in home kitchen — counters with the small signs of daily use, natural available daylight falling through a window — softened gently by the lens so it remains recognizable as a warm domestic space without competing with her; nothing in the background draws the eye from her. The lighting is warm, available, and natural — the intimate, slightly uneven quality of real indoor daylight, without studio fill or artificial polish — honest shadows present and intentional, soft highlights where the window light lands. The depth of field is Atmospheric: her face, the glass, the pack, and the ingredients are all sharp and clearly legible, while the kitchen behind softens progressively into warm, recognizable shapes without dissolving into heavy or flat bokeh. Her skin shows real texture — visible pores, natural tone variation, a relaxed asymmetric expression with nothing smoothed, beauty-filtered, or AI-perfect — the unpolished available light renders this texture with raw honesty, as it actually is. The scene embraces real imperfections: a light dusting of powder on the scoop, the banana freshly peeled, berries loose on the counter, the quiet unstaged disorder of a real morning. Unpolished authenticity and emotional presence over campaign polish. No gym equipment or athletic wear, no posed or to-camera smile, no performed delight, no legible text or logos anywhere in the frame, no competitor packaging, no artificial neon colors in the drink, no studio lighting or artificial fill, no styled flat-lay perfection, no airbrushed or over-smoothed skin, no heavy or uniform background blur, and no faces, pouch, or glass in the top 10% or bottom 20% of the frame."
```

---

## Compile Notes

- **~400 words**, single continuous prose string per the 8.1.1 output rule. Emphasis order: savoring moment + emotional presence first, drink, pack + ingredients, setting/light/authenticity, prohibitions last.
- **Style swapped** — base's "bright, crisp, high-end lifestyle-campaign photograph... 8k and photorealistic" replaced with `emotionally_raw`: "emotionally raw, intimate documentary photograph... photorealistic" per `taxonomy.json B_style.emotionally_raw`.
- **Angle and distance unchanged from base** — eye-level, frontal, waist-up medium shot, 85mm/f4 carried verbatim.
- **Opening line rebuilt** — "bright, crisp, high-end lifestyle-campaign" → "emotionally raw, intimate documentary." "8k" removed — does not fit documentary register.
- **Moment language deepened** — "candid moment of genuine, unperformed enjoyment" → "candid, emotionally present moment — fully private, fully unguarded." The emotional interiority of the base is foregrounded rather than softened by campaign polish.
- **Luminance anchor changed** — "She is the brightest, sharpest point in the frame" → "She is the sharpest, most present point in the frame, available light falling naturally on her face." "Brightest" removed since available light does not guarantee maximum brightness; "most present" preserves the hierarchy in documentary terms.
- **Lighting rebuilt** — "bright, soft, and broadly even, with gentle fill... crisp, polished, aspirational-lifestyle look" → "warm, available, and natural — the intimate, slightly uneven quality of real indoor daylight, without studio fill or artificial polish — honest shadows present and intentional." No fill. No evenness. Honest.
- **Kitchen backdrop rebuilt** — "bright, clean, aspirational home kitchen" → "real, lived-in home kitchen — counters with the small signs of daily use, natural available daylight falling through a window." Same space, stripped of idealization.
- **Counter items updated** — "casually but tidily placed" → "casually placed with the honest, unstaged disorder of a real morning." The tidiness of the base is a commercial instinct; emotionally raw replaces it with the disorder of an actual kitchen moment.
- **Imperfections reframed** — base "keeps small honest imperfections"; v10 "embraces real imperfections" — they are not incidental details but the point of the image.
- **Closing line replaced** — "Credibility in the moment and the materials, even within a crisp campaign-style frame" → "Unpolished authenticity and emotional presence over campaign polish."
- **Prohibition updated** — "no clinical studio look" replaced with "no studio lighting or artificial fill" (stronger, more specific to this style's core requirement).
- **DOF unchanged** — 85mm/f4 Atmospheric from Stage 6 carried verbatim.
- **Skin rendering** — natural texture clause preserved and reframed: "the unpolished available light renders this texture with raw honesty, as it actually is."
- **Pose variation:** not applicable — single subject.

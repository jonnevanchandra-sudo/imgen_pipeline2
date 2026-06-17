# Visual Prompt — Natural Protein Powder (Stage 8.1.1, flat YAML, Trial_03 — Style Variant v9 (medium-key))

Framework: `8.1.1 Prompt_Compiler.md` v2.3 (flat prose string, Luminance Hierarchy translation)
Input: SynthesisContract (Stage 7.1, Trial_03) — `Protein_Trial/Trial_03/07_SynthesisContract.md`
Style source: `taxonomy.json` → `F_exposure.medium_key` (base style, angle, distance, lighting direction retained)

## Style Variant (this version)

This is a copy of `08a_VisualPrompt.md` (base) with the **Exposure/Shadow** swapped, keeping the base **Style** (high-end lifestyle-campaign, home kitchen), **Angle** (eye_level), **Distance** (medium_shot, waist-up, 85mm at f/4), and **Lighting direction** (front, even — unchanged from base):

> medium exposure, balanced lighting, properly exposed subjects, clear midtones, dark background contrast, sharp studio lighting, photorealistic

This replaces the base's high-key character ("bright, soft, and broadly even... crisp, polished, aspirational-lifestyle look"). All other parameters carry over from the base unchanged: angle, distance, camera specs, home kitchen setting, and all entity_01–04 Critical preservation attributes.

**Exposure consequence — subject:** The subject is properly and cleanly exposed with clear midtones — no overblown highlights, no crushed shadows. The look shifts from the base's airy lifestyle brightness to a grounded, commercial studio quality.

**Exposure consequence — background:** Medium-key introduces dark background contrast — the kitchen behind her is notably darker than the subject, throwing her and the counter items into sharper relief. The base's "bright, clean, aspirational home kitchen" becomes a moody, receding kitchen backdrop. This naturally satisfies "nothing in the background outshines her" even more strongly than the base.

**Exposure consequence — opening line:** "bright" and "8k" removed from the opening descriptor; "photorealistic" is carried directly from the taxonomy phrase and already implies the rendering quality.

**LuminanceHierarchy note:** The contrast between entity_01 (subject, properly lit) and entity_05 (kitchen, darker background) is sharper in medium-key than in the base. entity_02/03/04 (glass, pouch, ingredients) remain clearly lit alongside her, a touch dimmer than her face.

No `ReferenceAssetManifest` exists for this run — output is a single `VisualPrompt` YAML key, no manifest appended.

```yaml
VisualPrompt: "A crisp, high-end lifestyle-campaign photograph for an Instagram feed, vertical 4:5 or square 1:1, photorealistic. A woman in her early thirties stands at her kitchen counter, photographed in a frontal, eye-level, waist-up medium shot on an 85mm lens at f/4 — straight-on, neutral camera height, balanced mid distance, natural undistorted proportions, showing her upper body and face. She wears a soft knit top, caught in the private moment just after a sip of a thick, creamy smoothie — her gaze stays down on the glass at her lips, eyes briefly closed or softened, an unguarded half-smile, the glass held close to her body at chest height. Even though the camera sits squarely in front of her, her attention never goes to the lens: this is a candid moment of genuine, unperformed enjoyment, not a posed campaign smile. She is the brightest, sharpest point in the frame. The smoothie is visibly thick and blended from real food — a pale oat-vanilla tone with a faint berry swirl, texture clinging to the inside of the glass, rendered with crisp, high-clarity detail. Beside her on the counter, within the same waist-up frame, sits an open matte kraft-paper protein powder pouch with a clean, minimal label that carries no legible text or logo, with a scoop dusted with powder resting against it, and nearby a peeled banana, a small scatter of rolled oats, a few fresh berries, and a split vanilla pod — each individually recognizable as real food, casually but tidily placed, not a styled flat-lay. The glass, pouch, scoop, and ingredients are all rendered crisp and sharp alongside her, lit clearly but a touch dimmer than her face. Behind her is a clean home kitchen — tidy counters and cabinetry — receding into darker contrast behind the subject, with the background falling noticeably dimmer than her and the counter items, throwing her into sharp relief; nothing in the background outshines her. The lighting is medium-key — balanced, properly exposed on the subject with clear midtones, sharp studio-quality illumination, no overblown highlights, no crushed shadows, the background held in darker contrast for a grounded, commercial, photorealistic quality. The depth of field is Atmospheric: her face, the glass, the pack, and the ingredients are all sharp and clearly legible, while the darker kitchen behind softens progressively into recognizable but receding shapes without dissolving into heavy or flat bokeh. Her skin shows real texture — visible pores, natural tone variation, a relaxed asymmetric expression with nothing smoothed, beauty-filtered, or AI-perfect — the clean, balanced midtone light rendering this texture clearly and without flattery, even as the rest of the image reads polished and commercial. The scene keeps small honest imperfections: a light dusting of powder on the scoop, the banana freshly peeled, berries loose on the counter. Credibility in the moment and the materials, even within a crisp campaign-style frame. No gym equipment or athletic wear, no posed or to-camera smile, no performed delight, no legible text or logos anywhere in the frame, no competitor packaging, no artificial neon colors in the drink, no clinical studio look, no styled flat-lay perfection, no airbrushed or over-smoothed skin, no heavy or uniform background blur, and no faces, pouch, or glass in the top 10% or bottom 20% of the frame."
```

---

## Compile Notes

- **~390 words**, single continuous prose string per the 8.1.1 output rule. Emphasis order: savoring moment + gaze first, drink, pack + ingredients, setting/light/camera/authenticity, prohibitions last.
- **Exposure swapped** — base's "bright, soft, and broadly even, with gentle fill that minimizes harsh shadow — a crisp, polished, aspirational-lifestyle look" replaced with `medium_key`: "balanced, properly exposed on the subject with clear midtones, sharp studio-quality illumination... the background held in darker contrast for a grounded, commercial, photorealistic quality" per `taxonomy.json F_exposure.medium_key`.
- **Style, angle, distance, lighting direction unchanged from base** — high-end lifestyle-campaign, home kitchen, eye-level, waist-up medium shot, 85mm/f4 all carried verbatim.
- **Opening line adjusted** — "bright" and "8k" removed; "photorealistic" replaces them, sourced directly from the taxonomy phrase. The medium-key look is grounded and commercial, not airy or high-brightness.
- **Kitchen backdrop updated** — "bright, clean, aspirational home kitchen — tidy counters and cabinetry, a window letting in even daylight" → "clean home kitchen — tidy counters and cabinetry — receding into darker contrast behind the subject." The "aspirational" descriptor is removed; medium-key's dark background contrast changes the backdrop's character from airy to dramatic-commercial.
- **LuminanceHierarchy translated** — entity_01 (Brightest): "the brightest, sharpest point in the frame"; entity_02/03/04 (Mid): "lit clearly but a touch dimmer than her face"; entity_05 (Dimmest): kitchen "falling noticeably dimmer... throwing her into sharp relief" — contrast is stronger than in the base.
- **Skin rendering** — natural texture clause preserved; medium-key framing: "the clean, balanced midtone light rendering this texture clearly and without flattery."
- **Pose variation:** not applicable — single subject.

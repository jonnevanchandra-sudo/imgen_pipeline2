# Visual Prompt — Natural Protein Powder (Stage 8.1.1, flat YAML, Trial_03 — Style Variant v8 (side lighting))

Framework: `8.1.1 Prompt_Compiler.md` v2.3 (flat prose string, Luminance Hierarchy translation)
Input: SynthesisContract (Stage 7.1, Trial_03) — `Protein_Trial/Trial_03/07_SynthesisContract.md`
Style source: `taxonomy.json` → `E_lighting.side` (base style, angle, distance retained)

## Style Variant (this version)

This is a copy of `08a_VisualPrompt.md` (base) with the **Directional Lighting** swapped, keeping the base **Style** (high-end lifestyle-campaign, home kitchen), **Angle** (eye_level), and **Distance** (medium_shot, waist-up, 85mm at f/4):

> side lighting, directional chiaroscuro, sculpted form

This replaces the base's even, soft, fill-minimized lighting ("bright, soft, and broadly even, with gentle fill that minimizes harsh shadow"). All other parameters carry over from the base unchanged: angle, distance, camera specs, home kitchen setting, and all entity_01–04 Critical preservation attributes.

**Lighting consequence — subject:** One side of her face and body is brightly lit; the other falls into sculpted shadow. The chiaroscuro contrast gives her face and form depth and dimension not present in the base's flat-fill approach. Her lit side remains the brightest point in the frame.

**Lighting consequence — setting:** The kitchen window becomes the directional source, positioned to one side. The lit side of the kitchen catches directional clarity; the far side recedes into softer shadow. The "bright, clean" kitchen of the base becomes a "clean, aspirational kitchen with directional light from one side." The overall intro is adjusted accordingly — "bright" removed from the opening line since chiaroscuro introduces intentional shadow.

**Lighting consequence — product items:** The glass, pouch, scoop, and ingredients on the counter catch the same directional light — one side lit, one side in shadow — which adds physical credibility and dimensionality to the surface materials.

**LuminanceHierarchy note:** entity_01 (Brightest) — her lit side — remains the brightest point. entity_02/03/04 (Mid) — glass, pouch, ingredients — lit clearly from the same source, a touch dimmer than her face. entity_05 (Dimmest) — kitchen backdrop — the shadow side recedes, reinforcing separation.

No `ReferenceAssetManifest` exists for this run — output is a single `VisualPrompt` YAML key, no manifest appended.

```yaml
VisualPrompt: "A crisp, high-end lifestyle-campaign photograph for an Instagram feed, vertical 4:5 or square 1:1, 8k and photorealistic. A woman in her early thirties stands at her kitchen counter, photographed in a frontal, eye-level, waist-up medium shot on an 85mm lens at f/4 — straight-on, neutral camera height, balanced mid distance, natural undistorted proportions, showing her upper body and face. She wears a soft knit top, caught in the private moment just after a sip of a thick, creamy smoothie — her gaze stays down on the glass at her lips, eyes briefly closed or softened, an unguarded half-smile, the glass held close to her body at chest height. Even though the camera sits squarely in front of her, her attention never goes to the lens: this is a candid moment of genuine, unperformed enjoyment, not a posed campaign smile. She is the brightest, sharpest point in the frame — her lit side catching the directional light with clarity while the shadow side falls into sculpted contrast that gives her face and form real depth and dimension. The smoothie is visibly thick and blended from real food — a pale oat-vanilla tone with a faint berry swirl, texture clinging to the inside of the glass, the directional light catching the glass surface and interior texture with crisp, high-clarity detail. Beside her on the counter, within the same waist-up frame, sits an open matte kraft-paper protein powder pouch with a clean, minimal label that carries no legible text or logo, with a scoop dusted with powder resting against it, and nearby a peeled banana, a small scatter of rolled oats, a few fresh berries, and a split vanilla pod — each individually recognizable as real food, casually but tidily placed, not a styled flat-lay, each catching the same directional light with one side lit and the other in shadow. The glass, pouch, scoop, and ingredients are all rendered crisp and sharp alongside her, lit clearly but a touch dimmer than her face. Behind her is a clean, aspirational home kitchen — tidy counters and cabinetry, a window to one side as the directional light source — with the lit side catching directional warmth and the far side receding into softer shadow, gently softened by the lens so it remains recognizable without competing with her or the counter items; nothing in the background outshines her. The lighting is directional side lighting — chiaroscuro contrast sculpting her face and form, a strong lit side and a shadow side that gives depth without losing legibility; the light source is consistent across the entire scene, falling from one direction across her, the counter items, and the kitchen behind. The depth of field is Atmospheric: her face, the glass, the pack, and the ingredients are all sharp and clearly legible, while the kitchen behind softens progressively into recognizable shapes without dissolving into heavy or flat bokeh. Her skin shows real texture — visible pores, natural tone variation, the directional light sculpting the lit and shadow planes of her face with depth and realism — nothing smoothed, beauty-filtered, or AI-perfect — even as the rest of the image reads polished and high-end. The scene keeps small honest imperfections: a light dusting of powder on the scoop, the banana freshly peeled, berries loose on the counter. Credibility in the moment and the materials, even within a crisp campaign-style frame. No gym equipment or athletic wear, no posed or to-camera smile, no performed delight, no legible text or logos anywhere in the frame, no competitor packaging, no artificial neon colors in the drink, no clinical studio look, no styled flat-lay perfection, no airbrushed or over-smoothed skin, no heavy or uniform background blur, and no faces, pouch, or glass in the top 10% or bottom 20% of the frame."
```

---

## Compile Notes

- **~410 words**, single continuous prose string per the 8.1.1 output rule. Emphasis order: savoring moment + gaze first, drink, pack + ingredients, setting/light/camera/authenticity, prohibitions last.
- **Lighting swapped** — base's "bright, soft, and broadly even, with gentle fill that minimizes harsh shadow" replaced with `side` lighting: "directional side lighting — chiaroscuro contrast sculpting her face and form, a strong lit side and a shadow side" per `taxonomy.json E_lighting.side`.
- **Style, angle, distance unchanged from base** — high-end lifestyle-campaign, home kitchen, eye-level, waist-up medium shot, 85mm/f4 all carried verbatim.
- **Opening line adjusted** — "bright" removed from "A bright, crisp, high-end lifestyle-campaign photograph" since chiaroscuro introduces intentional shadow that contradicts a blanket "bright" descriptor.
- **Kitchen backdrop updated** — "bright, clean, aspirational home kitchen — tidy counters and cabinetry, a window letting in even daylight" → "clean, aspirational home kitchen — tidy counters and cabinetry, a window to one side as the directional light source — with the lit side catching directional warmth and the far side receding into softer shadow."
- **LuminanceHierarchy translated** — entity_01 (Brightest): "her lit side catching the directional light with clarity"; entity_02/03/04 (Mid): "lit clearly but a touch dimmer than her face"; entity_05 (Dimmest): kitchen "far side receding into softer shadow."
- **Skin rendering** — natural texture clause preserved; chiaroscuro reinforces it: "the directional light sculpting the lit and shadow planes of her face with depth and realism."
- **Product items updated** — each counter item "catching the same directional light with one side lit and the other in shadow" — consistent light source across all scene elements.
- **Pose variation:** not applicable — single subject.

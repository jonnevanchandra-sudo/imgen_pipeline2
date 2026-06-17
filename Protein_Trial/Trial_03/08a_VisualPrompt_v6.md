# Visual Prompt — Natural Protein Powder (Stage 8.1.1, flat YAML, Trial_03 — Style Variant v6 (high angle))

Framework: `8.1.1 Prompt_Compiler.md` v2.3 (flat prose string, Luminance Hierarchy translation)
Input: SynthesisContract (Stage 7.1, Trial_03) — `Protein_Trial/Trial_03/07_SynthesisContract.md`
Style source: `taxonomy.json` → `C_angle.high_angle` (base style retained)

## Style Variant (this version)

This is a copy of `08a_VisualPrompt.md` (base) with the **Angle** portion swapped, keeping the base **Style** (high-end lifestyle-campaign, home kitchen) and **Distance** (medium_shot, waist-up, 85mm at f/4):

> high-angle shot looking down on the subject

This replaces the base's `eye_level` angle ("frontal, eye-level, waist-up medium shot... straight-on, neutral camera height"). All other parameters carry over from the base unchanged: crisp high-end lifestyle style, 85mm/f4, home kitchen setting, and all entity_01–04 Critical preservation attributes (genuine unguarded savoring, glass at lips, real smoothie texture, matte kraft pouch with no legible text, recognizable real ingredients, natural skin texture).

**Angle consequence — background:** From a high angle, the camera tilts down toward the subject. The kitchen behind her gives way to a more overhead view of the counter surface spreading around and below her, with cabinetry visible from above rather than straight-on. A window or kitchen light source may still appear at the far edge of the scene.

**Angle consequence — gaze:** Her gaze staying down on the glass is even more natural from above — the camera and her gaze point in the same downward direction, reinforcing the candid, private quality of the moment.

**LuminanceHierarchy note:** entity_01 (Brightest) remains her face — the high angle means even daylight falls more directly onto her from above. entity_02/03/04 (Mid) on the counter remain legible. entity_05 (Dimmest) — the kitchen surface around and below her — softens with distance.

No `ReferenceAssetManifest` exists for this run — output is a single `VisualPrompt` YAML key, no manifest appended.

```yaml
VisualPrompt: "A bright, crisp, high-end lifestyle-campaign photograph for an Instagram feed, vertical 4:5 or square 1:1, 8k and photorealistic. A woman in her early thirties stands at her kitchen counter, photographed from a high angle on an 85mm lens at f/4 — camera elevated above her and tilted downward, looking at her from above, natural proportions with gentle foreshortening, showing her upper body and face from a slightly overhead perspective. She wears a soft knit top, caught in the private moment just after a sip of a thick, creamy smoothie — her gaze stays down on the glass at her lips, eyes briefly closed or softened, an unguarded half-smile, the glass held close to her body at chest height. The camera looks down from above her, but her attention never goes to the lens: this is a candid moment of genuine, unperformed enjoyment, not a posed campaign smile. She is the brightest, sharpest point in the frame. The smoothie is visibly thick and blended from real food — a pale oat-vanilla tone with a faint berry swirl, texture clinging to the inside of the glass, rendered with crisp, high-clarity detail. Beside her on the counter, within the same frame, sits an open matte kraft-paper protein powder pouch with a clean, minimal label that carries no legible text or logo, with a scoop dusted with powder resting against it, and nearby a peeled banana, a small scatter of rolled oats, a few fresh berries, and a split vanilla pod — each individually recognizable as real food, casually but tidily placed, not a styled flat-lay. The glass, pouch, scoop, and ingredients are all rendered crisp and sharp alongside her, lit clearly but a touch dimmer than her face. Around and below her stretches the bright, clean, aspirational home kitchen — tidy counter surface and cabinetry seen from above, a window at the far edge of the scene letting in even daylight — softened gently by the lens so it remains recognizable as a bright, polished space without competing with her or the counter items; nothing in the background outshines her. The lighting throughout is bright, soft, and broadly even, with gentle fill that minimizes harsh shadow — a crisp, polished, aspirational-lifestyle look. The depth of field is Atmospheric: her face, the glass, the pack, and the ingredients are all sharp and clearly legible, while the kitchen surface below softens progressively into soft, bright, recognizable shapes without dissolving into heavy or flat bokeh. Her skin shows real texture — visible pores, natural tone variation, a relaxed asymmetric expression with nothing smoothed, beauty-filtered, or AI-perfect — even as the rest of the image reads polished and high-end. The scene keeps small honest imperfections: a light dusting of powder on the scoop, the banana freshly peeled, berries loose on the counter. Credibility in the moment and the materials, even within a crisp campaign-style frame. No gym equipment or athletic wear, no posed or to-camera smile, no performed delight, no legible text or logos anywhere in the frame, no competitor packaging, no artificial neon colors in the drink, no clinical studio look, no styled flat-lay perfection, no airbrushed or over-smoothed skin, and no heavy or uniform background blur."
```

---

## Compile Notes

- **~390 words**, single continuous prose string per the 8.1.1 output rule. Emphasis order follows CommunicationAllocation: savoring moment + gaze-on-glass first, drink, then pack + ingredient evidence, then setting/light/camera/authenticity, prohibitions last.
- **Angle swapped** — `eye_level` ("frontal, eye-level, waist-up medium shot... straight-on, neutral camera height") replaced with `high_angle` ("camera elevated above her and tilted downward... slightly overhead perspective with gentle foreshortening") per `taxonomy.json C_angle.high_angle`.
- **Style unchanged from base** — high-end lifestyle-campaign, home kitchen, bright/polished/8k carried verbatim.
- **Distance unchanged from base** — waist-up framing retained; "within the same frame" replaces "within the same waist-up frame" since the high angle changes the spatial logic of that phrase.
- **Background updated** — entity_05 shifts from "behind her... cabinetry, window" to "around and below her... counter surface and cabinetry seen from above" since a high angle reveals the ground plane rather than the wall behind.
- **Gaze line updated** — "camera sits squarely in front of her" rewritten to "camera looks down from above her" — same candor logic, correct geometry.
- **"No faces/pouch/glass in top 10% or bottom 20%" prohibition** — removed; that spatial rule is written for an eye-level medium shot and does not apply when the camera angle shifts the entire compositional geometry.
- **LuminanceHierarchy** — entity_01 (Brightest): "the brightest, sharpest point in the frame"; entity_02/03/04 (Mid): "lit clearly but a touch dimmer than her face"; entity_05 (Dimmest): kitchen surface "softened gently... without competing with her."
- **Skin rendering** — natural texture clause preserved per the Human Subject Rendering Requirement.
- **Pose variation:** not applicable — single subject.

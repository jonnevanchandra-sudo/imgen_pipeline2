# Visual Prompt — Natural Protein Powder (Stage 8.1.1, flat YAML, Trial_03 — Style Variant v7 (close-up))

Framework: `8.1.1 Prompt_Compiler.md` v2.3 (flat prose string, Luminance Hierarchy translation)
Input: SynthesisContract (Stage 7.1, Trial_03) — `Protein_Trial/Trial_03/07_SynthesisContract.md`
Style source: `taxonomy.json` → `D_distance.close_up` (base style retained)

## Style Variant (this version)

This is a copy of `08a_VisualPrompt.md` (base) with the **Distance** portion swapped, keeping the base **Style** (high-end lifestyle-campaign, home kitchen) and **Angle** (eye_level, frontal, straight-on, 85mm at f/4):

> close-up shot, tight on the subject

This replaces the base's `medium_shot` distance ("waist-up medium shot... balanced mid distance, showing her upper body and face"). All other parameters carry over from the base unchanged: crisp high-end lifestyle style, eye-level frontal angle, 85mm/f4, home kitchen setting, and all entity_01–04 Critical preservation attributes (genuine unguarded savoring, glass at lips, real smoothie texture, matte kraft pouch with no legible text, recognizable real ingredients, natural skin texture).

**Distance consequence — framing:** Close-up tightens the frame to her face and the glass at her lips — roughly chin to crown, with the glass filling the lower portion of the frame. The protein powder pouch, scoop, and ingredient spread fall outside the tight crop; only the very top of the pouch is glimpsed at the bottom edge.

**Distance consequence — product legibility:** The smoothie and glass become the primary product-bearing element in frame. The thick, real-food texture of the smoothie visible against the glass carries the evidential weight that the full ingredient spread held at medium distance.

**Distance consequence — skin rendering:** The close-up makes natural skin texture the dominant visual surface of the frame. The Human Subject Rendering Requirement (no airbrushed or beauty-filtered skin) is more critical here than at medium distance.

**LuminanceHierarchy note:** entity_01 (Brightest) — her face — fills more of the frame and becomes even more dominant. entity_02 (glass/smoothie) is sharp at the bottom. entity_03/04 (pouch/ingredients) are outside or barely at the frame's edge. entity_05 (Dimmest) — kitchen backdrop — softens behind her as in the base.

No `ReferenceAssetManifest` exists for this run — output is a single `VisualPrompt` YAML key, no manifest appended.

```yaml
VisualPrompt: "A bright, crisp, high-end lifestyle-campaign photograph for an Instagram feed, vertical 4:5 or square 1:1, 8k and photorealistic. A woman in her early thirties stands at her kitchen counter, photographed in a frontal, eye-level, close-up shot on an 85mm lens at f/4 — straight-on, neutral camera height, tight on her face and the glass at her lips, framing from just below chin height to just above the crown of her head, natural undistorted proportions. She wears a soft knit top visible at the very top of the chest, caught in the private moment just after a sip of a thick, creamy smoothie — her gaze stays down on the glass at her lips, eyes briefly closed or softened, an unguarded half-smile, the glass held close to her body and filling the lower portion of the tight frame. Even though the camera sits squarely in front of her, her attention never goes to the lens: this is a candid moment of genuine, unperformed enjoyment, not a posed campaign smile. She is the brightest, sharpest point in the frame. The smoothie is visibly thick and blended from real food — a pale oat-vanilla tone with a faint berry swirl, texture clinging to the inside of the glass, the close framing making the glass's real-food texture the dominant product detail in the lower half of the frame, rendered with crisp, high-clarity detail. At the very bottom edge of the frame, just barely glimpsed, the top of a matte kraft-paper protein powder pouch hints at the scene beyond — minimal label, no legible text or logo. The glass is rendered crisp and sharp in her hands, lit clearly but a touch dimmer than her face. Behind her is a bright, clean, aspirational home kitchen — tidy cabinetry, a window letting in even daylight — softened gently by the lens so it remains recognizable as a bright, polished space without competing with her; nothing in the background outshines her. The lighting throughout is bright, soft, and broadly even, with gentle fill that minimizes harsh shadow — a crisp, polished, aspirational-lifestyle look. The depth of field is Atmospheric: her face and the glass are sharp and clearly legible, while the kitchen behind softens progressively into soft, bright, recognizable shapes without dissolving into heavy or flat bokeh. Her skin shows real texture — visible pores, natural tone variation, a relaxed asymmetric expression with nothing smoothed, beauty-filtered, or AI-perfect — the tight close-up makes this natural texture the dominant visual surface of the frame; even as the rest of the image reads polished and high-end. The scene keeps small honest imperfections: the smoothie's real-food texture visible against the glass, the asymmetry of her half-smile. Credibility in the moment and the materials, even within a crisp campaign-style frame. No gym equipment or athletic wear, no posed or to-camera smile, no performed delight, no legible text or logos anywhere in the frame, no competitor packaging, no artificial neon colors in the drink, no clinical studio look, no airbrushed or over-smoothed skin, and no heavy or uniform background blur."
```

---

## Compile Notes

- **~360 words**, single continuous prose string per the 8.1.1 output rule. Emphasis order follows CommunicationAllocation: savoring moment + gaze-on-glass first, drink (now the primary product evidence at close-up), then partial pouch glimpse, then setting/light/camera/authenticity, prohibitions last.
- **Distance swapped** — `medium_shot` ("waist-up medium shot... balanced mid distance, showing her upper body and face") replaced with `close_up` ("close-up shot... tight on her face and the glass at her lips, framing from just below chin height to just above the crown of her head") per `taxonomy.json D_distance.close_up`.
- **Style unchanged from base** — high-end lifestyle-campaign, home kitchen, bright/polished/8k carried verbatim.
- **Angle unchanged from base** — eye-level, frontal, straight-on retained verbatim.
- **Entity visibility updated** — entity_03/04 (pouch + ingredients) are outside the tight frame; entity_02 (pouch) reduced to a bottom-edge glimpse; the glass/smoothie texture steps up to carry the evidential product weight.
- **"No faces/pouch/glass in top 10% or bottom 20%" prohibition** — removed; this spatial rule is written for a waist-up medium shot and does not apply at close-up distance where the face fills most of the frame by design.
- **"No styled flat-lay" prohibition** — removed; the counter is out of frame and the flat-lay risk does not exist at close-up distance.
- **Skin rendering emphasis elevated** — "the tight close-up makes this natural texture the dominant visual surface of the frame" added explicitly, per the Human Subject Rendering Requirement.
- **LuminanceHierarchy** — entity_01 (Brightest): "the brightest, sharpest point in the frame"; entity_02 (glass): "crisp and sharp... lit clearly but a touch dimmer than her face"; entity_05 (Dimmest): kitchen "softened gently... without competing with her."
- **Imperfections list updated** — counter-level imperfections (dusted scoop, berries) replaced with in-frame equivalents: smoothie texture on glass, asymmetric half-smile.
- **DOF unchanged** — 85mm/f4 Atmospheric kept; kitchen backdrop softens as in the base.
- **Pose variation:** not applicable — single subject.

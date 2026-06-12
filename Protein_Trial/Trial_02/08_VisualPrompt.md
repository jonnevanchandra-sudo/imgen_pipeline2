# Visual Prompt — Natural Protein Powder (Stage 8.2.1)

Framework: `8.2.1 Prompt_Compiler.md` v3.1 (GPT Image 2.0 JSON priority blocks + Compression System)
Input: SynthesisContract (Stage 7.1, re-run) — `Protein_Trial/Trial_02/07_SynthesisContract.md`

No reference images were supplied, so **no `BRAND_ASSETS` block** and **no `ReferenceAssetManifest`** are included — the generic pack is carried textually in `HIGH.brand` with the no-legible-text rule. Single subject → no multi-subject pose-variation clause. `CameraSpecs` (50mm, f/5) appear verbatim in CAMERA; `LuminanceHierarchy` is translated into LIGHTING as relative-exposure behavior. Compiled under the Single-Statement and Default-Elision rules to the 200–300 word target.

```json
{
  "VisualPrompt": {
    "CRITICAL": {
      "subjects": "A woman in her early thirties, alone at her own kitchen counter on an ordinary morning, in a soft knit top, caught just after a sip — the glass still at her lips, eyes softened, an unguarded half-smile. Her enjoyment must read as private and genuine, never aimed at the camera.",
      "emotion": "The quiet surprise of something healthy that actually tastes good — savoring, not celebration.",
      "evidence": "On the counter beside her, in just-used disarray: a peeled banana, scattered rolled oats, a few fresh berries, a split vanilla pod — each individually recognizable as real food, left as if she just made the drink, not arranged."
    },
    "HIGH": {
      "drink": "The smoothie is thick and visibly blended — a natural pale oat-vanilla tone with a faint berry swirl, its texture clinging to the inside of the glass.",
      "brand": "An open matte kraft-paper protein pouch and a powder-dusted scoop sit among the ingredients as ordinary kitchen objects. The label is clean and minimal, carrying no legible text or logo of any kind."
    },
    "MEDIUM": {
      "setting": "A lived-in home kitchen, everyday clutter at the frame edges — a real morning, not a set."
    },
    "LOW": {
      "style": "Warm editorial food-and-lifestyle photography; appetizing but never laboratory-clean."
    },
    "FORMAT": "Vertical 4:5 or square 1:1 for an Instagram feed. Keep her face, the pouch, and the glass out of the top 10% and bottom 20% of the frame.",
    "LIGHTING": "Soft directional morning window light keys her face and the glass with natural bounce fill, falling off gently into the room. Her face is the brightest point; the drink, pouch, and ingredients sit a touch lower; the kitchen and the window stay dimmer still — the window a soft diffused glow rather than a blown-out highlight, so nothing behind her outshines her. Daylight only, no theatrical or studio shaping.",
    "CAMERA": "Eye-level near-medium shot from the waist up, as if the viewer stands at the counter with her. 50mm at f/5: her face, the glass, and the counter ingredients stay sharp to clearly legible, while the kitchen and window soften progressively into recognizable shapes — counter line, window frame, cabinetry — never heavy bokeh or a flat cutout blur.",
    "AUTHENTICITY": {
      "human_authenticity": "Real skin — visible pores, natural tone variation, a relaxed asymmetric expression. Nothing smoothed or beauty-filtered.",
      "environmental_authenticity": "Everyday objects at the edges, light wear on the counter, real morning-light behavior — nothing set-dressed.",
      "material_authenticity": "Just-used traces: oats scattered where the scoop was used, a smudge or drip near the glass, powder dust on the scoop; matte natural surfaces, nothing glossy or plastic.",
      "imperfection_rule": "Credibility beats styling — keep the casual placement and small imperfections."
    },
    "SCENE": "She stands behind the counter; the open pouch, scoop, and ingredients sit on the counter surface in the lower foreground, between the viewer and her.",
    "NEGATIVE": "No gym equipment or athletic wear. No clinical or studio product shot. No posed to-camera smile. No styled flat-lay. No before/after framing. No legible text or logos anywhere. No competitor packaging. No artificial neon drink color. No airbrushed skin. No heavy or uniform background blur."
  }
}
```

---

## Compile Notes

- **~300 words** (excluding this note), inside the v3.1 target. Detail density is concentrated where it fights a default — ingredient identifiability and the no-legible-text label — and stripped everywhere the model would infer correctly on its own.
- **Single-Statement Rule:** every fact has one home. All depth-of-field / blur language lives **only** in CAMERA; LIGHTING owns all brightness/exposure facts (the `LuminanceHierarchy` translation); the kitchen is identified once in `MEDIUM.setting` and never re-identified (AUTHENTICITY.environmental describes only its imperfections). The no-legible-text rule is stated once positively in `HIGH.brand` and fenced once in NEGATIVE — the permitted NEGATIVE failure-mode exemption, used here because fabricated label text is a high-risk failure.
- **Default-Elision:** floor-anchoring, "ingredients on the counter are smaller than her," and "background is behind her" are omitted as surprisal-test failures. SCENE keeps only the one non-inferable placement fact — the evidence sits in the lower foreground *between viewer and subject*, so the model doesn't bury it behind her or push it out of frame.
- **CameraSpecs verbatim:** "50mm at f/5" stated as values, not paraphrased to "shallow depth of field." Anchors the Atmospheric/Soft-Focus falloff from `OpticalIntent`.
- **LuminanceHierarchy → exposure prose:** face Brightest → "brightest point"; drink/pouch/ingredients Mid → "a touch lower"; kitchen + window Dimmest → "dimmer still… nothing behind her outshines her." Translated as behavior, not a restated ranked list.
- **Fixed blocks flattened:** FORMAT, LIGHTING, CAMERA, SCENE collapse to single strings (compact post-elision); AUTHENTICITY keeps sub-keys (four genuinely distinct anti-AI instructions).
- **Single subject:** no pose-variation requirement and no "synchronized strides" negative — those apply only to 2+ shared-action subjects.
- **No new creative decisions** — every block traces to a resolved element in the SynthesisContract. Differs from `08a` (8.1.1 flat YAML) only in format and compression, not in content.

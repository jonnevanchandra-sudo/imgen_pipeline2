# Visual Prompt — Natural Protein Powder (Stage 8.2.1)

Framework: `8.2.1 Prompt_Compiler.md` v3.1 (GPT Image 2.0 JSON priority-block format + Compression System)
Input: SynthesisContract (Stage 7.1)

No reference images in this run → **no `BRAND_ASSETS` block, no `ReferenceAssetManifest`**. The pack is carried textually as a generic pouch with a hard no-legible-text rule.

```json
{
  "VisualPrompt": {
    "CRITICAL": {
      "subjects": "A woman in her early thirties, soft knit top, alone at her kitchen counter, caught just after a sip of a thick creamy smoothie — eyes briefly closed, an unguarded half-smile, glass still at her lips. Never posed to camera.",
      "emotion": "The quiet surprise of 'oh, that's actually good' — savoring, not celebration."
    },
    "HIGH": {
      "brand": "Beside her on the counter: an open matte kraft protein-powder pouch with a clean minimal label and a powder-dusted scoop. A peeled banana, scattered rolled oats, fresh berries, and a split vanilla pod lie in just-used disarray around it — each recognizable as real food.",
      "drink": "The smoothie is visibly thick, pale oat-vanilla with a faint berry swirl, texture clinging to the glass.",
      "setting": "A lived-in home kitchen in soft morning light — an ordinary morning, not a fitness routine."
    },
    "LOW": {
      "style": "Warm editorial food-and-lifestyle photography — appetizing, natural, unpolished."
    },
    "FORMAT": "Vertical 4:5 or square 1:1 for an Instagram feed post. Keep her face, the glass, and the pouch out of the top 10% and bottom 20% of the frame — Instagram UI may cover those zones.",
    "LIGHTING": "Soft morning window light keys her face and the glass, natural bounce fill, gentle falloff into the room. Bright, appetizing highlights on the drink. No theatrical shaping, no studio flatness.",
    "CAMERA": "Eye-level medium shot, waist up — the viewer stands at the counter with her. 50mm at f/2.2: face and glass sharp, counter items semi-legible and identifiable, window and kitchen dissolving into soft bright bokeh. Progressive falloff, no uniform blur.",
    "AUTHENTICITY": {
      "human_authenticity": "Real skin — visible pores, natural tone variation, a relaxed asymmetric expression. Nothing beauty-filtered.",
      "environmental_authenticity": "Light counter wear, everyday clutter at the frame edges.",
      "material_authenticity": "Oats scattered where the scoop was used, a smudge near the glass, matte kraft paper — just-used, not styled.",
      "imperfection_rule": "Credibility beats styling — keep the disarray."
    },
    "SCENE": "The glass is in her hand at her lips; pouch, scoop, and ingredients sit on the counter in the lower foreground.",
    "NEGATIVE": "No gym equipment or athletic wear. No posed to-camera smile. No legible text or logos anywhere. No competitor packaging. No artificial neon colors in the drink. No clinical studio look. No styled flat-lay perfection. No airbrushed skin."
  }
}
```

---

## Compile Notes

- **~330 words** — above the 200–300 target, within the 400 ceiling. Overage sits in `HIGH.brand`: the ingredient list (banana, oats, berries, vanilla) is protected MustSurvive evidence — it *is* the "natural ingredients" message — and not compressible.
- **CameraSpecs verbatim:** "50mm at f/2.2" stated as values in CAMERA, from `PhysicalRendering.CameraSpecs`.
- **Single-Statement applied:** the savoring moment lives only in CRITICAL (SCENE places the glass, doesn't re-describe the expression); drink texture only in HIGH.drink; all focus/blur only in CAMERA; "no legible text" stated once, in NEGATIVE (its home as a prohibition), with the pouch label described positively as "clean minimal" in HIGH.brand.
- **Default-Elision applied:** floor/surface anchoring, "kitchen behind her," natural object scales, window-as-light-source geometry all cut — implied by the scene. "Morning kitchen" carries its own furniture.
- **MEDIUM omitted:** "ordinary daily life" survives inside HIGH.setting's last clause; nothing else at that tier carried a distinct visual fact.
- **Pose variation:** not applicable — single subject (`pose_variation_required: false` in the CompositionRenderingContract).
- **No new creative decisions** — every sentence traces to the SynthesisContract.

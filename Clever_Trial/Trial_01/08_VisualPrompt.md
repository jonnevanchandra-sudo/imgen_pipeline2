# Visual Prompt — CLEVER Weight Down "3 PM Office Rescue" (Stage 8.2.1)

Framework: `8.2.1 Prompt_Compiler.md` v3.1 (GPT Image 2.0 JSON priority-block format + Compression System)
Input: SynthesisContract (Stage 7.1)

No reference images in this run → **no `BRAND_ASSETS` block, no `ReferenceAssetManifest`**. CLEVER Weight Down packaging (wordmark + '減重蛋白' label) is carried textually as the named ProductSpec.

```json
{
  "VisualPrompt": {
    "CRITICAL": {
      "subjects": "A CLEVER Weight Down pouch in soft pink-and-white packaging, paired with a prepared shake, sits sharp and bright at the front of an office desk. A hand enters the frame and reaches toward it — relaxed, unhurried, like reaching for something already decided.",
      "emotion": "A small choice that has quietly already been made — calm and settled, nothing left to resist or negotiate."
    },
    "HIGH": {
      "brand": "The pouch's 'CLEVER' wordmark and '減重蛋白' label text are crisp and fully legible. The shake is a smooth, uniform beverage in a glass or shaker bottle.",
      "setting": "An ordinary Hong Kong office desk in the mid-afternoon. Further back on the same desk sits a typical 3pm snack-run order — siu mai in a takeaway container and iced lemon tea in a disposable cup — recognizable but visually settled into the background."
    },
    "LOW": {
      "style": "Candid commercial-lifestyle photography — clean but unstaged, like a real desk caught mid-afternoon."
    },
    "FORMAT": "Vertical 4:5 (1080x1350) for Instagram. Keep all elements out of the bottom 15-20% of the frame, reserved for caption overlay.",
    "LIGHTING": "Soft, even daylight keys the pouch, shake, and hand as the brightest part of the frame, with a gentle natural falloff toward the snack and desk behind. No moody or dramatic shaping.",
    "CAMERA": "High-angle close-up, near distance, looking down over the desk. 50mm at f/4 — pouch, shake, and hand sharp; the siu mai and tea mildly softened but identifiable; the desk surroundings dissolve into the softest blur. Progressive falloff, no flat uniform blur.",
    "AUTHENTICITY": {
      "human_authenticity": "The hand shows real skin — visible pores, subtle tone variation, natural knuckle and joint detail. Nothing smoothed or airbrushed.",
      "environmental_authenticity": "Ordinary desk clutter at the frame edges — a laptop corner, notebook, pen.",
      "material_authenticity": "The pouch and shake look clean and matte; the takeaway box and cup look ordinary and slightly worn.",
      "imperfection_rule": "Credibility over polish — keep the everyday imperfections."
    },
    "SCENE": "The siu mai and iced lemon tea sit behind and to the side of the pouch and shake, further from the viewer.",
    "NEGATIVE": "No split-screen or VS graphic layout. No before/after or body-transformation imagery. No clinical or lab supplement look. No shaming close-up of the snack. No visible face or full figure. No legible text other than CLEVER and 減重蛋白. No dramatic or moody lighting."
  }
}
```

---

## Compile Notes

- **~230 words** — within the 200–300 target.
- **CameraSpecs verbatim:** "50mm at f/4" stated as values in CAMERA, from `PhysicalRendering.CameraSpecs`.
- **Single-Statement applied:** the "already decided" gesture lives only in CRITICAL.subjects; product legibility only in HIGH.brand; all focus/blur/depth-of-field facts only in CAMERA; luminance hierarchy translated into LIGHTING's exposure clause, not restated as a ranking; natural skin texture only in AUTHENTICITY.
- **Default-Elision applied:** floor/surface anchoring, "desk has furniture," ordinary object scale, and "hand belongs to a person" are all cut as inferable. "Office desk in the mid-afternoon" carries its own incidental objects.
- **MEDIUM omitted:** nothing at SimplifyWhenConstrained survived deduplication — the desk-environment fact already lives in HIGH.setting, and natural-skin-texture lives in AUTHENTICITY.
- **Pose variation:** not applicable — single entity is a hand only (`pose_variation_required: false` in the CompositionRenderingContract).
- **No new creative decisions** — every sentence traces to the SynthesisContract.

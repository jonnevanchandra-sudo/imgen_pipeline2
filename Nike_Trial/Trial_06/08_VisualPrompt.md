# Visual Prompt — Nike Chill Run Club (Stage 8.2)

Framework: 8.2 Prompt_Compiler.md v3.0 (GPT Image 2.0 JSON priority-block format)
Input: SynthesisContract (Stage 7.1)

No reference images were supplied for this run, so no `BRAND_ASSETS` block and no `ReferenceAssetManifest` are included.

```json
{
  "VisualPrompt": {
    "CRITICAL": {
      "subjects": "Four or five Hong Kong professionals in their twenties, visibly diverse in gender and styling, mid-stride along a waterfront promenade at night. Each wears a mix of office and running clothes — a blazer tied at the waist or slung over a shoulder, rolled sleeves under a running jacket, a crossbody work bag on one or two of them. Expressions are candid, mid-laugh or mid-conversation, not posed for camera.",
      "emotion": "Warm relief, not effort. This is the feeling of finally exhaling after a long workday — light, social, unguarded."
    },
    "HIGH": {
      "action": "The group moves at a relaxed, conversational jogging pace. Two subjects glance at each other mid-laugh. Body language is loose — arms swinging naturally, no race-ready tension, no competitive form.",
      "brand": "One subject's Nike Pegasus 41 running shoes are clearly visible in the lower frame mid-stride: engineered mesh upper with visible Flywire cable overlays at the midfoot, a thick foam midsole with a visible crash rail along the outer edge, a moderately stacked heel with a padded collar, and a lateral Swoosh in a contrasting tone, legible at this distance.",
      "setting": "A Hong Kong harbourfront promenade at night, with a railing beside the walkway and the dense illuminated skyline visible across the harbour — it should feel like an ordinary, lived-in evening in the city."
    },
    "MEDIUM": {
      "skyline": "The towers across the harbour are dense and warmly lit, softened by light haze and background bokeh — recognizable as Hong Kong but clearly secondary to the group in the foreground."
    },
    "LOW": {
      "style": "Warm-toned editorial lifestyle photography, documentary-candid, restrained color palette, premium but unpolished realism."
    },
    "FORMAT": {
      "aspect_ratio": "Square 1:1 or vertical 4:5 crop, optimized for an Instagram feed post.",
      "safe_zones": "No faces, logos, the visible shoe, or any critical visual information may appear in the top 10% or bottom 20% of the frame — these areas may be covered by Instagram UI or caption overlays."
    },
    "LIGHTING": {
      "quality": "Soft, warm directional light from streetlamps along the promenade, supplemented by ambient glow from the skyline.",
      "temperature": "Warm amber tones throughout — skin should read sun-touched and warm, not orange or sickly.",
      "source": "Streetlights act as the key light on the group from the side/front; the skyline provides a softer warm-cool ambient fill in the background.",
      "hierarchy": "The group reads brighter and warmer than the background skyline, which sits one stop or more darker and softer.",
      "prohibited": "No cold blue or neon-dominant lighting. No hard theatrical shadows. No flat studio lighting on subjects or shoe."
    },
    "CAMERA": {
      "shot_type": "Near full shot, group framed from roughly the knees up with at least one subject's feet/shoes visible at the bottom edge.",
      "angle": "Eye-level — the camera sits at the same height as the runners, as if it's one of the group.",
      "distance": "Close enough that faces and expressions are clearly readable, while still including the promenade and skyline behind.",
      "depth_of_field": "Aperture around f/2.8. The group is in sharp focus; the skyline falls into soft background blur.",
      "optical_notes": "Progressive bokeh falloff — the railing and water near the group stay semi-legible, while the towers further back dissolve into soft, warm circular bokeh."
    },
    "AUTHENTICITY": {
      "human_authenticity": "Real skin — visible pores, subtle tone variation, a light post-workday flush. Natural asymmetry in expressions and posture. Nothing smoothed or beauty-filtered.",
      "environmental_authenticity": "Slightly uneven promenade paving, ambient light spill, a faint evening haze over the water — a real city evening, not a clean set.",
      "material_authenticity": "Visible fabric creases on jackets and bags, naturally worn (not box-fresh) texture on the running shoe, non-glossy surfaces throughout.",
      "imperfection_rule": "Credibility beats polish. Slight asymmetries in pose, expression, and styling must remain — do not correct them toward symmetry or perfection."
    },
    "SCENE": {
      "depth_structure": "The group occupies the foreground and midground in sharp focus. The promenade railing and harbour water sit just behind them, semi-visible. The skyline occupies the background, softly blurred.",
      "spatial_relationships": "Subjects face and interact with each other — not the camera. The railing runs alongside the group on one side. The skyline is visible behind and beyond the water, framing the group without surrounding them.",
      "anchor_relationships": "The group is floor-anchored on the promenade pavement, mid-stride. The skyline is fixed across the harbour as a distant backdrop, not physically connected to the group.",
      "scale": "The group fills most of the frame at natural human scale. The skyline reads as a wide, distant backdrop — present but visually smaller and softer than the subjects."
    },
    "NEGATIVE": "No race numbers, finish lines, or competitive racing elements. No sprinting form or strained 'race faces'. No posed lineup facing the camera. No isolated or studio-style product shot of the shoe. No solo runner. No cold blue or neon-dominant lighting. No airbrushed or AI-smoothed skin. No flat studio lighting."
  }
}
```

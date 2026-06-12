# Visual Prompt — Nike Chill Run Club (Stage 8.2)

Framework: `8.2 Prompt_Compiler.md` v3.0 (GPT Image 2.0 JSON priority-block format)
Input: SynthesisContract (Stage 7.1)

No reference images were supplied for this run, so **no `BRAND_ASSETS` block** and **no `ReferenceAssetManifest`** are included. The Nike Pegasus requirement is carried as a textual `HIGH.brand` instruction — model name first, visual identifiers following — exactly as the Synthesis Contract preserved it.

```json
{
  "VisualPrompt": {
    "CRITICAL": {
      "subjects": "A loose group of four or five Hong Kong professionals in their twenties, visibly diverse in gender and styling, jogging together at night. They engage each other, mid-laugh or mid-conversation, never posed to the camera.",
      "emotion": "A shared exhale. The relief of finally unwinding after a long workday — light, social, unguarded. Recovery, not effort."
    },
    "HIGH": {
      "action": "Relaxed, conversational jogging pace — slow enough that they could still talk. Loose body language, arms swinging naturally, two subjects glancing at each other mid-laugh. No race tension, no competitive form.",
      "brand": "At least one subject wears Nike Pegasus (latest generation) running shoes, visible in the lower frame mid-stride: engineered mesh upper with visible Flywire cable overlays at the midfoot, a thick foam midsole with a visible crash rail along the lateral edge, a moderately stacked heel with a padded collar, and a lateral Swoosh in a contrasting tone, legible at this distance. Worn-in, lifestyle context — not a clean studio product shot.",
      "setting": "A Hong Kong harbourfront promenade at night: a railing runs alongside the walkway, the dense illuminated skyline sits across the water. It should feel like an ordinary, lived-in city evening."
    },
    "MEDIUM": {
      "main_character": "One subject reads as quietly self-possessed within the group — present and at ease, owning the evening without performing.",
      "skyline": "Towers across the harbour are dense and warmly lit, softened by light haze and bokeh — clearly Hong Kong, clearly secondary to the group."
    },
    "LOW": {
      "style": "Warm-toned editorial lifestyle photography. Documentary-candid, restrained palette, premium but unpolished realism."
    },
    "FORMAT": {
      "aspect_ratio": "Square 1:1 or vertical 4:5, optimized for an Instagram feed post.",
      "safe_zones": "No faces, the Swoosh, the visible shoe, or any critical visual information may appear in the top 10% or bottom 20% of the frame — these areas may be covered by Instagram UI or caption overlays."
    },
    "LIGHTING": {
      "quality": "Soft, warm directional light from promenade streetlamps, with ambient glow from the skyline.",
      "temperature": "Warm amber overall — skin reads sun-touched and warm, never orange or sickly.",
      "source": "Streetlamps key the group from the side and front; the skyline gives a softer, cooler ambient fill behind them.",
      "hierarchy": "The group sits brighter and warmer than the background; the skyline falls a stop or more darker and softer.",
      "prohibited": "No cold blue or neon-dominant cast. No hard theatrical shadows. No flat studio lighting on subjects or shoe."
    },
    "CAMERA": {
      "shot_type": "Near full shot — the group framed roughly knees-up, with at least one subject's shoes visible at the bottom edge.",
      "angle": "Eye-level. The camera sits at the runners' height, as if it's one of the group.",
      "distance": "Close enough to read faces and expressions clearly, far enough to keep the promenade and skyline behind.",
      "depth_of_field": "Around 35mm at f/2.8. The group is sharp; the skyline drops into soft background blur.",
      "optical_notes": "Progressive bokeh falloff — the railing and near water stay semi-legible, the far towers dissolve into smooth, warm circular bokeh. No flat, uniform blur layer."
    },
    "AUTHENTICITY": {
      "human_authenticity": "Real skin — visible pores, subtle tone variation, a light post-workday flush. Asymmetric, candid expressions and posture. Nothing smoothed or beauty-filtered.",
      "environmental_authenticity": "Slightly uneven promenade paving, ambient light spill, a faint haze over the water. A real city evening, not a clean set.",
      "material_authenticity": "Fabric creases on jackets and bags, naturally worn (not box-fresh) texture on the shoe, matte non-glossy surfaces throughout.",
      "imperfection_rule": "Credibility beats polish. Keep slight asymmetries in pose, expression, and styling — do not correct them toward symmetry or perfection."
    },
    "SCENE": {
      "depth_structure": "Group and shoes hold the foreground in sharp focus. The promenade railing and harbour water sit just behind, semi-visible. The skyline occupies the soft background.",
      "spatial_relationships": "Subjects face and interact with each other, not the camera. The railing runs alongside the group on one side. The skyline sits behind and beyond the water, framing the group without surrounding them.",
      "anchor_relationships": "The group and the visible shoes are floor-anchored on the promenade pavement, mid-stride. The skyline is fixed across the harbour as a distant horizon backdrop, not connected to the group.",
      "scale": "The group fills most of the frame at natural human scale. The shoes are true-to-life and small within the lower frame, subordinate to the faces. The skyline reads wide, distant, and softer than the subjects."
    },
    "NEGATIVE": "No race numbers, finish lines, or competitive racing. No sprinting or strained race faces. No posed lineup facing the camera. No solo runner. No isolated or studio product shot of the shoe. No product-hero framing. No competitor brands. No cold blue or neon-dominant lighting. No flat studio lighting. No airbrushed or AI-smoothed skin."
  }
}
```

---

## Compile Notes

- **MustSurvive → CRITICAL:** shared relief + peer group. **PreserveWhenPossible → HIGH:** easy non-competitive action, Nike Pegasus (name + identifiers, kept subordinate), HK night setting.
- **Named product (no reference image):** carried in `HIGH.brand` as text — model name first, visual identifiers following — per the 5.2.5 → Synthesis → Compiler handoff rule. No `BRAND_ASSETS` block emitted because no Brand-Bearing reference asset exists.
- **Fixed blocks** (FORMAT, LIGHTING, CAMERA, AUTHENTICITY, SCENE, NEGATIVE) written in full and uncompressed. DOF realism and natural-skin requirements from Stage 6.1 preserved verbatim in CAMERA / AUTHENTICITY.
- **No new creative decisions** introduced — every block traces to a resolved element in the Synthesis Contract.

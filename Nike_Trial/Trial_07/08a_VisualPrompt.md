# Visual Prompt — Nike Chill Run Club (Stage 8.1.1, flat YAML)

Framework: `8.1.1 Prompt_Compiler.md` v2.3 (flat prose string)
Input: SynthesisContract (Stage 7.1) — same contract as `08_VisualPrompt.md` / `08b_VisualPrompt.md`; only the compiler differs.

No `ReferenceAssetManifest` exists for this run (no reference images uploaded), so Brand Asset Embedding is **not activated** — output is identical to v2.2: a single `VisualPrompt` YAML key, no manifest appended. The Nike Pegasus requirement is carried as inline textual description (model name + visual identifiers together).

```yaml
VisualPrompt: "A candid, documentary-style lifestyle photograph for an Instagram feed, square 1:1 or vertical 4:5. Four or five Hong Kong professionals in their twenties, visibly diverse in gender and styling, jog together along a harbourfront promenade at night. They move at an easy, conversational pace — arms loose, two of them glancing at each other mid-laugh, all engaged with one another and never with the camera. The feeling is a shared exhale: the relief of finally unwinding after a long workday — light, social, unguarded; recovery, not effort. One subject wears Nike Pegasus running shoes (latest generation), clearly visible mid-stride in the lower frame: engineered mesh upper with Flywire cable overlays at the midfoot, a thick foam midsole with a visible crash rail along the lateral edge, a moderately stacked padded heel, and a contrasting lateral Swoosh legible at this distance. The shoes look worn-in, not box-fresh. The camera sits at eye level, framing the group from the knees up as if it were one of them, shot on a 35mm lens at f/2.8. The group is sharp; behind them the promenade railing and near water stay semi-legible while the dense illuminated skyline across the harbour dissolves into soft, warm circular bokeh — progressive depth falloff, never a flat uniform blur. Warm streetlamp light keys the group from the side and front; the background sits a stop or more darker and cooler, and skin reads warm, never orange. Skin shows real texture — visible pores, subtle tone variation, a light post-workday flush — with asymmetric candid expressions, and each runner is caught at a different point in their stride rather than moving in step. Fabric creases on jackets and bags, slightly uneven paving, ambient light spill, and a faint haze over the water keep the scene credible — credibility beats polish. No solo runner, no sprinting or race faces, no race numbers or finish lines, no posed lineup facing the camera, no studio product shot or product-hero framing, no competitor brands, no airbrushed skin, no cold neon-blue lighting, and no faces, Swoosh, or the visible shoe in the top 10% or bottom 20% of the frame."
```

---

## Compile Notes

- **~330 words**, single continuous prose string per the 8.1.1 output rule (no JSON, no nested structure). Emphasis order follows CommunicationAllocation: group + shared relief first, easy pace, then Pegasus, then camera/light/authenticity, prohibitions last.
- **CameraSpecs carried verbatim** from `PhysicalRendering.CameraSpecs` — "35mm lens at f/2.8" stated as values in the prose.
- **Wardrobe note:** the office-to-run hybrid styling (blazer, rolled sleeves, work bag) present in the SynthesisContract was **intentionally omitted**, mirroring the manual edit made to `08b_VisualPrompt.md`. If that omission is permanent, it should be resolved upstream (CampaignContract `required_assets` → Synthesis), not just at the compiler.
- **Pose variation** ("each runner caught at a different point in their stride") traces to `ImperfectionRendering` ("preserve slight asymmetries in pose... do not correct toward symmetry").
- **No BRAND_ASSETS / manifest** — Brand Asset Embedding inactive for this run; output identical to v2.2.

# Visual Prompt — Natural Protein Powder (Stage 8.1.1, flat YAML)

Framework: `8.1.1 Prompt_Compiler.md` v2.3 (flat prose string)
Input: SynthesisContract (Stage 7.1) — same contract as `08_VisualPrompt.md`; only the compiler differs.

No `ReferenceAssetManifest` exists for this run (no reference images uploaded), so Brand Asset Embedding is **not activated** — output is identical to v2.2: a single `VisualPrompt` YAML key, no manifest appended. The generic pack is carried as inline textual description with the no-legible-text rule woven into the prose.

```yaml
VisualPrompt: "An intimate, candid lifestyle photograph for an Instagram feed, vertical 4:5 or square 1:1. A woman in her early thirties stands alone at her kitchen counter on an ordinary morning, wearing a soft knit top, caught in the private moment just after a sip of a thick, creamy smoothie — eyes briefly closed, an unguarded half-smile, the glass still raised at her lips. Her enjoyment is genuine and unperformed, never directed at the camera: the quiet surprise of something healthy that actually tastes good. The smoothie is visibly thick and blended from real food — a pale oat-vanilla tone with a faint berry swirl, texture clinging to the inside of the glass. Beside her on the wooden counter sits an open matte kraft-paper protein powder pouch with a clean, minimal label that carries no legible text or logo, and a scoop dusted with powder resting against it. Around the pouch, in casual just-used disarray, lie a peeled banana, scattered rolled oats, a few fresh berries, and a split vanilla pod — each individually recognizable as real food, placed as if she just made the drink, not styled into a flat-lay. The kitchen behind her is lived-in and softly out of focus, with everyday objects at the edges of the frame and soft natural-morning light coming from a window — the light keys her face and the glass with natural bounce fill and gentle falloff into the room, leaving bright, appetizing highlights on the drink. The photograph is shot at eye level from the waist up on a 50mm lens at f/16, as if the viewer were standing at the counter with her: her face and the glass are sharp, the counter ingredients remain semi-legible and identifiable, and the window and kitchen dissolve into soft, bright bokeh with progressive depth falloff, never a flat uniform blur. Her skin shows real texture — visible pores, natural tone variation, a relaxed asymmetric expression with nothing smoothed or beauty-filtered — and the scene keeps its small imperfections: oats scattered where the scoop was used, a smudge near the glass, light wear on the counter. Credibility beats styling. No gym equipment or athletic wear, no posed to-camera smile, no legible text or logos anywhere in the frame, no competitor packaging, no artificial neon colors in the drink, no clinical studio look, no styled flat-lay perfection, no airbrushed skin, and no faces, pouch, or glass in the top 10% or bottom 20% of the frame."
```

---

## Compile Notes

- **~400 words**, single continuous prose string per the 8.1.1 output rule (no JSON, no nested structure). Emphasis order follows CommunicationAllocation: savoring moment first, drink, then pack + ingredient evidence, then setting/light/camera/authenticity, prohibitions last.
- **CameraSpecs carried verbatim** from `PhysicalRendering.CameraSpecs` — "50mm lens at f/2.2" stated as values in the prose.
- **No-legible-text rule stated twice deliberately** — once positively at the pouch description ("clean, minimal label that carries no legible text or logo") and once in the closing prohibitions. 8.1.1 has no Single-Statement rule, and fabricated label text is a high-risk failure mode worth fencing at both the asset and the prompt level.
- **Brand Asset Embedding inactive** — no reference images; when real packaging exists, rerun 5.2.5 with the file and this compiler will embed "This is reference_asset_01 — reproduce it exactly..." inline at the pouch description.
- **Pose variation:** not applicable — single subject.
- **No new creative decisions** — every sentence traces to a resolved element in the SynthesisContract.

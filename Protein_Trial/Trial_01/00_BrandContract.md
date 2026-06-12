# Brand Contract — Natural Protein Powder (Stage 0)

Framework: `0.Brand Intelligence.v2.md`
**Run mode: DECLARED ASSUMPTIONS.** No brand reference materials (ads, imagery, packaging, campaigns) were supplied — this contract is built from the campaign owner's stated intent only ("tastes good, natural ingredients") plus category knowledge. Every signal below is therefore an assumption with capped confidence (≤ 0.6), not an observation. Replace with an extracted BrandContract when real brand materials exist.

```json
{
  "BrandContract": {
    "Identity": {
      "essence": "Honest food that happens to be protein — pleasure and health without compromise",
      "positioning": "A food brand, not a supplement brand",
      "signals": [
        { "signal": "Ingredient transparency as identity (you can read and recognize everything in it)", "class": "Core", "confidence": 0.6, "basis": "assumed from stated intent" },
        { "signal": "Taste-first language — 'delicious' before 'protein per serving'", "class": "Core", "confidence": 0.6, "basis": "assumed from stated intent" },
        { "signal": "Everyday-kitchen context rather than gym context", "class": "Adaptive", "confidence": 0.5, "basis": "assumed" }
      ]
    },
    "Audience": {
      "primary": "Health-conscious adults 25–40 who eat well and move regularly but do not identify as gym athletes",
      "relationship_to_category": "Skeptical — they expect protein powder to taste chalky and artificial, and treat it as a tolerated obligation",
      "confidence": 0.55
    },
    "CommunicationPhilosophy": {
      "tone": "Plain-spoken, warm, sensory — show, don't claim",
      "avoid": ["clinical supplement language", "performance bravado", "before/after transformation framing"],
      "confidence": 0.6
    },
    "RenderingStyle": {
      "assumed_direction": "Natural-light food photography warmth; real kitchens and real skin; appetite appeal over lab cleanliness",
      "confidence": 0.5
    },
    "CoreTensions": [
      { "tension": "Indulgence ↔ Health", "resolution_bias": "Refuse the tradeoff — the product is proof you can have both" },
      { "tension": "Supplement category ↔ Food identity", "resolution_bias": "Behave like food in every visual decision" }
    ],
    "CreativeTradeoffs": [
      "Appetite appeal may outrank product-pack prominence",
      "Credibility (real kitchen, real person) outranks polish"
    ],
    "SacredBrandAssets": [
      "None on record — packaging and logo not yet supplied. When available, ingest via reference image (5.2.5) so the pack reproduces exactly."
    ]
  }
}
```

## Notes

- This contract deliberately makes the **smallest** set of assumptions needed for Strategy to run. It should be regenerated from real materials before any production campaign.
- The unnamed product pack is treated as **present but generic** downstream: a clean, minimal pouch with no legible invented brand text (image generators garble fabricated text; a clean label is safer than a fake one).

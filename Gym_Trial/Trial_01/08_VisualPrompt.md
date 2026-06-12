# Visual Prompt — Anytime Fitness Sai Ying Pun (Stage 8.2.1, v3.1)

Framework: `8.2.1 Prompt_Compiler.md`
Input: SynthesisContract (Stage 7.1)
Target generator: GPT Image 2.0
Compression System applied: Single-Statement Rule, Default-Elision Rule, 200–300 word target (BRAND_ASSETS exempt).

```json
{
  "VisualPrompt": {
    "CRITICAL": "A university-aged East Asian man in plain grey athletic wear, mid-rep on a squat rack, focused downward on the lift, not looking at camera. Candid gym photograph, vertical 4:5.",

    "HIGH": "He grips a loaded barbell on a silver Torque USA rack stacked with green, grey, yellow, and blue bumper plates (reference_asset_02 — reproduce exactly). Behind and to the side, a wood-paneled wall with a white 'AF' monogram and a black overhead rig holding an 'ANYTIME FITNESS'-branded punching bag, on purple flooring (reference_asset_03 — reproduce exactly, monogram must stay legible).",

    "MEDIUM": "Beyond the rack, the gym floor recedes: dark ceiling with exposed ductwork and recessed LED panels, black rubber tile with yellow hazard-stripe accents, treadmill row and machines (reference_asset_01 — style match).",

    "LOW": "Subtle warm-purple tint over the functional zone against cooler white-LED light on the main floor.",

    "FORMAT": "Vertical 4:5, medium shot, subject off-center.",

    "LIGHTING": "Even, slightly cool overhead LED gym lighting; soft ambient bounce off rubber flooring; bright, welcoming mood.",

    "CAMERA": "35mm lens, f/8, eye-level.",

    "AUTHENTICITY": "Natural skin texture with visible pores, slight asymmetry, and realistic sweat sheen — no airbrushing or beauty-filter smoothing. Athletic wear shows natural wrinkling.",

    "SCENE": "One continuous real gym interior, single subject, no other people.",

    "BRAND_ASSETS": [
      {
        "prompt_reference_id": "reference_asset_01",
        "role": "Style/atmosphere reference for the broader gym floor — ceiling, flooring, equipment row. Adapt freely; approximate match only."
      },
      {
        "prompt_reference_id": "reference_asset_02",
        "role": "Reproduce exactly — the silver Torque USA rack and its green/grey/yellow/blue bumper plate set must be recognizable as the equipment in use."
      },
      {
        "prompt_reference_id": "reference_asset_03",
        "role": "Reproduce exactly — the white 'AF' wall monogram, black functional rig with 'ANYTIME FITNESS' punching bag, and purple flooring. The 'AF' monogram must remain legible even at reduced sharpness."
      }
    ],

    "NEGATIVE": "No competitor logos, no extra people, no invented signage or legible text beyond the existing AF monogram and Anytime Fitness wordmark, no flat/uniform background blur, no airbrushed/plastic skin, no posed or camera-aware expression, no flexing or 'fitness model' framing, no group/class scene."
  },

  "ReferenceAssetManifest": [
    {
      "prompt_reference_id": "reference_asset_01",
      "source_filename": "gym_photo_01.jpg",
      "description": "Wide gym floor — ceiling, flooring, treadmill row"
    },
    {
      "prompt_reference_id": "reference_asset_02",
      "source_filename": "gym_photo_02.jpg",
      "description": "Torque USA rack with colorful bumper plates"
    },
    {
      "prompt_reference_id": "reference_asset_03",
      "source_filename": "gym_photo_03.jpg",
      "description": "AF-branded wall, functional rig, and punching bag on purple flooring"
    }
  ]
}
```

## Compile Notes

- Word count (CRITICAL through SCENE + LIGHTING/CAMERA/AUTHENTICITY/FORMAT/NEGATIVE, excluding BRAND_ASSETS): ~210 words — within the 200–300 target.
- Default-elision applied: omitted "indoor", "realistic photo quality", "well-lit" type defaults the generator would supply unprompted.
- Single-Statement Rule: lighting stated once (LIGHTING block); camera specs stated once (CAMERA block); skin/material realism stated once (AUTHENTICITY); NEGATIVE only fences failure modes whose positive form exists elsewhere (no airbrushing ↔ AUTHENTICITY; single subject ↔ SCENE).
- `BRAND_ASSETS` + `ReferenceAssetManifest` require the three source photos (`gym_photo_01.jpg`, `gym_photo_02.jpg`, `gym_photo_03.jpg` — the photos supplied earlier in this conversation) to be attached to the image-generation API call at generation time, in the order corresponding to `reference_asset_01/02/03`.

# Visual Prompt — FIT24 (Stage 8.2.1, v3.1)

Framework: `8.2.1 Prompt_Compiler.md`
Input: SynthesisContract (Stage 7.1)
Target generator: GPT Image 2.0
Compression System applied: Single-Statement Rule, Default-Elision Rule, 200–300 word target (BRAND_ASSETS exempt).

```json
{
  "VisualPrompt": {
    "CRITICAL": "A person in simple casual athletic wear runs at a calm, steady pace on a treadmill, facing floor-to-ceiling windows, looking ahead toward the view, not at camera. Candid gym photograph, vertical 4:5.",

    "HIGH": "Beside and around them, a row of black treadmills faces a floor-to-ceiling glass wall overlooking a green, tree-lined outdoor area. A circular blue-and-white 'FIT24' logo is mounted on the wall near the windows (reference_asset_01 — reproduce exactly, logo must stay legible).",

    "MEDIUM": "Black exposed ceiling with ductwork, conduit, pendant lighting, and ceiling-mounted AC units overhead; polished grey tile flooring with subtle reflections (reference_asset_01 — match).",

    "LOW": "A partition wall and additional gym equipment faintly visible in the background to one side.",

    "FORMAT": "Vertical 4:5, medium shot, slight 3/4 angle, subject off-center.",

    "LIGHTING": "Bright natural daylight flooding through the window wall, lighting the runner from the front/side; soft ambient bounce off the tile floor; airy, calm morning mood.",

    "CAMERA": "28mm lens, f/8.",

    "AUTHENTICITY": "Natural skin texture with visible pores, slight asymmetry, and a light realistic sweat sheen — no airbrushing or beauty-filter smoothing. Athletic wear shows natural movement and slight sweat-darkening.",

    "SCENE": "One continuous real gym interior, single subject, no other people.",

    "BRAND_ASSETS": [
      {
        "prompt_reference_id": "reference_asset_01",
        "role": "Reproduce exactly — the floor-to-ceiling window wall with its green outdoor view, the circular 'FIT24' wall logo, the row of black treadmills, and the exposed dark ceiling must be recognizable as this specific space. The 'FIT24' logo must remain legible even at reduced sharpness."
      }
    ],

    "NEGATIVE": "No competitor logos, no extra people, no invented signage or legible text beyond the existing FIT24 logo, no flat/uniform background blur, no airbrushed/plastic skin, no posed or camera-aware expression, no sprinting-at-max or elite-intensity framing, no group/class scene, no empty room devoid of the runner."
  },

  "ReferenceAssetManifest": [
    {
      "prompt_reference_id": "reference_asset_01",
      "source_filename": "gym_photo_fit24_01.jpg",
      "description": "Window wall with green outdoor view, FIT24 logo, treadmill row, exposed ceiling"
    }
  ]
}
```

## Compile Notes

- Word count (CRITICAL through SCENE + LIGHTING/CAMERA/AUTHENTICITY/FORMAT/NEGATIVE, excluding BRAND_ASSETS): ~190 words — within the 200–300 target (slightly under, acceptable given the single-reference-asset scene has fewer entities to describe).
- Default-elision applied: omitted "indoor", "realistic photo quality", "well-lit" type defaults the generator would supply unprompted.
- Single-Statement Rule: lighting stated once (LIGHTING block); camera specs stated once (CAMERA block); skin/material realism stated once (AUTHENTICITY); NEGATIVE only fences failure modes whose positive form exists elsewhere (no airbrushing ↔ AUTHENTICITY; single subject ↔ SCENE).
- `BRAND_ASSETS` + `ReferenceAssetManifest` require the source photo (`gym_photo_fit24_01.jpg` — the photo supplied earlier in this conversation) to be attached to the image-generation API call at generation time as `reference_asset_01`, as part of the asset package the user mentioned re-injecting.

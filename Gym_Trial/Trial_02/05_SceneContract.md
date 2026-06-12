# Scene Contract — FIT24 (Stage 5.2.5)

Framework: `5.2.5 Scene-Assembly.md`
Inputs: ArtDirectionContract (Stage 4) + ImageAnalysisContract (Stage 5.0) + CampaignContract (Stage 1)
ClientPreferenceContract: not available (Stage 5.5 skipped — no client response to a Visual Discovery package was solicited in this run). This stage runs identically to base Scene Assembly with reference image extraction.

```json
{
  "SceneContract": {
    "Metadata": {
      "brand": "FIT24",
      "concept": "Morning Mile",
      "reference_assets_used": true,
      "named_product_preservation": false
    },

    "RealityModel": "Photographic — a single candid moment captured as if by an observer with a camera, inside a real, physically continuous gym space. No surreal, illustrated, or composited elements.",

    "Entities": [
      {
        "entity_id": "entity_01",
        "name": "Runner (subject)",
        "type": "Human",
        "source": "Generated",
        "description": "An urban professional in their late 20s to mid-30s, wearing simple casual athletic wear (no branded athletic-wear logos), running at a steady pace on one of the treadmills (part of entity_02), facing the window wall. Looking ahead toward the windows/view, not at the camera.",
        "preservation_contract": {
          "preservation_priority": "Flexible",
          "recognizability_requirement": "N/A — generated entity, no reference image",
          "immutable_attributes": [
            "Single subject only (no second person)",
            "Casual athletic wear with no visible competitor or third-party logos"
          ],
          "flexible_attributes": [
            "Exact gender, ethnicity, hairstyle, build, and clothing color — open to generation",
            "Specific running pace/posture, within a calm, steady, non-sprinting range"
          ]
        }
      },
      {
        "entity_id": "entity_02",
        "name": "FIT24 window-wall training space",
        "type": "Brand-Bearing Environment",
        "source": "Reference Asset",
        "prompt_reference_id": "reference_asset_01",
        "description": "The floor-to-ceiling glass wall with its green, tree-lined outdoor view, the row of black treadmills facing the windows, the circular blue-and-white 'FIT24' wall logo, the exposed dark ceiling with ductwork and AC units, and the polished tile flooring — exactly as shown in the supplied reference photo. The runner (entity_01) is on one of these treadmills.",
        "preservation_contract": {
          "preservation_priority": "Critical",
          "recognizability_requirement": "Close Match (Exact Match for the 'FIT24' logo lettering itself)",
          "immutable_attributes": [
            "Floor-to-ceiling window wall with green, tree-lined outdoor view",
            "Circular blue-and-white 'FIT24' wall logo — exact lettering and proportions",
            "Row of black treadmills facing the windows",
            "Black exposed ceiling with ductwork and ceiling-mounted AC units",
            "Polished grey/dark tile flooring"
          ],
          "flexible_attributes": [
            "Exact viewing angle / proportion of window wall vs. treadmill row in frame",
            "Visibility of the background partition wall and additional equipment",
            "Time-of-day lighting intensity"
          ],
          "generation_rule": "Reproduce from reference_asset_01 — do not redraw the FIT24 logo or the window-wall view from training data; they must match the reference."
        }
      }
    ],

    "Relationships": [
      "entity_01 is on a treadmill belonging to entity_02, running facing the window wall — physically integrated into the space, not standing apart from it",
      "entity_02 surrounds entity_01 on all sides (floor, ceiling, window wall, logo) — the runner is inside this specific space, not composited in front of it"
    ],

    "DepthStructure": {
      "foreground": "entity_01 (runner) on a treadmill in the near-midground of the treadmill row",
      "midground": "Remaining treadmill row, FIT24 logo, window wall glass plane",
      "background": "Green outdoor view through the windows (trees, planters, outdoor seating) and the dim background partition/equipment to the right, receding into soft depth"
    },

    "GenerationRequirements": [
      "Single subject only — no additional people, staff, or background extras",
      "The window-wall view, FIT24 logo, treadmill row, and ceiling must originate from one coherent, physically continuous space matching reference_asset_01",
      "No legible text other than the existing 'FIT24' logo already present in the reference asset — no invented signage, posters, or screen text on the treadmill displays",
      "No competitor branding anywhere in frame",
      "Lighting and color grading must unify the subject and environment into one consistent photographic scene (see Stage 6 for specifics)"
    ],

    "ClientPreferenceConflicts": []
  },

  "ReferenceAssetManifest": [
    {
      "prompt_reference_id": "reference_asset_01",
      "source_filename": "gym_photo_fit24_01.jpg",
      "entity_id": "entity_02",
      "asset_type": "Brand-Bearing Environment",
      "preservation_priority": "Critical",
      "recognizability_requirement": "Close Match (Exact Match for 'FIT24' logo)"
    }
  ]
}
```

## Handoff Note

`ReferenceAssetManifest` travels downstream unchanged to Stage 8 (Prompt Compiler), which will use it to produce the `BRAND_ASSETS` block and to attach the source image to the generation API call. The user must re-supply `gym_photo_fit24_01.jpg` (the photo provided in this conversation) at generation time, mapped to `reference_asset_01`.

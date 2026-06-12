# Scene Contract — Anytime Fitness Sai Ying Pun (Stage 5.2.5)

Framework: `5.2.5 Scene-Assembly.md`
Inputs: ArtDirectionContract (Stage 4) + ImageAnalysisContract (Stage 5.0) + CampaignContract (Stage 1)
ClientPreferenceContract: not available (Stage 5.5 skipped — no client response to a Visual Discovery package was solicited in this run). This stage runs identically to base Scene Assembly with reference image extraction.

```json
{
  "SceneContract": {
    "Metadata": {
      "brand": "Anytime Fitness Sai Ying Pun",
      "concept": "Open When You Are",
      "reference_assets_used": true,
      "named_product_preservation": false
    },

    "RealityModel": "Photographic — a single candid moment captured as if by an observer with a camera, inside a real, physically continuous gym space. No surreal, illustrated, or composited elements.",

    "Entities": [
      {
        "entity_id": "entity_01",
        "name": "Student (subject)",
        "type": "Human",
        "source": "Generated",
        "description": "A HKU-aged (late teens to early 20s) university student of East Asian appearance, wearing casual athletic wear (plain t-shirt or tank, joggers or shorts — no branded athletic-wear logos), mid-set on the free-weight rack (entity_02). Genuinely focused on the lift, not looking at camera.",
        "preservation_contract": {
          "preservation_priority": "Flexible",
          "recognizability_requirement": "N/A — generated entity, no reference image",
          "immutable_attributes": [
            "Single subject only (no second person)",
            "Casual athletic wear with no visible competitor or third-party logos"
          ],
          "flexible_attributes": [
            "Exact gender, hairstyle, build, and clothing color — open to generation",
            "Specific exercise/lift performed (must be plausible on entity_02's rack — e.g. barbell squat, bench press, or overhead press)"
          ]
        }
      },
      {
        "entity_id": "entity_02",
        "name": "Torque USA rack with colorful bumper plates",
        "type": "Product/Equipment",
        "source": "Reference Asset",
        "prompt_reference_id": "reference_asset_02",
        "description": "The silver Torque USA half-rack/bench combination loaded with green, grey, yellow, and blue bumper plates, exactly as shown in the supplied reference photo. The student (entity_01) is actively using this rack.",
        "preservation_contract": {
          "preservation_priority": "High",
          "recognizability_requirement": "Close Match",
          "immutable_attributes": [
            "Silver 'TORQUE USA' rack/bench structure",
            "Color-coded bumper plate set: green (largest), grey, yellow, blue"
          ],
          "flexible_attributes": [
            "Exact plate count/arrangement on storage horns",
            "Visibility of the bench attachment depending on crop"
          ],
          "generation_rule": "Reproduce from reference_asset_02 — do not generate a generic power rack from training data."
        }
      },
      {
        "entity_id": "entity_03",
        "name": "AF-branded functional training wall + rig",
        "type": "Brand-Bearing Environment",
        "source": "Reference Asset",
        "prompt_reference_id": "reference_asset_03",
        "description": "The wood-paneled wall bearing the white 'AF' monogram, the black overhead functional rig with the 'ANYTIME FITNESS'-branded punching bag, and the purple rubber flooring of this zone, visible in the background/midground behind or beside the student.",
        "preservation_contract": {
          "preservation_priority": "Critical",
          "recognizability_requirement": "Close Match (Exact Match for the 'AF' wordmark lettering itself)",
          "immutable_attributes": [
            "White 'AF' monogram on wood-paneled wall — exact lettering and proportions",
            "'ANYTIME FITNESS' wordmark on the hanging punching bag",
            "Purple rubber flooring in this zone",
            "Black overhead functional rig with cable attachment points"
          ],
          "flexible_attributes": [
            "Viewing angle of the wall/rig",
            "Visibility of the side cable machine and bench"
          ],
          "generation_rule": "Reproduce from reference_asset_03 — do not redraw the 'AF' monogram from training data; it must match the reference exactly."
        }
      },
      {
        "entity_id": "entity_04",
        "name": "Broader gym floor (atmosphere)",
        "type": "Environmental",
        "source": "Reference Asset",
        "prompt_reference_id": "reference_asset_01",
        "description": "The general industrial-chic gym floor character — dark ceiling with exposed ductwork and a grid of recessed LED panels, black rubber tile flooring with hazard-stripe accents, treadmill row and Precor strength machines — receding into the background, establishing scale and depth beyond the immediate rack/wall area.",
        "preservation_contract": {
          "preservation_priority": "Medium",
          "recognizability_requirement": "Approximate Match",
          "immutable_attributes": [
            "Dark industrial ceiling with exposed ductwork and grid of recessed LED panels",
            "Black rubber tile flooring with yellow/black hazard-stripe accents",
            "Cardio row and Precor-branded equipment present somewhere in the space"
          ],
          "flexible_attributes": [
            "Exact equipment count/arrangement",
            "Camera angle relative to this zone"
          ],
          "generation_rule": "Use reference_asset_01 as a style/atmosphere reference for the gym's general character — adapt freely to the scene's composition."
        }
      }
    ],

    "Relationships": [
      "entity_01 is actively using entity_02 — physically engaged with the rack, mid-rep, weight in hand or on shoulders/chest depending on exercise chosen",
      "entity_03 is positioned behind or to the side of entity_01/entity_02, visible but not the point of focus — it grounds the scene as Anytime Fitness Sai Ying Pun",
      "entity_04 recedes beyond entity_02/entity_03, establishing that this is one continuous, larger gym floor rather than an isolated set"
    ],

    "DepthStructure": {
      "foreground": "entity_01 (student) and entity_02 (Torque rack with colorful plates)",
      "midground": "entity_03 (AF wall + functional rig), positioned behind/beside the foreground action",
      "background": "entity_04 (broader gym floor — ceiling, treadmill row, additional equipment) receding into soft depth"
    },

    "GenerationRequirements": [
      "Single subject only — no additional people, staff, or background extras",
      "All three reference assets (entity_02, entity_03, entity_04) must originate from a single coherent, physically continuous gym space — not three disconnected rooms",
      "No legible text other than the existing 'AF' monogram and 'ANYTIME FITNESS' wordmark already present in the reference assets — no invented signage, posters, or screen text",
      "No competitor branding anywhere in frame",
      "Lighting and color grading must unify all entities into one consistent photographic scene (see Stage 6 for specifics)"
    ],

    "ClientPreferenceConflicts": []
  },

  "ReferenceAssetManifest": [
    {
      "prompt_reference_id": "reference_asset_01",
      "source_filename": "gym_photo_01.jpg",
      "entity_id": "entity_04",
      "asset_type": "Environmental (style/atmosphere reference)",
      "preservation_priority": "Medium",
      "recognizability_requirement": "Approximate Match"
    },
    {
      "prompt_reference_id": "reference_asset_02",
      "source_filename": "gym_photo_02.jpg",
      "entity_id": "entity_02",
      "asset_type": "Product/Equipment",
      "preservation_priority": "High",
      "recognizability_requirement": "Close Match"
    },
    {
      "prompt_reference_id": "reference_asset_03",
      "source_filename": "gym_photo_03.jpg",
      "entity_id": "entity_03",
      "asset_type": "Brand-Bearing Environment",
      "preservation_priority": "Critical",
      "recognizability_requirement": "Close Match (Exact Match for 'AF' wordmark)"
    }
  ]
}
```

## Handoff Note

`ReferenceAssetManifest` travels downstream unchanged to Stage 8 (Prompt Compiler), which will use it to produce the `BRAND_ASSETS` block and to attach the three source images to the generation API call. The user must re-supply `gym_photo_01.jpg`, `gym_photo_02.jpg`, and `gym_photo_03.jpg` (the three photos provided in this conversation) at generation time, mapped to `reference_asset_01/02/03` respectively.

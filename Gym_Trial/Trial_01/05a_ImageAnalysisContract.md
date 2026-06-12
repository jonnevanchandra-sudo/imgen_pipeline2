# Image Analysis Contract — Anytime Fitness Sai Ying Pun (Stage 5.0)

Framework: `5a Image_Analysis.md`
Inputs: 3 venue photos supplied directly in this conversation (no filenames provided — referred to here as `gym_photo_01.jpg`, `gym_photo_02.jpg`, `gym_photo_03.jpg`, in upload order). BrandContract (Stage 0) + CampaignContract (Stage 1).

## Client Intent Declaration

The client did not provide a per-image intent table. Their stated intent — *"I want my gym to be used as the background... I'll be injecting it again when I want to generate the image"* — is interpreted as a single declaration applying to all three images:

```
Asset: gym_photo_01.jpg, gym_photo_02.jpg, gym_photo_03.jpg
Lock categories: Environment / Venue (all three); Brand Assets (gym_photo_03 — "AF" wall monogram + "Anytime Fitness" wordmark on the punching bag)
Strictness: Close Match — the generated gym must be recognizable as this specific club, but minor adaptation to lighting/composition is acceptable
Exclusions: none stated
```

This interpretation is recorded in `ClientConfirmationRequired` below as non-blocking — proceeding under this assumption.

```json
{
  "ImageAnalysisContract": {

    "Metadata": {
      "brand": "Anytime Fitness Sai Ying Pun",
      "campaign": "New member acquisition — HKU students",
      "framework": "Image Analysis Framework v1.0",
      "stage": "5.0 — Asset Extraction",
      "reference_images_provided": 3,
      "generation_mode": "Partial Generation (reference-guided)"
    },

    "AssetInventory": [
      {
        "asset_id": "asset_01",
        "filename": "gym_photo_01.jpg",
        "classification": ["Environmental"],
        "entity_assignment": "entity_04",
        "client_intent": "Use as the general gym-floor/atmosphere reference — overall ceiling, flooring, equipment density"
      },
      {
        "asset_id": "asset_02",
        "filename": "gym_photo_02.jpg",
        "classification": ["Environmental", "Product/Equipment"],
        "entity_assignment": "entity_02",
        "client_intent": "Use this specific free-weight rack and its colorful bumper plates as the equipment the subject trains with"
      },
      {
        "asset_id": "asset_03",
        "filename": "gym_photo_03.jpg",
        "classification": ["Brand-Bearing", "Environmental"],
        "entity_assignment": "entity_03",
        "client_intent": "Use this functional-training zone, including the 'AF' wall monogram and 'Anytime Fitness' wordmark, as the brand-recognition anchor"
      }
    ],

    "PreservationContracts": [
      {
        "asset_id": "asset_01",
        "entity_id": "entity_04",
        "classification": "Environmental",
        "preservation_priority": "Medium",
        "recognizability_requirement": "Approximate Match",

        "observations": [
          "Indoor commercial gym floor",
          "Dark/black ceiling with exposed black ductwork, conduit, and an HVAC unit",
          "Square recessed white LED ceiling panels arranged in a grid",
          "Black rubber tile flooring with a yellow-and-black diagonal hazard stripe on a low platform",
          "A grey structural pillar near the left side",
          "A black Precor-branded multi-station cable/lat-pulldown machine in the right foreground",
          "A row of black-and-silver treadmills with small individual screens receding into the background on the right",
          "Additional benches and plate-loaded machines visible on the left",
          "Mirrored wall visible in the background",
          "No people present"
        ],

        "immutable_attributes": [
          { "attribute": "Dark industrial ceiling with exposed ductwork and a grid of square recessed LED panels", "confidence": null, "notes": "directly observable" },
          { "attribute": "Black rubber tile flooring with yellow-and-black hazard striping accents", "confidence": null, "notes": "directly observable" },
          { "attribute": "Cardio equipment row (treadmills) and Precor-branded strength machines present", "confidence": null, "notes": "directly observable" }
        ],

        "flexible_attributes": [
          { "attribute": "Exact camera angle / which equipment is in the foreground", "reason": "Generated image will recompose around the subject; this image informs general atmosphere, not an exact viewpoint" },
          { "attribute": "Number and arrangement of treadmills/machines visible", "reason": "Incidental to recognizability — overall character matters more than exact count" }
        ],

        "uncertainties": [],

        "generation_instruction": "Use as a general atmosphere/style reference for the gym floor — industrial ceiling, black tile flooring with hazard-stripe accents, modern Precor equipment. Adapt camera angle and exact equipment arrangement to fit the scene's composition."
      },
      {
        "asset_id": "asset_02",
        "entity_id": "entity_02",
        "classification": "Environmental + Product/Equipment",
        "preservation_priority": "High",
        "recognizability_requirement": "Close Match",

        "observations": [
          "A silver 'TORQUE USA' half-rack/squat-rack system with an integrated flat bench",
          "Loaded with bumper plates: large green plates, mid-size grey plates, yellow plates, and a blue plate, stacked on the rack's storage horns",
          "A barbell resting in the rack's J-hooks",
          "Mirror reflections showing additional racks and a 'PRECOR'-branded machine in the background",
          "Black rubber flooring beneath the rack",
          "No people present"
        ],

        "immutable_attributes": [
          { "attribute": "Silver 'TORQUE USA' rack/bench combination structure", "confidence": null, "notes": "directly observable, brand text legible" },
          { "attribute": "Color-coded bumper plate set: green (largest), grey, yellow, and blue plates", "confidence": null, "notes": "directly observable" }
        ],

        "flexible_attributes": [
          { "attribute": "Exact plate quantity/arrangement on the storage horns", "reason": "Incidental detail — the colorful plate set reads as identity, exact count does not" },
          { "attribute": "Whether the bench attachment is visible in frame", "reason": "Depends on final composition/crop" }
        ],

        "uncertainties": [],

        "generation_instruction": "Reproduce from reference_asset_02 — the silver Torque USA rack with its distinctive green/grey/yellow/blue bumper-plate set should be recognizable as the equipment the subject is using. Do not generate a generic black power rack from training data."
      },
      {
        "asset_id": "asset_03",
        "entity_id": "entity_03",
        "classification": "Brand-Bearing + Environmental",
        "preservation_priority": "Critical",
        "recognizability_requirement": "Close Match (Exact Match for the 'AF' wordmark itself)",

        "observations": [
          "A black overhead functional-training rig with multiple cable attachment points spanning the ceiling area",
          "A black punching bag hanging from the rig, printed with the 'ANYTIME FITNESS' wordmark",
          "A wood-paneled accent wall behind the rig bearing a large white 'AF' monogram/wordmark in a clean sans-serif",
          "Purple rubber flooring distinguishing this functional-training zone from the main black-tile floor",
          "A Precor-branded cable column machine and a black bench to the right of the rig",
          "A wall-mounted fan and an HVAC duct visible above",
          "No people present"
        ],

        "immutable_attributes": [
          { "attribute": "White 'AF' monogram/wordmark on the wood-paneled wall — exact lettering, proportions, and placement", "confidence": null, "notes": "directly observable; this is the gym's core brand mark" },
          { "attribute": "'ANYTIME FITNESS' wordmark printed on the hanging punching bag", "confidence": null, "notes": "directly observable" },
          { "attribute": "Purple rubber flooring in this zone", "confidence": null, "notes": "directly observable; matches Anytime Fitness global brand color (Stage 0)" },
          { "attribute": "Black overhead functional-training rig with hanging bag and cable attachment points", "confidence": null, "notes": "directly observable" }
        ],

        "flexible_attributes": [
          { "attribute": "Exact viewing angle of the rig/wall", "reason": "Will adapt to the generated scene's composition" },
          { "attribute": "Presence/visibility of the side cable machine and bench", "reason": "Incidental to brand recognition — the wall + rig + flooring carry the identity" }
        ],

        "uncertainties": [
          { "attribute": "Whether the 'AF' wordmark must be fully legible and unobstructed in the final composition, or may be partially visible/cropped", "confidence": 0.5, "recommended_action": "Default to 'recognizable but may be partially framed' (Close Match); confirm with client if full, unobstructed legibility is required" }
        ],

        "generation_instruction": "Reproduce from reference_asset_03 — the white 'AF' monogram on the wood-paneled wall, the purple flooring, and the black functional rig with 'ANYTIME FITNESS'-branded punching bag should be recognizable in the background of the generated scene. Do not redraw the 'AF' monogram from memory."
      }
    ],

    "SceneAssemblyHandoff": {
      "entity_source_map": [
        { "entity_id": "entity_01", "source": "Generated", "asset_id": null, "generation_mode": "Generate from campaign context — HKU-aged student, no reference photo supplied" },
        { "entity_id": "entity_02", "source": "Reference Asset", "asset_id": "asset_02", "generation_mode": "Preserve — match reference_asset_02" },
        { "entity_id": "entity_03", "source": "Reference Asset", "asset_id": "asset_03", "generation_mode": "Preserve — match reference_asset_03" },
        { "entity_id": "entity_04", "source": "Reference Asset", "asset_id": "asset_01", "generation_mode": "Style/atmosphere reference — match reference_asset_01 loosely" }
      ],
      "partial_generation_note": "entity_01 (the student) is fully generated from campaign context. entity_02 and entity_03 are reference-locked at Close Match and must be recognizable. entity_04 is a looser atmosphere reference (Approximate Match) establishing the broader gym-floor character."
    },

    "ClientConfirmationRequired": [
      {
        "asset_id": "all",
        "attribute": "Client Intent Declaration was inferred from the client's general instruction, not itemized per image",
        "question": "Confirm Environment/Venue lock at Close Match for all three photos, with Brand Assets lock on the 'AF' wall monogram and 'Anytime Fitness' wordmark in gym_photo_03 — is this correct, or should any image be treated as Style Reference only (looser adaptation)?",
        "blocking": false
      },
      {
        "asset_id": "asset_03",
        "attribute": "AF wordmark legibility requirement",
        "question": "Should the 'AF' wall monogram be fully legible and unobstructed in the final image, or is partial/cropped visibility acceptable?",
        "blocking": false
      }
    ]
  }
}
```

## Handoff Note

All three reference images travel forward to Stage 5 (Scene Assembly) alongside this contract, and onward to Stage 8 (Prompt Compiler) as a `ReferenceAssetManifest` for attachment to the image-generation API call — per the user's note that they will re-supply these photos at generation time.

# Image Analysis Contract — FIT24 (Stage 5.0)

Framework: `5a Image_Analysis.md`
Inputs: 1 venue photo supplied directly in this conversation, referred to here as `gym_photo_fit24_01.jpg`. BrandContract (Stage 0) + CampaignContract (Stage 1).

## Client Intent Declaration

The client did not provide a per-image intent table. Their stated intent — *"I want an advertisement with that background... I'm gonna inject this image as an asset package again later"* — is interpreted as a single declaration:

```
Asset: gym_photo_fit24_01.jpg
Lock category: Environment / Venue + Brand Assets (FIT24 wall logo)
Strictness: Close Match — the generated gym must be recognizable as this specific location, but minor adaptation to lighting/composition is acceptable
Exclusions: none stated
```

This interpretation is recorded in `ClientConfirmationRequired` below as non-blocking — proceeding under this assumption.

```json
{
  "ImageAnalysisContract": {

    "Metadata": {
      "brand": "FIT24",
      "campaign": "New member acquisition — urban young professionals (Morning Mile)",
      "framework": "Image Analysis Framework v1.0",
      "stage": "5.0 — Asset Extraction",
      "reference_images_provided": 1,
      "generation_mode": "Partial Generation (reference-guided)"
    },

    "AssetInventory": [
      {
        "asset_id": "asset_01",
        "filename": "gym_photo_fit24_01.jpg",
        "classification": ["Brand-Bearing", "Environmental"],
        "entity_assignment": "entity_02",
        "client_intent": "Use this entire space — window wall with green outdoor view, treadmill row, FIT24 logo, exposed ceiling — as the recognizable backdrop for the ad"
      }
    ],

    "PreservationContracts": [
      {
        "asset_id": "asset_01",
        "entity_id": "entity_02",
        "classification": "Brand-Bearing + Environmental",
        "preservation_priority": "Critical",
        "recognizability_requirement": "Close Match (Exact Match for the 'FIT24' wall logo itself)",

        "observations": [
          "Floor-to-ceiling glass wall along one side of the room, looking out onto a green, tree-lined outdoor area with planters and outdoor seating",
          "A circular blue-and-white 'FIT24' logo mounted on the wall, visible through/near the glass frontage",
          "A row of black treadmills with individual screens, all facing the windows",
          "Black exposed ceiling with visible ductwork, conduit, pendant-style lighting, and ceiling-mounted split-unit air conditioners",
          "Polished grey/dark tile flooring with reflections",
          "A partition wall and additional gym equipment visible in the background to the right",
          "Bright daylight entering through the windows, dominant light source",
          "No people present"
        ],

        "immutable_attributes": [
          { "attribute": "Circular blue-and-white 'FIT24' logo — exact shape, lettering, and color", "confidence": null, "notes": "directly observable; this is the location's core brand mark" },
          { "attribute": "Floor-to-ceiling window wall with a green, tree-lined outdoor view", "confidence": null, "notes": "directly observable; the location's most distinctive visual signature" },
          { "attribute": "Row of black treadmills facing the windows", "confidence": null, "notes": "directly observable" },
          { "attribute": "Black exposed ceiling with ductwork and ceiling-mounted AC units", "confidence": null, "notes": "directly observable" }
        ],

        "flexible_attributes": [
          { "attribute": "Exact viewing angle / how much of the window wall vs. treadmill row is in frame", "reason": "Will adapt to the generated scene's composition" },
          { "attribute": "Visibility of the background partition wall and additional equipment", "reason": "Incidental detail — the window wall, logo, and treadmill row carry the identity" },
          { "attribute": "Time-of-day lighting intensity", "reason": "Composition & Rendering may adjust brightness/warmth while keeping the space recognizable" }
        ],

        "uncertainties": [
          { "attribute": "Whether the 'FIT24' logo must be fully legible and unobstructed in the final composition, or may be partially visible/cropped", "confidence": 0.5, "recommended_action": "Default to 'recognizable but may be partially framed' (Close Match); confirm with client if full, unobstructed legibility is required" }
        ],

        "generation_instruction": "Reproduce from reference_asset_01 — the window wall with its green outdoor view, the circular 'FIT24' logo, the treadmill row, and the exposed dark ceiling should be recognizable in the generated scene. Do not redraw the FIT24 logo from training data."
      }
    ],

    "SceneAssemblyHandoff": {
      "entity_source_map": [
        { "entity_id": "entity_01", "source": "Generated", "asset_id": null, "generation_mode": "Generate from campaign context — young professional, no reference photo supplied" },
        { "entity_id": "entity_02", "source": "Reference Asset", "asset_id": "asset_01", "generation_mode": "Preserve — match reference_asset_01" }
      ],
      "partial_generation_note": "entity_01 (the runner) is fully generated from campaign context. entity_02 (the FIT24 space — window wall, logo, treadmill row, ceiling) is reference-locked at Close Match and must be recognizable."
    },

    "ClientConfirmationRequired": [
      {
        "asset_id": "asset_01",
        "attribute": "Client Intent Declaration was inferred from the client's general instruction, not itemized",
        "question": "Confirm Environment/Venue + Brand Assets lock at Close Match for this photo (window wall, FIT24 logo, treadmill row) — is this correct, or should it be treated as Style Reference only (looser adaptation)?",
        "blocking": false
      },
      {
        "asset_id": "asset_01",
        "attribute": "FIT24 logo legibility requirement",
        "question": "Should the 'FIT24' wall logo be fully legible and unobstructed in the final image, or is partial/cropped visibility acceptable?",
        "blocking": false
      }
    ]
  }
}
```

## Handoff Note

The reference image travels forward to Stage 5 (Scene Assembly) alongside this contract, and onward to Stage 8 (Prompt Compiler) as a `ReferenceAssetManifest` for attachment to the image-generation API call — per the user's note that they will re-supply this photo (as part of an asset package) at generation time.

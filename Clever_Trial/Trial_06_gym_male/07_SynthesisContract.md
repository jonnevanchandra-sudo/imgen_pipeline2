```json
{
  "SynthesisContract": {
    "Metadata": {
      "brand": "CLEVER Protein",
      "campaign": "日本製清蛋白 · 輕盈恢復力 — male post-workout light recovery trial acquisition",
      "framework": "Synthesis v7.1",
      "stage": "7 — Communication Resolution",
      "variant": "Trial_06_gym_male",
      "upstream_contracts": [
        "Trial_06_gym_male/01_CampaignContract.md",
        "Trial_06_gym_male/02_StrategyContract.md",
        "Trial_06_gym_male/03_NarrativeContract.md",
        "Trial_06_gym_male/04_ArtDirectionContract.md",
        "Trial_06_gym_male/05a_ImageAnalysisContract.md",
        "Trial_06_gym_male/05_SceneContract.md",
        "Trial_06_gym_male/06_CompositionRenderingContract.md"
      ],
      "inherits_from": "None — this Synthesis consolidates Trial_06_gym_male's own from-scratch 01–06 chain only. It does not consume any Trial_04_gym or Trial_04_gym_male contract."
    },

    "EntitySummary": [
      { "entity_id": "entity_01", "role": "Male protagonist — lean athletic build, identity locked from reference_asset_03 + reference_asset_04", "hierarchy": "Secondary" },
      { "entity_id": "entity_02", "role": "CLEVER Clear Protein pouch (lemon)", "hierarchy": "Primary" },
      { "entity_id": "entity_03", "role": "Clear lemon protein drink in transparent shaker", "hierarchy": "Primary" },
      { "entity_id": "entity_04", "role": "CLEVER logo + Made-in-Japan brand cue", "hierarchy": "Supporting" },
      { "entity_id": "entity_05", "role": "Clean studio floor + rolled mat", "hierarchy": "Supporting" },
      { "entity_id": "entity_06", "role": "Bright studio windows / sky-blue diffused background", "hierarchy": "Supporting" },
      { "entity_id": "entity_07", "role": "On-image ad typography: '日日飲，激發體能' / '日本製·清蛋白'", "hierarchy": "Secondary" }
    ],

    "CommunicationAllocation": {
      "MustSurvive": [
        "Clear, refreshing lemon protein drink as the hero — not a heavy bro-shake",
        "Male protagonist's identity (face/hair from reference_asset_03 + reference_asset_04) and lean-not-bulky build",
        "On-image headline '日日飲，激發體能' and subtitle '日本製 · 清蛋白' fully legible",
        "CLEVER brand logo and Japanese-made cue",
        "Bright, airy, window-lit studio mood — no heavy gym or dark supplement aesthetic"
      ],
      "Suppressed": [
        "Any mid-exercise activity, sweating, or straining — scene is strictly post-workout cool-down",
        "Wardrobe, pose, background, or any baked-in logo/text/UI graphic from the two reference images — none of that is scene content"
      ]
    },

    "ConflictResolutions": [
      {
        "conflict": "Two separate reference images (image7.png mid-plank, image (1).png standing by a window) show the same identity but in unrelated poses, wardrobe, and — for image (1).png — with pre-existing ad text/logo/UI baked into the frame.",
        "resolution": "Treat both strictly as face/hair/build identity sources only (per 05a_ImageAnalysisContract PreservationContract), cross-validating the same person. Discard all pose, wardrobe, background, and overlay content from both. The new on-image headline and CLEVER lockup are generated fresh per ArtDirectionContract.TypographicIntent, not copied from image (1).png's baked-in text.",
        "owning_layer": "Synthesis"
      },
      {
        "conflict": "Narrative/Art Direction calls for a lean, capable, non-bulky male build, while image7.png shows visible toned muscle mid-plank that could be read as more defined than intended.",
        "resolution": "Build is locked at 'lean, athletic, toned — not bodybuilder-bulky' per PreservationContract.immutable_attributes; the post-workout cool-down framing (calm expression, relaxed stance) keeps the read aligned with 'capable, not muscle-flexing' per ArtDirection anti_cliche_rules.",
        "owning_layer": "Synthesis"
      }
    ],

    "PhysicalRendering": {
      "CameraSpecs": {
        "focal_length_mm": "85mm",
        "aperture_f_stop": "f/4",
        "depth_of_field_category": "Atmospheric"
      },
      "LightingSummary": "Bright, soft natural daylight from large studio windows as key; gentle fill; specular glint on glass/liquid; even bright background exposure to keep white typography legible.",
      "MaterialSummary": "Glass/liquid transparency with light condensation; matte pouch vs glossy shaker; lightweight athletic fabric; natural, unfiltered human skin rendering with visible texture and a light post-workout flush."
    },

    "RenderingConstraintsCarried": {
      "natural_skin_rendering_required": true,
      "face_reference_reproduction_required": true,
      "face_reference_sources": ["reference_asset_03", "reference_asset_04"],
      "typography_legibility_required": true,
      "pose_variation_required": false
    },

    "ClientConfirmationRequired": [
      "Headline copy '日日飲，激發體能' was transcribed from a low-resolution screenshot of image (1).png and has not been independently verified — confirm exact characters before final generation."
    ],

    "FinalDirectives": {
      "must_attach_reference_images": ["image1.png", "image4.png", "image7.png", "image (1).png"],
      "generation_notes": [
        "Attach image1.png as reference_asset_01 (CLEVER pack/product) and image4.png as reference_asset_02 (CLEVER logo) per ReferenceAssetManifest.",
        "Attach image7.png as reference_asset_03 and image (1).png as reference_asset_04 — both used for identity only, cross-validated against each other.",
        "Do not reproduce any pose, wardrobe, background, or pre-existing text/logo/UI overlay from image7.png or image (1).png.",
        "Render the new ad headline and subtitle fresh, per ArtDirectionContract.TypographicIntent — not copied from any reference image."
      ]
    }
  }
}
```

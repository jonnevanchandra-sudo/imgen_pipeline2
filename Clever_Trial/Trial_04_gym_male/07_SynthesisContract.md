```json
{
  "SynthesisContract": {
    "Metadata": {
      "brand": "CLEVER Protein",
      "campaign": "日本製輕盈美學 — gym variant, male model post-workout light recovery",
      "framework": "Synthesis v7.1",
      "stage": "7 — Communication Resolution",
      "variant": "Trial_04_gym_male — bright yoga/fitness studio, male model from image 6.png, on-image ad typography",
      "upstream_contracts": [
        "BrandContract (contract.md)",
        "CampaignContract (01_CampaignContract.md)",
        "StrategyContract (02_StrategyContract.md)",
        "NarrativeContract (03_NarrativeContract.md)",
        "ArtDirectionContract (04_ArtDirectionContract.md)",
        "ImageAnalysisContract (05a_ImageAnalysisContract.md)",
        "SceneContract (05_SceneContract.md)",
        "CompositionRenderingContract (06_CompositionRenderingContract.md)"
      ],
      "new_creative_decisions_introduced": false
    },

    "StrategicResolution": {
      "resolved_theme": "Post-workout lightness — Japanese clear protein is the smart gym-goer's recovery ritual, not a heavy shake.",
      "activated_dimensions_carried": ["Accessibility (Critical)", "Performance (Critical)", "Confidence (High)", "Innovation (Medium)", "Heritage (Medium)"],
      "suppressed_tensions": [
        "The 'Performance Orthodoxy' barrier (heavy shake = effective protein) is resolved by visual proof: the clear, pale-yellow drink is visibly high-quality and clean, not watered-down."
      ],
      "audience_takeaway_confirmed": "After a yoga/fitness session, CLEVER clear Japanese protein is the obvious, guilt-free recovery choice — light, refreshing, and genuinely high-protein. Not a heavy, chalky shake."
    },

    "NarrativeResolution": {
      "emotional_arc_confirmed": "Post-workout warmth + reluctance to undo the lightness → calm, refreshing recovery ritual that extends the workout's lightness rather than contradicting it.",
      "identity_landing": "Smart, lean, modern gym-goer who recovers with Japanese clear protein — his active self and his health-conscious self are finally aligned.",
      "key_visual_proof_points": [
        "The clear pale-yellow drink in the transparent shaker is the visible proof that protein can be light and refreshing.",
        "The male model's calm, lightly satisfied expression (reproduced from reference_asset_03) confirms the ritual feels good, not like a chore.",
        "The bright, airy yoga studio setting communicates 'this is wellness, not a supplement counter.'"
      ],
      "suppressed_communications": [
        "Suppress: any hint of intensity, strain, or bodybuilding — the narrative is recovery, not performance.",
        "Suppress: medical-sounding claims — functional benefits travel only on the product packaging (entity_02).",
        "Suppress: generic wellness clichés (before/after body shots, weighing scales, heavy sweat imagery)."
      ]
    },

    "VisualResolution": {
      "visual_concept_confirmed": "Gym Light-Recovery Ritual — post-yoga cool-down as a personal light-wellness moment in a bright, window-lit studio.",
      "hierarchy_confirmed": [
        "Primary: Clear lemon drink (entity_03) + CLEVER lemon pack (entity_02) — hero product cluster",
        "Secondary: Male model's calm expression and lean athletic posture (entity_01) — emotional proof; face reproduced from reference_asset_03",
        "Secondary: On-image typography overlay (entity_07) — editorial voice naming the moment",
        "Supporting: CLEVER logo + Made in Japan cue (entity_04)",
        "Supporting: Clean gym floor + rolled yoga mat (entity_05)",
        "Background: Bright gym windows softened to sky-blue bokeh plane (entity_06)"
      ],
      "attention_flow_confirmed": "Foreground hero product cluster → male model's face → ad headline in window-light background → brand cue → clean floor/mat",
      "anti_cliches_enforced": [
        "No heavy dumbbells or weight machines in frame",
        "No sweating or straining",
        "No dark gym surfaces",
        "No mirror wall background",
        "No other people"
      ]
    },

    "PhysicalRendering": {
      "CameraSpecs": {
        "focal_length_mm": "85mm",
        "aperture_f_stop": "f/4",
        "depth_of_field_category": "Atmospheric",
        "framing": "eye-level near medium shot"
      },
      "LightingSpecs": {
        "key_source": "Natural daylight from large floor-to-ceiling gym windows",
        "quality": "Soft, high-key, directional",
        "background_exposure": "Bright but controlled — the window zone must be luminous enough for the ad typography to read as white text floating in light, not washed out completely",
        "hero_product_lighting": "Cleanest, most direct light on the shaker and pack; gentle specular glint on the glass",
        "skin_tone": "Warm-neutral; slight healthy post-workout flush — never orange"
      },
      "MaterialSpecs": {
        "drink": "Clear, pale-yellow, translucent — light physically passes through; never opaque or milky",
        "shaker": "Glass-clear body; light condensation; CLEVER logo clearly on body",
        "pack": "White matte pouch; bright yellow lemon band; dark-blue CLEAR PROTEIN typography",
        "active_wear": "Light athletic t-shirt (white or light blue, lightweight moisture-wicking fabric) — same register as in reference image 6.png",
        "floor": "Light wood or pale rubber — clean, minimal"
      },
      "SkinRendering": "Natural pores, fine lines, subtle tone variation, light post-workout flush. No airbrushing. No beauty filter. Reproduce the male model's natural skin register from reference_asset_03 (image 6.png)."
    },

    "TypographyResolution": {
      "headline": "告別運動後重裝感！",
      "subtitle": "日本製 · 清蛋白",
      "typography_style": "Bold modern sans-serif; clean, confident, no decorative elements",
      "text_color": "White",
      "placement": "Upper portion of the frame, within the bright gym window-light background plane; above and clear of the male model's face and product hero cluster",
      "legibility_requirement": "Fully legible at mobile screen size; white text must maintain sufficient contrast against the bright but controlled window-light background",
      "function": "The headline ('告別運動後重裝感！') names the moment the image shows — the editorial voice that makes the ad intent explicit. The subtitle ('日本製 · 清蛋白') anchors the product claim. Together they ensure the image reads as an advertisement, not merely a lifestyle photo."
    },

    "EntitySummary": [
      {
        "entity_id": "entity_01",
        "role": "Identity proof — calm, lightly flushed East Asian male, mid-to-late twenties, lean healthy build, light athletic t-shirt, post-workout cool-down",
        "generation": "Reproduced from reference_asset_03 (image 6.png); near exact face and hair match; discard shaker and outdoor background from that image"
      },
      {
        "entity_id": "entity_02",
        "role": "Hero brand product — CLEVER lemon CLEAR PROTEIN pouch",
        "generation": "Reproduce from reference_asset_01 (image1.png); near exact match"
      },
      {
        "entity_id": "entity_03",
        "role": "Hero drink — transparent shaker with clear pale-yellow lemon protein",
        "generation": "Reproduce from reference_asset_01 (image1.png); near exact match; clear liquid mandatory"
      },
      {
        "entity_id": "entity_04",
        "role": "Brand identity — CLEVER logo + Made in Japan cue",
        "generation": "Reproduce CLEVER wordmark from reference_asset_02 (image4.png); exact match"
      },
      {
        "entity_id": "entity_05",
        "role": "Scene anchor — clean gym floor + rolled yoga mat",
        "generation": "Generated; near-empty floor with single yoga mat prop only"
      },
      {
        "entity_id": "entity_06",
        "role": "Background — bright gym with large floor-to-ceiling windows; sky-blue natural light",
        "generation": "Generated; softens to glowing bokeh plane at f/4; carries typography"
      },
      {
        "entity_id": "entity_07",
        "role": "Campaign-mandatory on-image typography — headline + subtitle",
        "generation": "Generated; white text; upper background zone; critical legibility requirement"
      }
    ],

    "ConflictResolutions": [
      {
        "conflict": "Window background brightness vs. typography legibility",
        "resolution": "The window zone is bright and glowing but must not be completely blown out — background exposure is controlled so white text maintains at least moderate contrast."
      },
      {
        "conflict": "Gym setting (fitness brand code) vs. light-wellness campaign (not hardcore gym)",
        "resolution": "The gym is coded as yoga/pilates studio — large windows, clean light floor, rolled yoga mat. No heavy equipment. The fitness context signals aspiration while the studio aesthetic removes the 'gym bro supplement' association."
      },
      {
        "conflict": "Post-workout skin (light flush) vs. natural skin rendering requirement",
        "resolution": "The post-workout flush is a natural, authentic skin state. The natural_skin_rendering_required constraint prohibits airbrushing and beauty filters, not natural color variation. The male model's skin register from reference_asset_03 is reproduced with texture intact."
      },
      {
        "conflict": "Male model reference face vs. active-wear styling",
        "resolution": "The male model's face and hair are reproduced from reference_asset_03 (image 6.png). Clothing shifts to a CLEVER-context light athletic t-shirt (same light blue / white register as the reference image). The outdoor sky background in image 6.png is discarded; the indoor gym studio environment is fully generated."
      }
    ],

    "FinalDirectives": [
      "The transparent shaker with the clear pale-yellow lemon drink is the single most important visual element — it must be the brightest, sharpest, most specular-lit object in the frame.",
      "The CLEVER lemon CLEAR PROTEIN pouch must be reproduced exactly from reference_asset_01 (image1.png) — do not generate packaging from training data.",
      "The male model's face and hair must be reproduced from reference_asset_03 (image 6.png) — East Asian male, mid-to-late twenties, short dark hair, lean build. Discard the shaker and outdoor background from that image.",
      "The ad headline '告別運動後重裝感！' and subtitle '日本製 · 清蛋白' must be present in the upper window-light background zone and legible at mobile screen size.",
      "The background must be a bright yoga/pilates studio with large floor-to-ceiling windows — not a dark gym, not a mirror wall, not the outdoor sky from image 6.png.",
      "85mm f/4 — carry these CameraSpecs verbatim to the Prompt Compiler CAMERA block.",
      "Natural skin rendering: visible pores, light post-workout flush, no beauty filter — reproduce the male model's natural texture from reference_asset_03.",
      "Only three elements on the gym floor/midground zone: the male model, the pack, the shaker. The rolled yoga mat is the only additional environmental prop.",
      "Attach three reference images to the API call: image1.png (reference_asset_01), image4.png (reference_asset_02), image 6.png (reference_asset_03)."
    ]
  }
}
```

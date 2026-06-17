```json
{
  "SynthesisContract": {
    "Metadata": {
      "brand": "CLEVER Protein",
      "campaign": "日本製輕盈美學 — HK OL post-workout light recovery trial acquisition",
      "framework": "Synthesis v7.1",
      "stage": "7 — Communication Resolution",
      "variant": "Trial_04_gym — bright yoga/fitness studio, on-image ad typography",
      "upstream_contracts": [
        "BrandContract (contract.md)",
        "CampaignContract (01_CampaignContract.md)",
        "StrategyContract (02_StrategyContract.md)",
        "NarrativeContract (03_NarrativeContract.md)",
        "ArtDirectionContract (04_ArtDirectionContract.md)",
        "SceneContract (05_SceneContract.md)",
        "CompositionRenderingContract (06_CompositionRenderingContract.md)"
      ],
      "new_creative_decisions_introduced": false
    },

    "StrategicResolution": {
      "resolved_theme": "Post-workout lightness — Japanese clear protein is the modern HK OL's gym recovery ritual, not a heavy shake.",
      "activated_dimensions_carried": ["Accessibility (Critical)", "Performance (Critical)", "Confidence (High)", "Innovation (Medium)", "Heritage (Medium)"],
      "suppressed_tensions": [
        "The 'Performance Orthodoxy' barrier (heavy shake = effective protein) is resolved by visual proof: the clear, pale-yellow drink is visibly high-quality and clean, not watered-down."
      ],
      "audience_takeaway_confirmed": "If I want to recover light and smart after my yoga/fitness session, CLEVER clear Japanese protein is the obvious, guilt-free choice — not a heavy, chalky shake."
    },

    "NarrativeResolution": {
      "emotional_arc_confirmed": "Post-workout warmth + reluctance to undo lightness → calm, refreshing recovery ritual that extends the workout's lightness rather than contradicting it.",
      "identity_landing": "Smart, light-beauty gym OL who recovers with Japanese clear protein — her active self and her beauty self are finally aligned.",
      "key_visual_proof_points": [
        "The clear pale-yellow drink in the transparent shaker is the visible proof that protein can be light and refreshing.",
        "The OL's calm, lightly satisfied expression confirms the ritual feels good, not like a chore.",
        "The bright, airy yoga studio setting communicates 'this is wellness, not a supplement counter.'"
      ],
      "suppressed_communications": [
        "Suppress: any hint of intensity, strain, or bodybuilding — the narrative is recovery, not performance.",
        "Suppress: medical-sounding claims — functional benefits travel only on the product packaging (entity_02), not in the environment.",
        "Suppress: generic wellness clichés (girl laughing alone, salad, before/after body shots)."
      ]
    },

    "VisualResolution": {
      "visual_concept_confirmed": "Gym Light-Recovery Ritual — post-yoga cool-down as a personal light-beauty moment in a bright, window-lit studio.",
      "hierarchy_confirmed": [
        "Primary: Clear lemon drink (entity_03) + CLEVER lemon pack (entity_02) — hero product cluster",
        "Secondary: OL's calm expression and active-wear posture (entity_01) — emotional proof",
        "Secondary: On-image typography overlay (entity_07) — editorial voice naming the moment",
        "Supporting: CLEVER logo + Made in Japan cue (entity_04)",
        "Supporting: Clean gym floor + rolled yoga mat (entity_05)",
        "Background: Bright gym windows softened to sky-blue bokeh plane (entity_06)"
      ],
      "attention_flow_confirmed": "Foreground hero product cluster → OL's face → ad headline in window-light background → brand cue → clean floor/mat",
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
        "active_wear": "White mesh/crochet crop top texture; pastel lemon-yellow shorts",
        "floor": "Light wood or pale rubber — clean, minimal"
      },
      "SkinRendering": "Natural pores, fine lines, subtle tone variation, light post-workout flush. No airbrushing. No beauty filter. No plastic or wax sheen."
    },

    "TypographyResolution": {
      "headline": "告別運動後重裝感！",
      "subtitle": "日本製 · 清蛋白",
      "typography_style": "Bold modern sans-serif; clean, confident, no decorative elements",
      "text_color": "White",
      "placement": "Upper portion of the frame, within the bright gym window-light background plane; above and clear of the OL's face and product hero cluster",
      "legibility_requirement": "Fully legible at mobile screen size; white text must maintain sufficient contrast against the bright but controlled window-light background",
      "function": "The headline ('告別運動後重裝感！') names the moment the image shows — it is the editorial voice that makes the ad intent explicit. The subtitle ('日本製 · 清蛋白') anchors the product claim. Together they ensure the image reads as an advertisement, not merely a lifestyle photo."
    },

    "EntitySummary": [
      {
        "entity_id": "entity_01",
        "role": "Identity proof — calm, lightly flushed HK OL in white mesh crop top + pastel yellow shorts, post-workout cool-down",
        "generation": "Fully generated; loose match persona"
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
        "resolution": "The window zone is bright and glowing but must not be completely blown out — background exposure is controlled so white text maintains at least moderate contrast. The typography is placed within this controlled bright zone, not in a pure overexposed white area."
      },
      {
        "conflict": "Gym setting (fitness brand code) vs. light-beauty campaign (not hardcore gym)",
        "resolution": "The gym is coded as yoga/pilates studio throughout — large windows, clean light floor, rolled yoga mat. No heavy equipment. This resolves the tension: the fitness context signals aspiration and active lifestyle, while the yoga-studio aesthetic code removes the 'gym bro supplement' association."
      },
      {
        "conflict": "Post-workout skin (light flush) vs. natural skin rendering requirement",
        "resolution": "The post-workout flush is a natural, authentic skin state — this is captured as real warmth (not orange, not heavy sweat). The natural_skin_rendering_required constraint is fully compatible with a light flush; it prohibits airbrushing and beauty filters, not natural color variation."
      }
    ],

    "FinalDirectives": [
      "The transparent shaker with the clear pale-yellow lemon drink is the single most important visual element — it must be the brightest, sharpest, most specular-lit object in the frame.",
      "The CLEVER lemon CLEAR PROTEIN pouch must be reproduced exactly from reference_asset_01 — do not generate packaging from training data.",
      "The ad headline '告別運動後重裝感！' and subtitle '日本製 · 清蛋白' must be present in the upper window-light background zone and legible at mobile screen size.",
      "The OL must wear white mesh/crochet crop top + pastel/lemon-yellow workout shorts — this is the key visual bridge to the brand's existing female active-wear imagery (image3, image4).",
      "The background must be a bright yoga/pilates studio with large floor-to-ceiling windows — not a dark gym, not a mirror wall, not an outdoor setting.",
      "85mm f/4 — carry these CameraSpecs verbatim to the Prompt Compiler CAMERA block.",
      "Natural skin rendering: visible pores, light post-workout flush, no beauty filter.",
      "Only three elements on the gym floor/midground zone: the OL, the pack, the shaker. The rolled yoga mat is the only additional environmental prop."
    ]
  }
}
```

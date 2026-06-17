```json
{
  "SynthesisContract": {
    "Metadata": {
      "brand": "CLEVER Protein",
      "campaign": "日本製輕盈美學 — HK OL afternoon tea trial acquisition",
      "framework": "Synthesis v7.1",
      "stage": "7 — Communication Resolution",
      "variant": "Trial_05_office — office desk setting, female model face from image 5.png, on-image ad typography",
      "upstream_contracts": [
        "BrandContract (contract.md)",
        "CampaignContract (Trial_04_office/01_CampaignContract.md)",
        "StrategyContract (Trial_04_office/02_StrategyContract.md)",
        "NarrativeContract (Trial_04_office/03_NarrativeContract.md)",
        "ArtDirectionContract (Trial_04_office/04_ArtDirectionContract.md)",
        "ImageAnalysisContract (05a_ImageAnalysisContract.md)",
        "SceneContract (05_SceneContract.md)",
        "CompositionRenderingContract (06_CompositionRenderingContract.md)"
      ],
      "new_creative_decisions_introduced": false
    },

    "StrategicResolution": {
      "resolved_theme": "3:30pm guilt-free light-beauty ritual — Japanese clear protein replaces the afternoon snack at the office desk.",
      "activated_dimensions_carried": ["Accessibility (Critical)", "Performance (Critical)", "Confidence (High)", "Innovation (Medium)", "Heritage (Medium)"],
      "suppressed_tensions": [
        "The 'Category Misfit' barrier (protein is heavy/gym-only) is resolved by visual proof: the clear, pale-yellow drink on a clean desk looks nothing like a gym shake."
      ],
      "audience_takeaway_confirmed": "Swapping my 3:30pm snack for this Japanese clear protein is an easy, guilt-free upgrade — light, refreshing, and it fits right into my afternoon break."
    },

    "NarrativeResolution": {
      "emotional_arc_confirmed": "Mid-afternoon desk fatigue + guilt about snacking → calm, light satisfaction of a smart, image-aligned choice.",
      "identity_landing": "Smart, light-beauty office lady who has quietly upgraded her 3:30pm ritual — the drink in her hand signals who she's becoming.",
      "key_visual_proof_points": [
        "The clear pale-yellow drink in the transparent shaker is the visible proof that protein can be light and refreshing.",
        "The female model's calm, lightly satisfied expression (reproduced from reference_asset_03) confirms the ritual feels good, not like a sacrifice.",
        "The near-empty, clean desk communicates 'intentional' — this is a curated moment, not an impulse snack."
      ],
      "suppressed_communications": [
        "Suppress: any hint of gym culture, bodybuilding, or heavy supplement imagery.",
        "Suppress: medical or curative health claims — functional benefits live on the pack only.",
        "Suppress: guilt or body shaming — the emotional register is pride and lightness, not fear or restriction."
      ]
    },

    "VisualResolution": {
      "visual_concept_confirmed": "Office Light-Beauty Ritual — 3:30pm desk break reframed as a personal light-beauty moment with Japanese clear protein.",
      "hierarchy_confirmed": [
        "Primary: Clear lemon drink (entity_03) + CLEVER lemon pack (entity_02) — hero product cluster",
        "Secondary: Female model's calm expression and office-wear posture (entity_01) — emotional proof; face reproduced from reference_asset_03",
        "Secondary: On-image typography overlay (entity_07) — editorial voice naming the moment",
        "Supporting: CLEVER logo + Made in Japan cue (entity_04)",
        "Supporting: Clean desk surface + 3:30 clock (entity_05)",
        "Background: Flat sky-blue plane softened by DoF (entity_06)"
      ],
      "attention_flow_confirmed": "Foreground hero product cluster → model's face → ad headline in background → brand cue → clean desk surface",
      "anti_cliches_enforced": [
        "No gym, dumbbells, or heavy supplement aesthetics",
        "No cluttered desk",
        "No before/after body imagery",
        "No generic wellness stock photo clichés"
      ]
    },

    "PhysicalRendering": {
      "CameraSpecs": {
        "focal_length_mm": "85mm",
        "aperture_f_stop": "f/4",
        "depth_of_field_category": "Atmospheric",
        "framing": "eye-level near medium shot at desk distance"
      },
      "LightingSpecs": {
        "key_source": "Soft high-key daylight (controlled studio quality)",
        "quality": "Bright, soft, even — no harsh shadows",
        "background_exposure": "Evenly lit flat sky-blue plane — consistent exposure ensures typography reads cleanly; no pooling shadows or bright spots",
        "hero_product_lighting": "Cleanest, most direct light on shaker and pack; gentle specular glint on glass",
        "skin_tone": "Warm-neutral; never orange"
      },
      "MaterialSpecs": {
        "drink": "Clear, pale-yellow, translucent — light physically passes through; never opaque or milky",
        "shaker": "Glass-clear body; light condensation; CLEVER logo clearly on body",
        "pack": "White matte pouch; bright yellow lemon band; dark-blue CLEAR PROTEIN typography",
        "office_wear": "Polished-casual blouse or fitted top — clean, professional, not athletic",
        "desk": "Near-empty clean surface; small 3:30 clock the only additional prop"
      },
      "SkinRendering": "Natural pores, fine lines, subtle tone variation, natural asymmetry. No airbrushing. No beauty filter. Reproduce the female model's natural complexion register from reference_asset_03 (image 5.png)."
    },

    "TypographyResolution": {
      "headline": "告別3點3罪惡感！",
      "subtitle": "日本製 · 清蛋白",
      "typography_style": "Bold modern sans-serif; clean, confident, no decorative elements",
      "text_color": "White or dark-blue — whichever reads best against the sky-blue background",
      "placement": "Upper portion of the frame, within the clean sky-blue background plane; above and clear of the model's face and product hero cluster",
      "legibility_requirement": "Fully legible at mobile screen size",
      "function": "The headline ('告別3點3罪惡感！') names the moment the image shows — the editorial voice making ad intent explicit. The subtitle ('日本製 · 清蛋白') anchors the product claim. Together they ensure the image reads as an advertisement, not merely a lifestyle photo."
    },

    "EntitySummary": [
      {
        "entity_id": "entity_01",
        "role": "Identity proof — calm, lightly satisfied East Asian female, early-to-mid twenties, neat hair bun, polished-casual office wear, seated at desk on afternoon break",
        "generation": "Reproduced from reference_asset_03 (image 5.png); near exact face and hair match; dress in office wear; discard sports bra, shaker, and outdoor background from that image"
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
        "role": "Scene anchor — clean desk surface with small 3:30 clock",
        "generation": "Generated; near-empty desk with clock the only prop beyond pack and shaker"
      },
      {
        "entity_id": "entity_06",
        "role": "Background — flat sky-blue plane; softens to smooth DoF bokeh; carries typography",
        "generation": "Generated; no furniture, windows, or clutter behind subject"
      },
      {
        "entity_id": "entity_07",
        "role": "Campaign-mandatory on-image typography — headline + subtitle",
        "generation": "Generated; white or dark-blue text; upper background zone; critical legibility requirement"
      }
    ],

    "ConflictResolutions": [
      {
        "conflict": "Female model from image 5.png is wearing a sports bra — this must not appear in the office setting",
        "resolution": "Only the model's face, hair bun, and overall build are reproduced. Clothing is fully replaced by polished-casual office wear. The outdoor mountain background from image 5.png is discarded entirely and replaced by the generated sky-blue office backdrop."
      },
      {
        "conflict": "Natural skin rendering requirement vs. reference face reproduction",
        "resolution": "The model's natural complexion from image 5.png is already naturally textured and unpretouched — reproducing it faithfully satisfies the natural_skin_rendering_required constraint. No beauty filter is applied on top."
      },
      {
        "conflict": "Typography legibility vs. sky-blue background lightness",
        "resolution": "Background exposure is controlled so it reads as a smooth sky-blue plane — neither too bright (which would wash out white text) nor too dark (which would fight the CLEVER brand register). Dark-blue text is the fallback if white reads insufficiently against the sky-blue."
      }
    ],

    "FinalDirectives": [
      "The transparent shaker with the clear pale-yellow lemon drink is the single most important visual element — it must be the brightest, sharpest, most specular-lit object in the frame.",
      "The CLEVER lemon CLEAR PROTEIN pouch must be reproduced exactly from reference_asset_01 (image1.png) — do not generate packaging from training data.",
      "The female model's face and neat hair bun must be reproduced from reference_asset_03 (image 5.png) — East Asian female, early-to-mid twenties, clean bun, bright natural complexion. Dress her in polished-casual office wear. Discard sports bra, shaker, and outdoor background from that image.",
      "The ad headline '告別3點3罪惡感！' and subtitle '日本製 · 清蛋白' must be present in the upper background zone and legible at mobile screen size.",
      "The background must be a flat, clean sky-blue plane — no visible office furniture, no windows, no clutter behind the subject.",
      "85mm f/4 — carry these CameraSpecs verbatim to the Prompt Compiler CAMERA block.",
      "Natural skin rendering: visible pores, natural asymmetry, no beauty filter — reproduce the model's natural texture from reference_asset_03.",
      "Only three objects on the desk surface: the pack, the shaker, and the small 3:30 clock.",
      "Attach three reference images to the API call: image1.png (reference_asset_01), image4.png (reference_asset_02), image 5.png (reference_asset_03)."
    ]
  }
}
```

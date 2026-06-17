```json
{
  "CompositionRenderingContract": {
    "Metadata": {
      "brand": "CLEVER Protein",
      "campaign": "日本製輕盈美學 — gym variant, male model post-workout light recovery",
      "framework": "Composition & Rendering v6.1",
      "stage": "6 — Visual Expression",
      "variant": "Trial_04_gym_male — bright yoga/fitness studio, male model from image 6.png, on-image ad typography"
    },

    "HierarchyPlan": [
      {
        "element": "entity_03",
        "hierarchy_level": "Primary",
        "luminance_priority": "Brightest",
        "reason": "The clear lemon drink in the transparent shaker is the single differentiating hero — the natural window light catches the glass and liquid first, making it the most luminous and visually striking element in the frame.",
        "source": "Preservation"
      },
      {
        "element": "entity_02",
        "hierarchy_level": "Primary",
        "luminance_priority": "Brightest",
        "reason": "The lemon CLEAR PROTEIN pouch co-anchors the hero cluster. Brand legibility is mandatory; the white pack surface reflects the window light cleanly and must be clearly readable alongside the shaker.",
        "source": "Preservation"
      },
      {
        "element": "entity_01",
        "hierarchy_level": "Secondary",
        "luminance_priority": "Mid",
        "reason": "The male model's calm, post-workout expression and lean athletic build are the emotional proof of the recovery ritual — read after the hero product cluster, never outshining it. His face, reproduced from reference_asset_03, must be clearly recognizable.",
        "source": "Narrative"
      },
      {
        "element": "entity_07",
        "hierarchy_level": "Secondary",
        "luminance_priority": "Mid",
        "reason": "On-image ad headline ('告別運動後重裝感！' + '日本製·清蛋白') is a campaign-mandatory element — white text in the bright window-light background zone is legible but does not compete with the hero product cluster. It occupies the background breathing room above and behind the male model.",
        "source": "Campaign"
      },
      {
        "element": "entity_04",
        "hierarchy_level": "Supporting",
        "luminance_priority": "Mid",
        "reason": "CLEVER logo + Made-in-Japan cue — required branding legibility; supporting not focal.",
        "source": "Preservation"
      },
      {
        "element": "entity_05",
        "hierarchy_level": "Supporting",
        "luminance_priority": "Dimmest",
        "reason": "The clean gym floor and rolled yoga mat anchor the scene moment; must read as a gym context but never compete with the hero cluster.",
        "source": "Environmental"
      },
      {
        "element": "entity_06",
        "hierarchy_level": "Supporting",
        "luminance_priority": "Bright but diffused",
        "reason": "The large gym windows are bright but their light is softened by depth-of-field into a smooth, glowing sky-blue plane — they frame the subject and carry the typography without creating competing focal points.",
        "source": "Environmental"
      }
    ],

    "AttentionPlan": {
      "entry_element": "entity_03",
      "attention_progression": ["entity_03", "entity_02", "entity_01", "entity_07", "entity_04", "entity_05"],
      "exit_element": "entity_06",
      "mechanisms": ["luminance_contrast", "sharpness_hierarchy", "depth_separation", "gaze_vectors", "typographic_anchor"],
      "reason": "Eye lands on the clear bright drink (sharpest, specular-lit, foreground), joins the pack as a brand cluster, rises to the male model's calm expression for the emotional read, then catches the white ad headline floating in the bright window-light background zone — the headline names what the image just showed. Brand cue and clean window light confirm the ritual context."
    },

    "VisualFlowPlan": {
      "flow_direction": "diagonal_clockwise",
      "flow_pattern": "golden_spiral",
      "supports": ["AttentionPlan"],
      "reason": "Gentle spiral from the foreground hero product cluster up to the male model's face and relaxed posture, then outward to the ad headline in the upper window-light background zone. The bright, near-empty gym space gives breathing room so the spiral feels natural and unhurried."
    },

    "CameraPlan": {
      "perspective_intent": "eye_level",
      "framing_intent": "medium_shot",
      "distance_intent": "near",
      "focal_length_mm": "85mm",
      "depth_of_field_category": "Atmospheric",
      "aperture_f_stop": "f/4",
      "supports": ["HierarchyPlan"],
      "source": "Hierarchy",
      "reason": "85mm at f/4 gives flattering compression and keeps the male model and product proportionally natural. Atmospheric DoF softens the gym windows in the background into a smooth, glowing sky-blue plane while keeping the typography legible. Commercial Isolation (f/1.8–f/2.8) unnecessary and would risk blurring the headline."
    },

    "LightingPlan": {
      "supports": ["HierarchyPlan"],
      "source": "Hierarchy",
      "intent": ["depth_perception", "emotional_interpretation", "subject_separation", "typography_legibility"],
      "possible_techniques": [
        "natural_daylight_key_from_gym_windows",
        "soft_fill_from_studio_walls_to_minimize_harsh_shadows",
        "specular_glint_on_glass_and_liquid",
        "even_bright_background_exposure_for_typography_readability"
      ],
      "reason": "Bright, soft, natural daylight flooding in from the large gym windows is the key light source. The clear shaker and pack receive the cleanest, most direct light with a gentle specular glint. The male model is lit by the same natural window light — warm-neutral on skin, healthy, light post-workout flush, never orange. The background window zone is bright and evenly lit so the typography overlay reads as white text floating cleanly in a glowing window plane. No harsh gym spotlights or artificial light."
    },

    "MaterialPlan": {
      "supports": ["HierarchyPlan"],
      "source": "Hierarchy",
      "intent": ["tactile_credibility", "emotional_interpretation"],
      "possible_techniques": [
        "glass_and_liquid_transparency",
        "light_condensation_on_shaker",
        "matte_pouch_surface_vs_glossy_glass",
        "lightweight_athletic_fabric_texture",
        "natural_gym_floor_texture"
      ],
      "human_skin_rendering": "Natural skin texture visible — pores, fine lines, subtle tone variation and a slight healthy flush from post-workout warmth. No airbrushing, no beauty filter, no plastic or wax sheen. Reproduce the male model's natural skin register from reference_asset_03.",
      "reason": "Liquid clarity is the most important material truth. Light condensation on the shaker reinforces 'cold and refreshing after a warm workout.' Matte pack surface vs. glossy shaker body creates material contrast. The lightweight athletic t-shirt fabric adds tactile authenticity to the sportswear read without the visual weight of heavy gym gear."
    },

    "AtmosphericPlan": {
      "supports": ["VisualFlowPlan"],
      "source": "Emotion",
      "intent": ["depth_perception", "environmental_mood", "post_workout_release"],
      "possible_techniques": ["natural_window_light_key", "high_key_airy_fill", "clean_bright_background_exposure"],
      "reason": "Bright, open, airy atmosphere carries the 'post-workout release and lightness' emotion. The large gym windows make the background feel like the studio is breathing — light and space. The typography reads as floating cleanly in that light. The overall atmosphere should evoke: 'this is the best moment of the gym session.'"
    },

    "OpticalPlan": {
      "supports": ["AttentionPlan"],
      "source": "Attention",
      "intent": ["attention_guidance", "perceptual_credibility", "typography_legibility"],
      "possible_techniques": ["progressive_depth_falloff", "gentle_specular_on_product", "window_bokeh_softening"],
      "bokeh_behavior": "Progressive, depth-dependent falloff at 85mm f/4: foreground pack and shaker are crisply sharp; the male model remains sharp to softly diffuse by depth; the bright gym windows in the background soften further into a smooth, glowing sky-blue/white plane. The typography, sitting in this background window-light zone, softens slightly but remains fully legible. No flat uniform blur. No blown-out bright spots that wash out the text.",
      "reason": "At 85mm f/4, large bright windows in the background produce a naturally beautiful, smooth luminous bokeh. The typography reads as a designed overlay floating in that glow. The window light must be bright but not over-exposed to the point where white text becomes invisible."
    },

    "RenderingConstraints": {
      "reality_model_compliance": true,
      "preservation_compliance": true,
      "hierarchy_protection": true,
      "natural_skin_rendering_required": true,
      "pose_variation_required": false,
      "typography_legibility_required": true,
      "face_reference_reproduction_required": true,
      "face_reference_note": "The male model's face must be reproduced from reference_asset_03 (image 6.png) with natural skin texture intact — no beauty filter applied to the reference face.",
      "typography_legibility_note": "On-image headline '告別運動後重裝感！' and subtitle '日本製·清蛋白' must be fully legible at mobile screen size. White text must maintain sufficient contrast against the bright gym window-light background."
    },

    "PerceptualValidation": {
      "SkinNaturalismAssertion": "Rendered skin must show visible pores, fine lines, and subtle tone variation with a light healthy flush from post-workout warmth — no smoothing, no beauty filter. Face must remain recognizable as the reference in image 6.png.",
      "DepthOfFieldRealismAssertion": "Bokeh must follow progressive depth-dependent falloff from 85mm f/4 — no flat cutout blur. The gym window background must soften to a smooth luminous plane.",
      "TypographyLegibilityAssertion": "Ad headline '告別運動後重裝感！' must be readable as text at mobile screen size — white text against the bright gym window-light background must maintain clear contrast. Not distorted, not partially obscured by the male model or product, not washed out by the window brightness."
    }
  }
}
```

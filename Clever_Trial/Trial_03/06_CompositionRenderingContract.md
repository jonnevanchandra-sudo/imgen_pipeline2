```json
{
  "CompositionRenderingContract": {
    "Metadata": {
      "brand": "CLEVER Protein",
      "campaign": "日本製輕盈美學 — HK OL afternoon tea trial acquisition",
      "framework": "Composition & Rendering v6.1",
      "stage": "6 — Visual Expression"
    },

    "HierarchyPlan": [
      {
        "element": "entity_03",
        "hierarchy_level": "Primary",
        "luminance_priority": "Brightest",
        "reason": "The clear lemon drink in the transparent shaker is the single differentiating hero — 'protein that behaves like a refreshing drink.' Must be the first thing the eye sees and must read as clear and translucent.",
        "source": "Preservation"
      },
      {
        "element": "entity_02",
        "hierarchy_level": "Primary",
        "luminance_priority": "Brightest",
        "reason": "The lemon CLEAR PROTEIN pouch co-anchors the hero cluster. Brand legibility is a mandatory requirement; pack must be clearly readable alongside the shaker.",
        "source": "Preservation"
      },
      {
        "element": "entity_01",
        "hierarchy_level": "Secondary",
        "luminance_priority": "Mid",
        "reason": "The OL's calm, guilt-free expression and body language are emotional proof of the ritual — read after the hero product cluster, never outshining it.",
        "source": "Narrative"
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
        "reason": "The minimal desk surface (with 3:30 clock) anchors the scene moment; must read but never compete.",
        "source": "Environmental"
      },
      {
        "element": "entity_06",
        "hierarchy_level": "Supporting",
        "luminance_priority": "Dimmest",
        "reason": "The clean background exists only to frame the subject — no competing luminance, no bright spots.",
        "source": "Environmental"
      }
    ],

    "AttentionPlan": {
      "entry_element": "entity_03",
      "attention_progression": ["entity_03", "entity_02", "entity_01", "entity_04", "entity_05"],
      "exit_element": "entity_06",
      "mechanisms": ["luminance_contrast", "sharpness_hierarchy", "depth_separation", "gaze_vectors"],
      "reason": "Eye lands on the clear bright drink (brightest, sharpest, foreground), immediately joins the pack as a brand cluster, rises to the OL's relaxed face for the emotional read, then brand/logo and finally the clean surrounding space confirms the ritual context. Minimal mechanisms — the low structural density means hierarchy is already natural without heavy intervention."
    },

    "VisualFlowPlan": {
      "flow_direction": "diagonal_clockwise",
      "flow_pattern": "golden_spiral",
      "supports": ["AttentionPlan"],
      "reason": "Gentle spiral from the foreground hero cluster up to the OL's face allows the eye to circulate naturally within the clean frame. The near-empty background and desk give generous breathing room so the spiral doesn't feel rushed or crowded."
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
      "reason": "85mm at f/4 gives a slightly compressed, flattering perspective that keeps the OL and product proportionally natural without wide-angle distortion — appropriate for a polished social-commerce lifestyle shot. Eye-level near medium keeps the peer-to-peer 'aspiring self' relationship. Atmospheric DoF (f/4): the background softens gracefully but does not dissolve — the clean sky-blue backdrop reads as an intentional empty space, not a blurred-out mess. At 85mm even f/4 produces a gentle, smooth background falloff that will make the already-minimal background feel even cleaner. Commercial Isolation (f/1.8–f/2.8) is unnecessary here because the background is already empty — deep bokeh on a blank wall adds nothing."
    },

    "LightingPlan": {
      "supports": ["HierarchyPlan"],
      "source": "Hierarchy",
      "intent": ["depth_perception", "emotional_interpretation", "subject_separation"],
      "possible_techniques": [
        "soft_high_key_daylight_key",
        "gentle_fill_to_minimize_shadow_on_background",
        "specular_glint_on_glass_and_liquid",
        "slight_rim_light_on_subject_edge"
      ],
      "reason": "Bright, soft, high-key light establishes the clean Japanese refreshment mood from brand contract. The clear shaker and pack receive the cleanest, most direct light — a gentle specular glint on the glass makes the liquid look crisp and refreshing. The OL is lit a touch softer, warm-neutral on skin. The background is lit evenly and cleanly (fills shadows) so it reads as a flat, controlled sky-blue plane — no shadows pooling in corners, no uneven gradients that create visual noise. No bright practical light sources (windows, lamps) visible behind the subject — the background must not emit luminance that competes with the product hero. Skin is warm-neutral, never orange, no harsh shadows, no studio-flatness either."
    },

    "MaterialPlan": {
      "supports": ["HierarchyPlan"],
      "source": "Hierarchy",
      "intent": ["tactile_credibility", "emotional_interpretation"],
      "possible_techniques": [
        "glass_and_liquid_transparency",
        "light_condensation_on_shaker",
        "matte_pouch_surface_vs_glossy_glass",
        "natural_fabric_behavior_on_wardrobe"
      ],
      "human_skin_rendering": "Natural skin texture visible — pores, fine lines, subtle tone variation and asymmetry appropriate to a woman in her mid-to-late twenties. No airbrushing, no beauty filter, no plastic or wax sheen. Healthy, lightly luminous, real.",
      "reason": "Liquid clarity is the most important material truth in this image: the beverage must read as clear and translucent, with light visibly passing through it. Light condensation on the shaker reinforces 'cold and refreshing.' Matte pack surface vs. glossy shaker body creates material contrast that helps separate the two hero objects. Skin rendered with real texture per the Human Subject Rendering Requirement."
    },

    "AtmosphericPlan": {
      "supports": ["VisualFlowPlan"],
      "source": "Emotion",
      "intent": ["depth_perception", "environmental_mood"],
      "possible_techniques": ["high_key_airy_fill", "clean_background_exposure"],
      "reason": "Airy, clean, high-key atmosphere carries the 'lightness' emotion and reinforces the photoshoot-set quality of the background. No atmospheric haze, no moody shadows, no depth fog. The background should feel like light, clean, empty air."
    },

    "OpticalPlan": {
      "supports": ["AttentionPlan"],
      "source": "Attention",
      "intent": ["attention_guidance", "perceptual_credibility"],
      "possible_techniques": ["progressive_depth_falloff", "gentle_specular_on_product"],
      "bokeh_behavior": "Progressive, depth-dependent falloff consistent with 85mm at f/4: the foreground pack and shaker are crisply sharp; the OL remains sharp to softly diffuse based on her depth from the focal plane; the minimal desk surface softens slightly; the clean background behind the OL softens further into a smooth, even sky-blue plane. Because the background is already near-empty, the bokeh does not need to work hard — it simply ensures the flat blue wall reads as smooth and non-distracting. No flat uniform cutout blur; no ring bokeh from a busy background.",
      "reason": "85mm at f/4 on a near-empty background will produce a naturally elegant, smooth falloff that makes the background read as an intentional design choice, not an oversight."
    },

    "RenderingConstraints": {
      "reality_model_compliance": true,
      "preservation_compliance": true,
      "hierarchy_protection": true,
      "natural_skin_rendering_required": true,
      "pose_variation_required": false
    }
  }
}
```

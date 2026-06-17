```json
{
  "CompositionRenderingContract": {
    "Metadata": {
      "brand": "CLEVER Protein",
      "campaign": "日本製輕盈美學 — HK OL afternoon tea trial acquisition",
      "framework": "Composition & Rendering v6.1",
      "stage": "6 — Visual Expression",
      "variant": "Trial_04_office — office desk, on-image ad typography"
    },

    "HierarchyPlan": [
      {
        "element": "entity_03",
        "hierarchy_level": "Primary",
        "luminance_priority": "Brightest",
        "reason": "The clear lemon drink in the transparent shaker is the single differentiating hero — must be first thing the eye sees and must read as clear and translucent.",
        "source": "Preservation"
      },
      {
        "element": "entity_02",
        "hierarchy_level": "Primary",
        "luminance_priority": "Brightest",
        "reason": "The lemon CLEAR PROTEIN pouch co-anchors the hero cluster. Brand legibility is mandatory; pack must be clearly readable alongside the shaker.",
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
        "element": "entity_07",
        "hierarchy_level": "Secondary",
        "luminance_priority": "Mid",
        "reason": "On-image ad headline ('告別3點3罪惡感！' + '日本製·清蛋白') is a campaign-mandatory element — must be legible but must not compete with the hero product cluster for dominance. It occupies the background zone above and behind the OL.",
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
        "reason": "The minimal desk surface (with 3:30 clock) anchors the scene moment; must read but never compete.",
        "source": "Environmental"
      },
      {
        "element": "entity_06",
        "hierarchy_level": "Supporting",
        "luminance_priority": "Dimmest",
        "reason": "The clean background exists only to frame the subject and carry the typography — no competing luminance, no bright spots.",
        "source": "Environmental"
      }
    ],

    "AttentionPlan": {
      "entry_element": "entity_03",
      "attention_progression": ["entity_03", "entity_02", "entity_01", "entity_07", "entity_04", "entity_05"],
      "exit_element": "entity_06",
      "mechanisms": ["luminance_contrast", "sharpness_hierarchy", "depth_separation", "gaze_vectors", "typographic_anchor"],
      "reason": "Eye lands on the clear bright drink (brightest, sharpest, foreground), joins the pack as a brand cluster, rises to the OL's relaxed face for the emotional read, then catches the ad headline in the background zone — the headline names what the image just showed. Brand/logo and clean space confirm the ritual context."
    },

    "VisualFlowPlan": {
      "flow_direction": "diagonal_clockwise",
      "flow_pattern": "golden_spiral",
      "supports": ["AttentionPlan"],
      "reason": "Gentle spiral from the foreground hero cluster up to the OL's face, then outward to the ad headline in the upper background. The near-empty environment gives breathing room so the spiral feels natural, not rushed."
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
      "reason": "85mm at f/4 gives flattering compression and keeps the OL and product proportionally natural. Atmospheric DoF softens the background into a smooth sky-blue plane while keeping the typography legible — at f/4 with an already-minimal background, the typography sits in a slightly softened but still readable zone. Commercial Isolation (f/1.8–f/2.8) unnecessary; it would risk blurring the headline."
    },

    "LightingPlan": {
      "supports": ["HierarchyPlan"],
      "source": "Hierarchy",
      "intent": ["depth_perception", "emotional_interpretation", "subject_separation", "typography_legibility"],
      "possible_techniques": [
        "soft_high_key_daylight_key",
        "gentle_fill_to_minimize_shadow_on_background",
        "specular_glint_on_glass_and_liquid",
        "even_background_exposure_for_typography_readability"
      ],
      "reason": "Bright, soft, high-key light establishes the clean Japanese refreshment mood. The clear shaker and pack receive the cleanest, most direct light. The OL is lit a touch softer, warm-neutral on skin. The background is evenly lit as a flat, controlled sky-blue plane — consistent exposure in the background zone ensures the typography overlay is readable and not fighting shadow gradients. No bright practical light sources behind the subject."
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
      "human_skin_rendering": "Natural skin texture visible — pores, fine lines, subtle tone variation and asymmetry. No airbrushing, no beauty filter, no plastic or wax sheen. Healthy, lightly luminous, real.",
      "reason": "Liquid clarity is the most important material truth. Light condensation on the shaker reinforces 'cold and refreshing.' Matte pack surface vs. glossy shaker body creates material contrast."
    },

    "AtmosphericPlan": {
      "supports": ["VisualFlowPlan"],
      "source": "Emotion",
      "intent": ["depth_perception", "environmental_mood"],
      "possible_techniques": ["high_key_airy_fill", "clean_background_exposure"],
      "reason": "Airy, clean, high-key atmosphere carries the 'lightness' emotion. The background must feel like clean, open air — so the typography reads as floating cleanly in a designed space, not pasted onto a textured wall."
    },

    "OpticalPlan": {
      "supports": ["AttentionPlan"],
      "source": "Attention",
      "intent": ["attention_guidance", "perceptual_credibility", "typography_legibility"],
      "possible_techniques": ["progressive_depth_falloff", "gentle_specular_on_product"],
      "bokeh_behavior": "Progressive, depth-dependent falloff at 85mm f/4: foreground pack and shaker are crisply sharp; the OL remains sharp to softly diffuse by depth; the clean background softens further into a smooth even sky-blue plane. The typography, sitting in the background plane, softens slightly but remains legible — it is intentionally in the background zone, not the foreground sharpness zone. No flat uniform blur.",
      "reason": "At 85mm f/4, a near-empty background produces a naturally elegant, smooth falloff. The typography reads as a designed overlay element — slightly softened by depth but still fully legible at mobile screen size."
    },

    "RenderingConstraints": {
      "reality_model_compliance": true,
      "preservation_compliance": true,
      "hierarchy_protection": true,
      "natural_skin_rendering_required": true,
      "pose_variation_required": false,
      "typography_legibility_required": true,
      "typography_legibility_note": "On-image headline '告別3點3罪惡感！' and subtitle '日本製·清蛋白' must be fully legible at mobile screen size. Background exposure must be consistent enough to support text contrast."
    },

    "PerceptualValidation": {
      "SkinNaturalismAssertion": "Rendered skin must show visible pores, fine lines, and subtle tone variation — no smoothing or beauty filter.",
      "DepthOfFieldRealismAssertion": "Bokeh must follow progressive depth-dependent falloff from 85mm f/4 — no flat cutout blur.",
      "TypographyLegibilityAssertion": "Ad headline '告別3點3罪惡感！' must be readable as text — not distorted, not partially obscured by the OL or product, not rendered as unreadable marks."
    }
  }
}
```

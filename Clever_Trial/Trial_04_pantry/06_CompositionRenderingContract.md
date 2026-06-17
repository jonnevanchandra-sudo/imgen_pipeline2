```json
{
  "CompositionRenderingContract": {
    "Metadata": {
      "brand": "CLEVER Protein",
      "campaign": "日本製輕盈美學 — HK OL afternoon tea trial acquisition",
      "framework": "Composition & Rendering v6.1",
      "stage": "6 — Visual Expression",
      "variant": "Trial_04_pantry — office pantry/kitchenette, active preparation ritual, on-image ad typography"
    },

    "HierarchyPlan": [
      {
        "element": "entity_03",
        "hierarchy_level": "Primary",
        "luminance_priority": "Brightest",
        "reason": "The clear lemon drink in the transparent shaker is the single differentiating hero — the entire scene is built around this ritual moment. Must be first thing the eye sees; must read as clear, translucent, and refreshing. Held actively by the OL or prominent on the counter.",
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
        "reason": "The OL's calm, purposeful standing posture and expression are emotional proof of the deliberate ritual — read after the hero product cluster. Her standing position gives her a taller presence than the seated office variant; she should read as active and upright without outshining the product.",
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
        "luminance_priority": "Low",
        "reason": "The clean pantry counter surface anchors the scene and hosts the hero product cluster — must read but never compete with the product or the OL.",
        "source": "Environmental"
      },
      {
        "element": "entity_06",
        "hierarchy_level": "Supporting",
        "luminance_priority": "Dimmest",
        "reason": "The pantry background exists only to frame the subject, confirm the pantry setting through minimal cues (water dispenser), and carry the typography in the upper zone — no competing luminance, no bright spots behind the subject.",
        "source": "Environmental"
      }
    ],

    "AttentionPlan": {
      "entry_element": "entity_03",
      "attention_progression": ["entity_03", "entity_02", "entity_01", "entity_07", "entity_04", "entity_05"],
      "exit_element": "entity_06",
      "mechanisms": ["luminance_contrast", "sharpness_hierarchy", "depth_separation", "active_gesture_vectors", "typographic_anchor"],
      "reason": "Eye lands on the clear bright drink (brightest, sharpest, foreground — active in hands or prominent on counter), joins the pack as a brand cluster, rises to the OL's calm purposeful face and active posture for the emotional and behavioral read, then catches the ad headline in the background zone. The headline names what the image just showed. Brand/logo and clean pantry confirm the setting."
    },

    "VisualFlowPlan": {
      "flow_direction": "diagonal_upward",
      "flow_pattern": "gentle_arc",
      "supports": ["AttentionPlan"],
      "reason": "Gentle arc from the foreground hero cluster (counter level) up through the OL's tall standing form to the ad headline in the upper background. The OL's standing posture provides a natural vertical anchor that draws the eye upward — more dynamic than the seated office variant while maintaining calm."
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
      "reason": "85mm at f/4 gives flattering compression; at counter height and near distance, the foreground pack and shaker are crisply sharp while the OL reads sharp-to-gently-soft and the background pantry elements (water dispenser, walls) soften into a gently blurred, recognizable-but-unobtrusive backdrop. Atmospheric f/4 keeps the typography legible in the background zone without requiring Commercial Isolation. Eye-level at counter height ensures the product cluster and the OL's upper body share the frame naturally."
    },

    "LightingPlan": {
      "supports": ["HierarchyPlan"],
      "source": "Hierarchy",
      "intent": ["depth_perception", "emotional_interpretation", "subject_separation", "typography_legibility"],
      "possible_techniques": [
        "soft_high_key_daylight_quality_from_small_window_or_overhead_LED",
        "gentle_fill_to_minimize_shadow_on_background",
        "specular_glint_on_glass_and_liquid",
        "even_background_exposure_for_typography_readability"
      ],
      "reason": "Bright, soft, high-key light establishes the clean Japanese refreshment mood within the pantry context. The clear shaker and pack receive the cleanest, most direct light — a gentle specular glint on the glass makes the drink look crisp and refreshing. The OL is lit a touch softer, warm-neutral on skin. Background is evenly lit as a controlled, clean plane — consistent exposure in the background zone ensures the typography overlay is readable and not fighting pantry surface texture or shadow gradients. No harsh single-direction spotlights. No bright practical light source directly behind the subject."
    },

    "MaterialPlan": {
      "supports": ["HierarchyPlan"],
      "source": "Hierarchy",
      "intent": ["tactile_credibility", "emotional_interpretation"],
      "possible_techniques": [
        "glass_and_liquid_transparency",
        "light_condensation_on_shaker",
        "matte_pouch_surface_vs_glossy_glass",
        "natural_fabric_behavior_on_office_wear",
        "clean_light_counter_surface_with_subtle_material_texture"
      ],
      "human_skin_rendering": "Natural skin texture visible — pores, fine lines, subtle tone variation and asymmetry. No airbrushing, no beauty filter, no plastic or wax sheen. Healthy, lightly luminous, real. Hands visible holding the shaker — natural hand and finger texture.",
      "reason": "Liquid clarity is the most important material truth. Light condensation on the shaker reinforces 'cold and refreshing.' Matte pack surface vs. glossy shaker body creates material contrast. Counter surface should have subtle natural texture (light wood grain or matte stone) without being visually dominant."
    },

    "AtmosphericPlan": {
      "supports": ["VisualFlowPlan"],
      "source": "Emotion",
      "intent": ["depth_perception", "environmental_mood"],
      "possible_techniques": ["high_key_airy_fill", "clean_background_exposure", "minimal_ambient_warmth"],
      "reason": "Bright, clean, purposeful atmosphere. Not cozy-domestic (home kitchen). Not cold-corporate (conference room). The pantry reads as the small, curated, privately-carved space within a busy workday — where a deliberate, light-beauty choice is made. Airy and luminous, consistent with the 'guilt-free lightness' emotional register."
    },

    "OpticalPlan": {
      "supports": ["AttentionPlan"],
      "source": "Attention",
      "intent": ["attention_guidance", "perceptual_credibility", "typography_legibility", "pantry_context_legibility"],
      "possible_techniques": ["progressive_depth_falloff", "gentle_specular_on_product"],
      "bokeh_behavior": "Progressive, depth-dependent falloff at 85mm f/4: foreground pack and shaker are crisply sharp; the OL remains sharp to softly diffuse by depth; the pantry background (water dispenser, walls) softens further into a gently blurred, clean backdrop — recognizable as a pantry through the soft form of the water dispenser but not distractingly detailed. The typography, sitting in the upper background plane, softens slightly but remains fully legible at mobile screen size. No flat uniform blur.",
      "reason": "At 85mm f/4, the pantry background produces a naturally clean falloff. The water dispenser reads as a soft pantry-identifying form without cluttering the frame. The typography reads as a designed overlay element — slightly softened by depth but still fully legible."
    },

    "RenderingConstraints": {
      "reality_model_compliance": true,
      "preservation_compliance": true,
      "hierarchy_protection": true,
      "natural_skin_rendering_required": true,
      "pose_variation_required": false,
      "typography_legibility_required": true,
      "typography_legibility_note": "On-image headline '告別3點3罪惡感！' and subtitle '日本製·清蛋白' must be fully legible at mobile screen size. Background exposure must be consistent enough to support text contrast regardless of whether the pantry wall or the water dispenser form is behind the text."
    },

    "PerceptualValidation": {
      "SkinNaturalismAssertion": "Rendered skin must show visible pores, fine lines, and subtle tone variation — no smoothing or beauty filter. Hands holding the shaker must show natural hand texture, not artificial perfection.",
      "DepthOfFieldRealismAssertion": "Bokeh must follow progressive depth-dependent falloff from 85mm f/4 — the pantry background must be gently blurred and recognizable, not flat-cutout or uniformly blurred.",
      "TypographyLegibilityAssertion": "Ad headline '告別3點3罪惡感！' must be readable as text at mobile screen size — not distorted, not partially obscured by the OL or product cluster, not rendered as unreadable marks, and not fighting background texture from the pantry wall or water dispenser."
    }
  }
}
```

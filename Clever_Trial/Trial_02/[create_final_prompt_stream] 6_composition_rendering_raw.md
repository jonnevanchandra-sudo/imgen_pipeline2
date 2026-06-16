```json
{
  "CompositionRenderingContract": {
    "Metadata": {
      "brand": "CLEVER Protein",
      "campaign": "Clever Protein clear whey HK OL afternoon tea trial acquisition",
      "framework": "Composition & Rendering v6.1",
      "stage": "6 — Visual Expression"
    },

    "HierarchyPlan": [
      {
        "element": "entity_03",
        "hierarchy_level": "Primary",
        "luminance_priority": "Brightest",
        "reason": "Art Direction FocalPriority tier 1: the clear, refreshing lemon drink is the obvious hero of the 3:30 ritual; it must be recognized as a clear drink (not a snack, not a thick shake) first.",
        "source": "Preservation"
      },
      {
        "element": "entity_02",
        "hierarchy_level": "Primary",
        "luminance_priority": "Brightest",
        "reason": "The lemon CLEAR PROTEIN packshot co-anchors the hero with the shaker — brand legibility is a MandatoryRequirement; product + drink read as one focal cluster.",
        "source": "Preservation"
      },
      {
        "element": "entity_01",
        "hierarchy_level": "Secondary",
        "luminance_priority": "Mid",
        "reason": "FocalPriority tier 2: the OL's calm, lightly satisfied, guilt-free state is proof of the ritual's effect — read after the drink, must not outshine the hero.",
        "source": "Narrative"
      },
      {
        "element": "entity_04",
        "hierarchy_level": "Supporting",
        "luminance_priority": "Mid",
        "reason": "CLEVER logo + Made-in-Japan cue — required branding, but legibility-supporting rather than the focal entry point.",
        "source": "Preservation"
      },
      {
        "element": "entity_05",
        "hierarchy_level": "Supporting",
        "luminance_priority": "Dimmest",
        "reason": "FocalPriority tier 3: office-afternoon context (desk, ~3:30 cue, clean light tonality) confirms the moment but must stay quiet; bright windows capped below the hero.",
        "source": "Environmental"
      }
    ],

    "AttentionPlan": {
      "entry_element": "entity_03",
      "attention_progression": ["entity_03", "entity_02", "entity_01", "entity_04", "entity_05"],
      "exit_element": "entity_05",
      "mechanisms": ["luminance_contrast", "sharpness_hierarchy", "gaze_vectors", "depth_separation"],
      "reason": "Eye lands on the clear drink (brightest, sharpest, foreground), reads the adjacent pack as the same brand cluster, then the OL's relaxed gaze/expression confirms the emotional payoff, then logo + office context register as reinforcement. Minimum mechanisms needed for a stable single-focal hierarchy."
    },

    "VisualFlowPlan": {
      "flow_direction": "diagonal_clockwise",
      "flow_pattern": "golden_spiral",
      "supports": ["AttentionPlan"],
      "reason": "A gentle spiral from the foreground drink up to the OL's face and back down to the desk pack keeps the eye circulating within the hero cluster while the airy office holds the negative space — supports the 'calm desk sanctuary' breathing room without a competing second focus."
    },

    "CameraPlan": {
      "perspective_intent": "eye_level",
      "framing_intent": "medium_shot",
      "distance_intent": "near",
      "focal_length_mm": "50mm",
      "depth_of_field_category": "Atmospheric",
      "aperture_f_stop": "f/4",
      "supports": ["HierarchyPlan"],
      "source": "Hierarchy",
      "reason": "Eye-level near medium shot frames the OL with the hero drink/pack in the foreground at desk distance — peer-level, 'this could be me' relationship per SubjectRelationshipLogic. Atmospheric DoF (f/4): the office stays recognizable and the ~3:30 afternoon cue remains legible enough to read context, but is softened so it never competes with the hero. Not Commercial Isolation — the office context carries part of the story (it must read as office-afternoon). Not Environmental Context — a fully sharp background would clutter the clean, light look and pull attention off the drink. 50mm gives a natural, undistorted lifestyle perspective."
    },

    "LightingPlan": {
      "supports": ["HierarchyPlan"],
      "source": "Hierarchy",
      "intent": ["depth_perception", "emotional_interpretation", "subject_separation"],
      "possible_techniques": ["soft_daylight_key", "high_key_clean_fill", "gentle_specular_on_glass"],
      "reason": "Soft, bright, high-key daylight establishes the clean, light, Japanese refreshment mood. The clear drink and pack receive the brightest, cleanest light with a gentle specular highlight on the glass/liquid to read as crisp and refreshing. The OL is lit a touch softer (Mid). Background office light and any window are exposed down so they never outshine the hero cluster — no bright window blowing out behind the subject. Warm-neutral skin, never orange; airy not clinical."
    },

    "MaterialPlan": {
      "supports": ["HierarchyPlan"],
      "source": "Hierarchy",
      "intent": ["tactile_credibility", "emotional_interpretation"],
      "possible_techniques": ["transparent_liquid_clarity", "condensation_on_shaker", "matte_pouch_surface_vs_glossy_glass"],
      "human_skin_rendering": "Visible natural skin texture — pores, fine lines, subtle tone variation and asymmetry appropriate to a woman in her late twenties to early thirties. No airbrushing, no beauty-filter, no plastic/wax sheen. Healthy, lightly luminous but real.",
      "reason": "Liquid clarity is the single most important material truth — the beverage must read clear/translucent, with light passing through it, distinct from any thick/opaque shake. Light condensation on the shaker reinforces 'refreshing'. Matte pouch vs. glossy bottle separates the two product elements. Skin rendered with real texture per the Human Subject Rendering Requirement."
    },

    "AtmosphericPlan": {
      "supports": ["VisualFlowPlan"],
      "source": "Emotion",
      "intent": ["depth_perception", "environmental_mood"],
      "possible_techniques": ["airy_negative_space", "subtle_aerial_softening_of_background"],
      "reason": "Light, airy atmosphere with generous clean negative space conveys 'lightness' and 'guilt-free' emotionally and gives the hero room to breathe. No haze or density that would obscure focal points or muddy the high-key brightness."
    },

    "OpticalPlan": {
      "supports": ["AttentionPlan"],
      "source": "Attention",
      "intent": ["attention_guidance", "perceptual_credibility"],
      "possible_techniques": ["progressive_background_softening", "gentle_specular_glints"],
      "bokeh_behavior": "Progressive depth-dependent falloff consistent with 50mm at f/4: the foreground drink and pack are crisply sharp, the OL is sharp to gently soft depending on her depth from the focal plane, and the office background softens gradually with distance — desk and near objects remain semi-legible (including the ~3:30 afternoon cue), far walls/windows soften more. Smooth, gentle bokeh — never a flat uniform cutout blur, never full dissolve.",
      "reason": "Soft progressive falloff isolates the hero cluster enough to win attention while keeping the office readable as context, matching the Atmospheric DoF category."
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

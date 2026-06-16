# Composition & Rendering Contract — CLEVER Weight Down "3 PM Office Rescue" (Stage 6.1)

Framework: `6.1 Composition_Rendering.md`
Inputs: SceneContract (Stage 5.2.5), RealityModel = Realistic
Decision Type: Visual Expression — hierarchy, attention, camera, rendering behavior.

```json
{
  "CompositionRenderingContract": {

    "HierarchyPlan": [
      {
        "element": "entity_01",
        "hierarchy_level": "Primary",
        "luminance_priority": "Brightest",
        "reason": "The CLEVER Weight Down product is the 'already chosen' object — Art Direction's AttentionControl requires it to claim immediate cognitive priority as the resolved option (entity_01 is also the Critical/Near-Exact ProductSpec-locked entity).",
        "source": "Preservation"
      },
      {
        "element": "entity_03",
        "hierarchy_level": "Secondary",
        "luminance_priority": "Mid",
        "reason": "The hand reaching toward the product reinforces the 'Quiet Swap' relationship (Recognition) without competing with the product itself.",
        "source": "Narrative"
      },
      {
        "element": "entity_02",
        "hierarchy_level": "Secondary",
        "luminance_priority": "Dimmest",
        "reason": "The comparison snack/drink must remain recognizable to carry the contrast, but reads as receded/passed-over — consistent with Art Direction's 'already decided' emotional state and the SceneContract's background placement.",
        "source": "Narrative"
      },
      {
        "element": "entity_04",
        "hierarchy_level": "Supporting",
        "luminance_priority": "Dimmest",
        "reason": "The desk environment grounds the scene as an ordinary mid-afternoon office moment without drawing attention from the product or the contrast.",
        "source": "Environmental"
      }
    ],

    "AttentionPlan": {
      "entry_element": "entity_01",
      "attention_progression": ["entity_01", "entity_03", "entity_02"],
      "exit_element": "entity_02",
      "mechanisms": ["luminance_contrast", "sharpness_hierarchy", "depth_separation"],
      "reason": "Attention enters on the CLEVER product (brightest, sharpest), is reinforced by the hand's reaching gesture toward it, then settles briefly on the softened, dimmer comparison snack/drink in the background — completing the 'Quiet Swap' contrast without it ever out-competing the product."
    },

    "VisualFlowPlan": {
      "flow_direction": "bottom_to_top",
      "flow_pattern": "diagonal_clockwise",
      "supports": ["AttentionPlan"],
      "reason": "The product sits in the lower/foreground portion of the frame closest to the viewer; the hand enters from one side at a similar depth; the comparison items recede diagonally into the upper/background desk area — a calm diagonal path that mirrors the attention progression without abrupt jumps."
    },

    "CameraPlan": {
      "perspective_intent": "high_angle",
      "framing_intent": "close_up",
      "distance_intent": "near",
      "focal_length_mm": "50mm",
      "depth_of_field_category": "Atmospheric",
      "aperture_f_stop": "f/4",
      "supports": ["HierarchyPlan"],
      "source": "Hierarchy",
      "reason": "A high-angle, near-distance view over the desk reads naturally as someone looking down at their own workspace (Recognition). 50mm at f/4 keeps the product (entity_01) and hand (entity_03) crisp while softening the comparison snack/drink (entity_02) and desk surroundings (entity_04) just enough that they remain recognizable but secondary — entity_02 still carries communication value (the contrast), so full isolation (Commercial Isolation) would remove too much of its legibility."
    },

    "LightingPlan": {
      "supports": ["HierarchyPlan"],
      "source": "Hierarchy",
      "intent": ["depth_perception", "subject_separation", "emotional_interpretation"],
      "possible_techniques": ["soft_window_key_light", "gentle_falloff_toward_background"],
      "reason": "Soft, even ambient daylight (consistent with an office interior) keys onto the product and hand as the brightest, clearest area of the frame, with a gentle natural falloff toward the desk background where the comparison snack/drink sits — reinforcing the Brightest/Mid/Dimmest luminance ranking without introducing dramatic or moody lighting that would contradict CLEVER's calm tone."
    },

    "MaterialPlan": {
      "supports": ["HierarchyPlan"],
      "source": "Hierarchy",
      "intent": ["tactile_credibility", "emotional_interpretation"],
      "possible_techniques": ["matte_packaging_finish", "worn_takeaway_material_contrast"],
      "human_skin_rendering": "entity_03's hand shows visible natural skin texture — pores, subtle tone variation, natural knuckle/joint detail — with no airbrushing or 'AI-perfect' smoothing, per the Human Subject Rendering Requirement.",
      "reason": "The CLEVER pouch and shake render with a clean matte/soft-sheen finish consistent with the brand's minimalist packaging, while the takeaway container and cup for entity_02 show ordinary, slightly worn disposable materials — the material contrast itself reinforces 'considered choice' vs. 'grab-and-go' without any added graphic elements."
    },

    "AtmosphericPlan": {
      "supports": ["VisualFlowPlan"],
      "source": "RealityModel",
      "intent": ["depth_perception", "environmental_mood"],
      "possible_techniques": ["clean_interior_ambiance", "soft_daylight_diffusion"],
      "reason": "A clean, softly diffused interior atmosphere (no haze, no stylized color cast) supports the calm, unhurried mood established by Narrative and Art Direction, while the gentle depth gradient helps separate entity_01/entity_03 from the receding entity_02/entity_04."
    },

    "OpticalPlan": {
      "supports": ["AttentionPlan"],
      "source": "Attention",
      "intent": ["attention_guidance", "perceptual_credibility"],
      "possible_techniques": ["gentle_bokeh_falloff", "edge_softening_on_background_objects"],
      "bokeh_behavior": "At 50mm/f/4, the product and hand (foreground, ~near focal plane) remain fully sharp. The comparison snack/drink (entity_02), sitting further back on the desk, shows mild progressive softening — edges and label details lose crispness but overall shapes (takeaway box, cup) remain identifiable. The desk surroundings (entity_04) at the greatest distance show the most softening, with incidental objects reduced to soft, recognizable forms rather than hard bokeh discs.",
      "reason": "This falloff keeps the comparison snack/drink legible enough to read as 'siu mai + iced tea' (required for the contrast) while ensuring it never sharpens to compete with the product — consistent with the Atmospheric category and the Dimmest/Secondary luminance assignment."
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

## Notes

- `natural_skin_rendering_required: true` applies to entity_03 (the single hand) — visible natural texture, no airbrushing.
- `pose_variation_required: false` — only one human element (a hand) is present, with no shared multi-subject action.
- Depth of Field Category: **Atmospheric** (f/4) selected because entity_02 carries communication value (the contrast) and must remain recognizable, ruling out Commercial Isolation; AttentionPlan does not require full background legibility either, ruling out Environmental Context.

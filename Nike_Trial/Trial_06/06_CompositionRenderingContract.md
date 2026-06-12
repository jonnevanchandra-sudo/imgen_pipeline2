# Composition & Rendering Contract — Nike Chill Run Club (Stage 6.1)

Framework: 6.1 Composition_Rendering.md
Inputs: SceneContract (Stage 5.2.5)

```json
{
  "CompositionRenderingContract": {

    "HierarchyPlan": [
      {
        "element": "entity_01",
        "hierarchy_level": "Primary",
        "reason": "The social connection within the group is the core communication (Narrative: isolation → connection); it must claim attention first.",
        "source": "Narrative"
      },
      {
        "element": "entity_02",
        "hierarchy_level": "Secondary",
        "reason": "Nike Pegasus 41 carries a Critical/Near-Exact PreservationContract and a Required visibility note — it must be legible but not dominate over the group's social dynamic.",
        "source": "Preservation"
      },
      {
        "element": "entity_03",
        "hierarchy_level": "Supporting",
        "reason": "The Hong Kong harbourfront establishes setting and atmosphere but is environmental context, not the focal communication.",
        "source": "Environmental"
      }
    ],

    "AttentionPlan": {
      "entry_element": "entity_01",
      "attention_progression": ["entity_01", "entity_02", "entity_03"],
      "exit_element": "entity_03",
      "mechanisms": ["sharpness_hierarchy", "luminance_contrast", "depth_separation"],
      "reason": "Sharp focus and warm key light on the group draw the eye first to faces and interaction; the eye then drops naturally to the legible shoe in the lower frame before drifting out to the softly-lit skyline as atmospheric context."
    },

    "VisualFlowPlan": {
      "flow_direction": "diagonal_clockwise",
      "flow_pattern": "linear_vector",
      "supports": ["AttentionPlan"],
      "reason": "A diagonal arrangement of the group along the promenade leads the eye from the nearest, sharpest figures toward the skyline, reinforcing the entry-to-exit attention path without competing focal points."
    },

    "CameraPlan": {
      "perspective_intent": "eye_level",
      "framing_intent": "full_shot",
      "distance_intent": "near",
      "focal_length_mm": "35mm",
      "aperture_f_stop": "f/2.8",
      "supports": ["HierarchyPlan"],
      "source": "Hierarchy",
      "reason": "Eye-level placement supports the Belonging relationship — the viewer feels like part of the group, not a spectator. A near full-shot at 35mm keeps faces readable while including footwear in the lower frame, satisfying both the Primary (group) and Secondary (Pegasus) hierarchy levels. f/2.8 gives enough separation to soften the skyline without erasing its identity."
    },

    "LightingPlan": {
      "supports": ["HierarchyPlan"],
      "source": "Emotion",
      "intent": ["depth_perception", "emotional_interpretation", "subject_separation"],
      "possible_techniques": ["warm_practical_light_emphasis", "rim_lighting_emphasis"],
      "reason": "Warm streetlight-driven key lighting separates the group from the cooler depth of the harbour and skyline, reinforcing both the 'Mental Reset' emotional warmth and the client's preference for amber over neon-blue tones."
    },

    "MaterialPlan": {
      "supports": ["HierarchyPlan"],
      "source": "Hierarchy",
      "intent": ["tactile_credibility", "emotional_interpretation"],
      "possible_techniques": ["surface_roughness_contrast", "specular_reflection_control"],
      "human_skin_rendering": "Visible pores, natural tone variation, and a subtle post-workday flush on cheeks/forehead — no airbrushing or uniform smoothing.",
      "reason": "Contrasting the soft texture of casual fabrics against the engineered mesh of the Pegasus 41 reinforces the 'real evening, real people' credibility the campaign depends on."
    },

    "AtmosphericPlan": {
      "supports": ["VisualFlowPlan"],
      "source": "RealityModel",
      "intent": ["depth_perception", "environmental_mood"],
      "possible_techniques": ["aerial_perspective", "warm_ambient_glow"],
      "reason": "A light haze softens the distant towers, reinforcing depth and an unhurried evening mood without obscuring the skyline's identity or competing with the group as the focal point."
    },

    "OpticalPlan": {
      "supports": ["AttentionPlan"],
      "source": "Attention",
      "intent": ["attention_guidance", "perceptual_credibility"],
      "possible_techniques": ["bokeh_blur_isolation", "vignette_focus_hold"],
      "bokeh_behavior": "Falloff begins just behind the group: the promenade railing and near water remain semi-legible, while the tower skyline resolves into soft, warm circular bokeh with progressively less detail toward the frame edges.",
      "reason": "Progressive bokeh keeps the skyline recognizable as Hong Kong while ensuring it never out-competes the group for attention."
    },

    "RenderingConstraints": {
      "reality_model_compliance": true,
      "preservation_compliance": true,
      "hierarchy_protection": true,
      "natural_skin_rendering_required": true
    }
  }
}
```

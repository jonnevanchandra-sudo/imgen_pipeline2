# Composition & Rendering Contract — Nike Chill Run Club (Stage 6.1)

Framework: `6.1 Composition_Rendering.md`
Inputs: SceneContract (Stage 5.2.5) — RealityModel, Entities, Relationships, DepthStructure, RelativeScale, PreservationContracts
Decision Type: Visual Expression. Priority order applied: Narrative Clarity > Hierarchy Stability > Attention Guidance > Emotional Reinforcement > Visual Beauty. Human subjects present → natural-skin rendering requirement is in force.

```json
{
  "CompositionRenderingContract": {

    "HierarchyPlan": [
      {
        "element": "entity_01",
        "hierarchy_level": "Primary",
        "reason": "The shared human moment carries the Mental Reset + belonging communication; it must read first.",
        "source": "Narrative"
      },
      {
        "element": "entity_02",
        "hierarchy_level": "Secondary",
        "reason": "Nike Pegasus must remain legible and correctly preserved (Near Exact), but must not out-compete the human signal — product is proof, not hero.",
        "source": "Preservation"
      },
      {
        "element": "entity_03",
        "hierarchy_level": "Secondary",
        "reason": "Promenade grounds the scene as a real HK evening and supports the 'integrated into city life' meaning.",
        "source": "Environmental"
      },
      {
        "element": "entity_04",
        "hierarchy_level": "Supporting",
        "reason": "Skyline provides place identity and depth but stays a distant backdrop.",
        "source": "Environmental"
      }
    ],

    "AttentionPlan": {
      "entry_element": "entity_01",
      "attention_progression": ["entity_01", "entity_02", "entity_03", "entity_04"],
      "exit_element": "entity_04",
      "mechanisms": ["luminance_contrast", "sharpness_hierarchy", "depth_separation"],
      "reason": "Attention should land on the group's faces and interaction first, drop briefly to the shoes mid-stride, then settle into the promenade and skyline. Minimum mechanisms used to hold a stable hierarchy without fragmenting focus."
    },

    "VisualFlowPlan": {
      "flow_direction": "left_to_right",
      "flow_pattern": "linear_vector",
      "supports": ["AttentionPlan"],
      "reason": "The group's lateral mid-stride movement creates a natural left-to-right read that mirrors the eye path from people to footwear to setting, reinforcing the easy forward motion of the run."
    },

    "CameraPlan": {
      "perspective_intent": "eye_level",
      "framing_intent": "full_shot",
      "distance_intent": "mid",
      "focal_length_mm": "35mm",
      "aperture_f_stop": "f/2.8",
      "supports": ["HierarchyPlan"],
      "source": "Hierarchy",
      "reason": "Eye-level places the viewer among the group as a peer (Subject Relationship Logic = belonging). A near full shot from the knees up keeps faces readable while letting at least one subject's shoes enter the lower frame. 35mm holds group + promenade context; f/2.8 separates the group from the skyline without flattening the midground."
    },

    "LightingPlan": {
      "supports": ["HierarchyPlan"],
      "source": "Emotion",
      "intent": ["depth_perception", "emotional_interpretation", "subject_separation"],
      "possible_techniques": ["warm_directional_key_from_streetlamps", "ambient_skyline_fill"],
      "reason": "Warm directional streetlamp light keys the group and lifts them above a softer, cooler background, carrying the 'warm relief / exhale' tone while keeping the subjects clearly separated from the city behind."
    },

    "MaterialPlan": {
      "supports": ["HierarchyPlan"],
      "source": "Emotion",
      "intent": ["tactile_credibility", "emotional_interpretation"],
      "possible_techniques": ["fabric_crease_retention", "surface_roughness_contrast"],
      "human_skin_rendering": "Visible pores, subtle tone variation, and a light post-workday flush; natural asymmetry in expression and posture. No airbrushing, no beauty-filter smoothing.",
      "reason": "Real fabric creases on jackets/bags and a non-glossy, lightly worn shoe surface increase credibility and keep the image from reading as a polished studio render."
    },

    "AtmosphericPlan": {
      "supports": ["VisualFlowPlan"],
      "source": "Emotion",
      "intent": ["depth_perception", "environmental_mood"],
      "possible_techniques": ["light_evening_haze", "aerial_perspective"],
      "reason": "A faint evening haze over the harbour deepens the sense of distance to the skyline and warms the mood without obscuring the foreground group."
    },

    "OpticalPlan": {
      "supports": ["AttentionPlan"],
      "source": "Attention",
      "intent": ["attention_guidance", "perceptual_credibility"],
      "possible_techniques": ["bokeh_blur_isolation"],
      "bokeh_behavior": "Progressive falloff beginning roughly 1–2 m behind the group: the railing and nearby water stay semi-legible, mid-distance towers soften, and the far skyline dissolves into smooth, warm circular bokeh consistent with 35mm at f/2.8. No flat, uniform cutout blur.",
      "reason": "Depth-dependent bokeh isolates the group as the focal point while keeping the HK setting recognizable, guiding attention without a hard background cutout."
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

---

## Reasoning Notes

- **Hierarchy protects preservation, not the reverse:** the Pegasus is held Secondary so its Near-Exact preservation never escalates into a product-hero composition — consistent with Strategy's `forbidden_positioning: ProductHero`.
- **DOF realism:** bokeh is tied explicitly to `35mm / f/2.8` with progressive falloff, satisfying the framework's Depth of Field Realism requirement (no uniform blur layer).
- **Skin naturalism:** human subjects present → `natural_skin_rendering_required: true` and an explicit `human_skin_rendering` description, per the Human Subject Rendering Requirement.
- **Boundary:** no messaging, narrative, scene construction, or preservation decisions changed here — Scene Assembly outputs treated as source truth.

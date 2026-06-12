# Composition & Rendering Contract — Nike Chill Run Club (Stage 6.1, Variant: No Lighting Hierarchy)

Framework: `6.1 Composition_Rendering.md`
Inputs: SceneContract (Stage 5.2.5) — same as `Trial_08/05_SceneContract.md`
Decision Type: Visual Expression — how the scene blueprint is perceptually realized (hierarchy, attention, camera, lighting, materials, atmosphere, optics).

**Variant note:** This is a manually hand-edited fork of `Trial_08/06_CompositionRenderingContract.md`. The **lighting/luminance hierarchy has been removed**: `HierarchyPlan.luminance_priority` is deleted from every entity, `LightingPlan` no longer assigns a brightest/dimmest exposure ranking, `AttentionPlan` no longer uses `luminance_contrast` as an attention mechanism, and `OpticalPlan.bokeh_behavior` no longer makes a brightness comparison between group and skyline. Everything else (HierarchyPlan levels, CameraPlan, MaterialPlan, AtmosphericPlan, depth-of-field structure, RenderingConstraints) is unchanged from the original Trial_08 Stage 6.1 output. This file is the input for re-running Stage 7 and Stage 8.

```json
{
  "CompositionRenderingContract": {

    "HierarchyPlan": [
      {
        "element": "entity_01",
        "hierarchy_level": "Primary",
        "reason": "The group's energized 'mode switch' is the campaign's core communication and must dominate visual attention.",
        "source": "Narrative"
      },
      {
        "element": "entity_02",
        "hierarchy_level": "Secondary",
        "reason": "The Nike Pegasus is a Critical preservation requirement and must be legible, but stays subordinate to the human moment per CampaignContract's Optional/non-hero visibility.",
        "source": "Preservation"
      },
      {
        "element": "entity_03",
        "hierarchy_level": "Secondary",
        "reason": "The West Kowloon promenade/plaza grounds the scene in a real, energetic Hong Kong setting and carries part of the location story (Medium structural density per Art Direction).",
        "source": "Environmental"
      },
      {
        "element": "entity_04",
        "hierarchy_level": "Supporting",
        "reason": "The skyline establishes 'Hong Kong at night' but must never compete with the group for attention.",
        "source": "Environmental"
      }
    ],

    "AttentionPlan": {
      "entry_element": "entity_01",
      "attention_progression": ["entity_01", "entity_02", "entity_03", "entity_04"],
      "exit_element": "entity_04",
      "mechanisms": ["sharpness_hierarchy", "depth_separation", "gaze_vectors"],
      "reason": "Sharpness and depth separation keep the group crispest against a softer environment; the group's own movement direction (gaze/body vectors) leads the eye toward the shoes and then out across the plaza to the skyline, giving a single readable path without competing focal points."
    },

    "VisualFlowPlan": {
      "flow_direction": "diagonal_clockwise",
      "flow_pattern": "diagonal_clockwise",
      "supports": ["AttentionPlan"],
      "reason": "A diagonal composition lets the group move across the frame on the open plaza while the harbour railing and skyline recede along the same diagonal, reinforcing forward energy and momentum consistent with 'The Mode Switch.'"
    },

    "CameraPlan": {
      "perspective_intent": "eye_level",
      "framing_intent": "medium_shot",
      "distance_intent": "near",
      "focal_length_mm": "35mm",
      "depth_of_field_category": "Atmospheric",
      "aperture_f_stop": "f/4",
      "supports": ["HierarchyPlan"],
      "source": "Hierarchy",
      "reason": "A 35mm eye-level medium shot keeps the viewer at peer height within the group (Subject Relationship Logic: belonging), wide enough to include the promenade and skyline context that Art Direction's Medium structural density calls for. f/4 (Atmospheric/Soft Focus, the default category) keeps the plaza and group sharp while softening the skyline so it supports rather than competes with the Primary hierarchy."
    },

    "LightingPlan": {
      "supports": ["HierarchyPlan"],
      "source": "Hierarchy",
      "intent": ["depth_perception", "emotional_interpretation", "subject_separation"],
      "possible_techniques": ["warm_practical_lighting"],
      "reason": "Warm promenade lamp light and ambient city glow establish a vibrant Hong Kong night atmosphere around the group, supporting the energized, social mood. No specific exposure ranking is assigned between the group and the skyline — relative brightness is left open for Synthesis/Prompt Compiler to resolve through general atmosphere rather than an explicit hierarchy."
    },

    "MaterialPlan": {
      "supports": ["HierarchyPlan"],
      "source": "Hierarchy",
      "intent": ["tactile_credibility", "emotional_interpretation"],
      "possible_techniques": ["surface_roughness_contrast", "specular_reflection_control"],
      "human_skin_rendering": "Visible natural skin texture across all subjects — pores, subtle tone variation, light post-workday flush on cheeks — with natural asymmetry in expressions and features; no airbrushing or beauty-filter smoothing.",
      "reason": "Contrasting the crisp/structured texture of office-mode garments (blazer weave, shirt collar) against the technical, slightly worn texture of activewear and the Pegasus mesh reinforces the 'mode switch' concept tactilely, while natural skin texture keeps the energized expressions credible rather than artificial."
    },

    "AtmosphericPlan": {
      "supports": ["VisualFlowPlan"],
      "source": "RealityModel",
      "intent": ["depth_perception", "environmental_mood"],
      "possible_techniques": ["aerial_perspective", "ambient_haze"],
      "reason": "A faint cross-harbour haze softens the skyline into the diagonal recession established by VisualFlowPlan, adding nighttime depth without obscuring the group or plaza."
    },

    "OpticalPlan": {
      "supports": ["AttentionPlan"],
      "source": "Attention",
      "intent": ["attention_guidance", "perceptual_credibility"],
      "possible_techniques": ["progressive_depth_falloff"],
      "bokeh_behavior": "Gradual, depth-dependent falloff consistent with 35mm at f/4: the group, the Pegasus, and the near promenade/railing remain sharp to clearly legible; the plaza surface softens slightly with distance; the cross-harbour skyline softens further into recognizable but gently blurred building forms and light glow — never a flat cutout blur.",
      "reason": "Moderate, progressive falloff keeps attention anchored on the group while letting the plaza and skyline remain contextually legible, matching the Atmospheric depth-of-field category."
    },

    "RenderingConstraints": {
      "reality_model_compliance": true,
      "preservation_compliance": true,
      "hierarchy_protection": true,
      "natural_skin_rendering_required": true,
      "pose_variation_required": true
    }
  }
}
```

---

## Validation

- ✓ Hierarchy readable: group (Primary) → Pegasus & plaza (Secondary) → skyline (Supporting); attention order preserved via sharpness/depth/gaze, not luminance.
- ✓ Depth of Field Category: **Atmospheric** (default), `f/4` falls within `f/4`–`f/5.6`; unchanged from base Trial_08.
- ✓ Depth of Field Realism: progressive falloff specified (group/Pegasus/railing sharp → plaza softens slightly → skyline softened but recognizable) — not uniform blur.
- ✓ `natural_skin_rendering_required: true` and `human_skin_rendering` populated — Human Subject Rendering Requirement satisfied.
- ✓ `pose_variation_required: true` — unchanged from base Trial_08.
- ✓ **Lighting/luminance hierarchy removed**: no `luminance_priority` per entity, no brightest/dimmest exposure ranking in `LightingPlan`, no luminance-based attention mechanism, no brightness comparison in `OpticalPlan.bokeh_behavior`.
- ✓ Reality Model (Realistic) respected throughout.
- ✓ Ready for Synthesis (re-run).

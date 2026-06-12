# Composition & Rendering Contract — Nike Chill Run Club (Stage 6.1, re-run)

Framework: `6.1 Composition_Rendering.md` (current — Luminance Hierarchy + Depth of Field Category Selection)
Inputs: SceneContract (Stage 5.2.5) — identical to Trial_07 (Stages 00–05 unchanged)
Decision Type: Visual Expression. Priority order: Narrative Clarity > Hierarchy Stability > Attention Guidance > Emotional Reinforcement > Visual Beauty. Human subjects present → natural-skin rendering requirement in force; multiple subjects sharing an action (group jog) → Multi-Subject Pose Variation Requirement in force.

This is a re-run of Trial_07's Stage 6.1 against the updated framework. `HierarchyPlan.hierarchy_level`/`reason`/`source`, `AttentionPlan`, `VisualFlowPlan`, `LightingPlan`, `MaterialPlan`, and `AtmosphericPlan` are unchanged from Trial_07 — only `luminance_priority` (new), `CameraPlan.depth_of_field_category`/`aperture_f_stop` (re-derived), `OpticalPlan.bokeh_behavior` (re-derived), and `RenderingConstraints.pose_variation_required` (now explicit per the current framework) differ.

```json
{
  "CompositionRenderingContract": {

    "HierarchyPlan": [
      {
        "element": "entity_01",
        "hierarchy_level": "Primary",
        "luminance_priority": "Brightest",
        "reason": "The shared human moment carries the Mental Reset + belonging communication; it must read first and brightest.",
        "source": "Narrative"
      },
      {
        "element": "entity_02",
        "hierarchy_level": "Secondary",
        "luminance_priority": "Mid",
        "reason": "Nike Pegasus must remain legible and correctly preserved (Near Exact), but must not out-compete the human signal — product is proof, not hero. Visible and lit, but not the brightest element.",
        "source": "Preservation"
      },
      {
        "element": "entity_03",
        "hierarchy_level": "Secondary",
        "luminance_priority": "Mid",
        "reason": "Promenade grounds the scene as a real HK evening and supports the 'integrated into city life' meaning; lit enough to read, subordinate to the group.",
        "source": "Environmental"
      },
      {
        "element": "entity_04",
        "hierarchy_level": "Supporting",
        "luminance_priority": "Dimmest",
        "reason": "Skyline provides place identity and depth but stays a distant backdrop. The illuminated skyline is a naturally bright source and must be exposed down so its window-lights never outshine the group.",
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
      "depth_of_field_category": "Atmospheric",
      "aperture_f_stop": "f/5",
      "supports": ["HierarchyPlan"],
      "source": "Hierarchy",
      "reason": "Eye-level places the viewer among the group as a peer (Subject Relationship Logic = belonging). A near full shot from the knees up keeps faces readable while letting at least one subject's shoes enter the lower frame. 35mm holds group + promenade context. Depth of Field Category Selection: entity_03 (promenade) and entity_04 (skyline) are Secondary/Supporting Environmental elements that contribute place identity ('integrated into city life', 'reads as Hong Kong'), but neither needs to be rendered crisp/detailed for that meaning to land — the skyline communicates through warm light shapes, not architectural detail. AttentionPlan does not call for isolating a single element (it sequences across the whole group plus shoes plus setting). This rules out both Environmental Context (no need for sharp background detail) and Commercial Isolation (no isolation mandate), landing on the default Atmospheric/Soft Focus category. f/5 (35mm) keeps the group and the Pegasus sharp, lets the railing and near water stay clearly legible, and softens the skyline into recognizable but gentle light shapes — slightly less aggressive than Trial_07's f/2.8, which over-isolated the group relative to the 'integrated into city life' communication."
    },

    "LightingPlan": {
      "supports": ["HierarchyPlan"],
      "source": "Emotion",
      "intent": ["depth_perception", "emotional_interpretation", "subject_separation"],
      "possible_techniques": ["warm_directional_key_from_streetlamps", "ambient_skyline_fill"],
      "reason": "Warm directional streetlamp light keys the group and lifts them above a softer, cooler background, carrying the 'warm relief / exhale' tone while keeping the subjects clearly separated from the city behind. The skyline's window-lights are exposed down relative to the group so they read as ambient city glow rather than competing bright points, honoring entity_04's Dimmest luminance_priority."
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
      "bokeh_behavior": "Atmospheric/Soft Focus falloff for 35mm at f/5: the group and the visible Pegasus stay sharp, the railing and near water remain clearly legible, and mid-distance towers soften gradually. The far skyline reads as soft, recognizable building shapes and warm light glow rather than dissolving into heavy circular bokeh — its brightness is diffused, not blown-out, consistent with its Dimmest luminance_priority. Progressive falloff, no flat uniform blur.",
      "reason": "Depth-dependent softening keeps the group as the focal point and the HK setting clearly recognizable — 'integrated into city life' depends on the skyline reading as Hong Kong, not as an abstract glow."
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

## Reasoning Notes

- **Luminance Hierarchy (new):** entity_01 = Brightest (Primary), entity_02/03 = Mid (Secondary, visible and lit but subordinate), entity_04 = Dimmest (Supporting; the illuminated skyline's window-lights are exposed down so they never outshine the group).
- **Depth of Field Category Selection (new):** Atmospheric/Soft Focus (f/4–f/5.6), selected as f/5. The promenade and skyline contribute place identity ("Hong Kong at night") but don't require sharp architectural detail to do so, and AttentionPlan sequences across the whole scene rather than isolating one element — neither Environmental Context nor Commercial Isolation criteria apply, so the default Atmospheric category governs. This replaces Trial_07's f/2.8 with a slightly deeper field that keeps the railing/water legible alongside the group while the skyline stays soft but recognizable.
- **`pose_variation_required: true`** (now explicit) — group of 4–5 subjects share a jogging action; the Multi-Subject Pose Variation Requirement applies. This was already informally honored in Trial_07's `08a_VisualPrompt.md` ("each runner caught at a different point in their stride") via `ImperfectionRendering`, but the current framework surfaces it as a formal `RenderingConstraints` flag and Perceptual Validation assertion.
- **DOF realism:** bokeh tied to 35mm / f/5 with a named falloff curve consistent with the Atmospheric category; group, Pegasus, and near-promenade all stay legible while the skyline remains soft but identifiable.
- **Hierarchy protects preservation, not the reverse:** the Pegasus stays Secondary so its Near-Exact preservation never escalates into a product-hero composition — consistent with Strategy's `forbidden_positioning: ProductHero`.
- **Boundary:** no messaging, narrative, or scene-construction changes — SceneContract treated as source truth; HierarchyPlan levels/sources, AttentionPlan, VisualFlowPlan, LightingPlan content, MaterialPlan, and AtmosphericPlan unchanged from Trial_07.

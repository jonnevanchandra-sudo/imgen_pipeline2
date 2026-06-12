# Composition & Rendering Contract — Natural Protein Powder (Stage 6.1, re-run)

Framework: `6.1 Composition_Rendering.md` (current — Luminance Hierarchy + Depth of Field Category Selection)
Inputs: SceneContract (Stage 5.2.5) — identical to Trial_01 (Stages 00–05 unchanged)
Decision Type: Visual Expression. Priority order: Narrative Clarity > Hierarchy Stability > Attention Guidance > Emotional Reinforcement > Visual Beauty. One human subject present → natural-skin requirement in force; single subject → pose variation requirement not triggered.

This is a re-run of Trial_01's Stage 6.1 against the updated framework. `HierarchyPlan`, `AttentionPlan`, `VisualFlowPlan`, `LightingPlan`, `MaterialPlan`, and `AtmosphericPlan` are unchanged from Trial_01 — only `luminance_priority` (new), `CameraPlan.depth_of_field_category`/`aperture_f_stop` (re-derived), and `OpticalPlan.bokeh_behavior` (re-derived) differ.

```json
{
  "CompositionRenderingContract": {

    "HierarchyPlan": [
      {
        "element": "entity_01",
        "hierarchy_level": "Primary",
        "luminance_priority": "Brightest",
        "reason": "The unguarded savoring moment is the entire communication (Narrative: skepticism → genuine enjoyment); it must read first and brightest.",
        "source": "Narrative"
      },
      {
        "element": "entity_02",
        "hierarchy_level": "Secondary",
        "luminance_priority": "Mid",
        "reason": "The drink is the object of the pleasure and the appetite carrier — second read, tightly coupled to the face, well-lit but not outranking it.",
        "source": "Narrative"
      },
      {
        "element": "entity_04",
        "hierarchy_level": "Secondary",
        "luminance_priority": "Mid",
        "reason": "Ingredients are the visible proof of 'natural' — they must be identifiable and adequately lit without competing with the human moment.",
        "source": "Preservation"
      },
      {
        "element": "entity_03",
        "hierarchy_level": "Secondary",
        "luminance_priority": "Mid",
        "reason": "The pack anchors the ad to the product but is held to kitchen-object status (Strategy: no SupplementHero) — visible, not a lit hero object.",
        "source": "Preservation"
      },
      {
        "element": "entity_05",
        "hierarchy_level": "Supporting",
        "luminance_priority": "Dimmest",
        "reason": "Kitchen establishes 'ordinary life, not a regime' but stays atmospheric. The window is a naturally bright source and must be exposed down so it never outshines entity_01.",
        "source": "Environmental"
      }
    ],

    "AttentionPlan": {
      "entry_element": "entity_01",
      "attention_progression": ["entity_01", "entity_02", "entity_04", "entity_03", "entity_05"],
      "exit_element": "entity_05",
      "mechanisms": ["sharpness_hierarchy", "luminance_contrast", "directional_lines"],
      "reason": "Attention lands on the lit face mid-savor, drops to the glass at her lips, then follows the counter line to the ingredients and open pack, releasing into the soft kitchen. Three mechanisms suffice; the counter edge does the guiding."
    },

    "VisualFlowPlan": {
      "flow_direction": "top_to_bottom",
      "flow_pattern": "linear_vector",
      "supports": ["AttentionPlan"],
      "reason": "Face → glass → counter evidence is a natural downward read that mirrors the act of drinking and ends on the proof, reinforcing pleasure-first, ingredients-second."
    },

    "CameraPlan": {
      "perspective_intent": "eye_level",
      "framing_intent": "medium_shot",
      "distance_intent": "near",
      "focal_length_mm": "50mm",
      "depth_of_field_category": "Atmospheric",
      "aperture_f_stop": "f/5",
      "supports": ["HierarchyPlan"],
      "source": "Hierarchy",
      "reason": "Eye-level and near places the viewer at the counter inside the intimate moment (Subject Relationship Logic: Intimacy). A medium shot from the waist up keeps the savoring expression dominant while the counter foreground holds glass, ingredients, and pack. Depth of Field Category Selection: entity_05 (kitchen) is Supporting/Environmental and explicitly held 'atmospheric' — it carries no independent communication weight, and AttentionPlan's mechanisms guide attention through sharpness/contrast across multiple Secondary elements rather than isolating one. Neither the Environmental Context nor Commercial Isolation criteria are met, so this falls to the default Atmospheric/Soft Focus category. f/5 (50mm) keeps face, glass, and counter evidence (entity_02/03/04) sharp and legible while the kitchen and window soften without dissolving into heavy bokeh — correcting Trial_01's f/2.2, which over-isolated the subject relative to the upstream hierarchy and attention signals."
    },

    "LightingPlan": {
      "supports": ["HierarchyPlan"],
      "source": "Emotion",
      "intent": ["depth_perception", "emotional_interpretation", "subject_separation"],
      "possible_techniques": ["soft_window_key", "natural_bounce_fill"],
      "reason": "Soft directional morning window light keys the face and the glass, with gentle natural falloff into the kitchen — warmth and ordinariness without theatrical shaping. The window itself is exposed down relative to the face and glass so it reads as a soft light source, not a bright competing shape, honoring entity_05's Dimmest luminance_priority. Appetite appeal depends on daylight credibility."
    },

    "MaterialPlan": {
      "supports": ["HierarchyPlan"],
      "source": "Emotion",
      "intent": ["tactile_credibility", "emotional_interpretation"],
      "possible_techniques": ["surface_roughness_contrast", "specular_reflection_control"],
      "human_skin_rendering": "Visible pores and natural tone variation; a relaxed, slightly asymmetric expression mid-savor. No airbrushing, no beauty-filter smoothing.",
      "reason": "Tactile truth carries both messages: condensation and thick texture on the glass say 'tastes good'; matte kraft paper, dusty scoop, oat and berry surfaces say 'real food'. Skin must stay real for the unguarded moment to be believed."
    },

    "AtmosphericPlan": {
      "supports": ["VisualFlowPlan"],
      "source": "Emotion",
      "intent": ["depth_perception", "environmental_mood"],
      "possible_techniques": ["soft_daylight_airiness"],
      "reason": "A light, airy morning atmosphere keeps the scene fresh and ordinary; no haze or drama — atmosphere must not compete with the appetite read."
    },

    "OpticalPlan": {
      "supports": ["AttentionPlan"],
      "source": "Attention",
      "intent": ["attention_guidance", "perceptual_credibility"],
      "possible_techniques": ["bokeh_blur_isolation"],
      "bokeh_behavior": "Atmospheric/Soft Focus falloff for 50mm at f/5: face, glass, and counter evidence (ingredients, pack, scoop) remain sharp to semi-legible across the foreground/midground. The kitchen and window soften progressively with distance but remain recognizable as large shapes — counter line, window frame, cabinetry — rather than dissolving into abstract bokeh. The window's brightness is rendered soft-edged and diffused, not a sharp blown-out highlight, consistent with its Dimmest luminance_priority.",
      "reason": "Depth guides the eye down the attention path while keeping the ingredient evidence readable and the kitchen contextually present — if the ingredients blur to abstraction, the 'natural' message dies, and if the kitchen vanishes entirely, 'ordinary daily life' loses its setting."
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

---

## Reasoning Notes

- **Luminance Hierarchy (new):** entity_01 = Brightest (Primary), entity_02/03/04 = Mid (Secondary, well-lit but subordinate), entity_05 = Dimmest (Supporting, and the window — a naturally bright source — is exposed down so it never outshines the subject).
- **Depth of Field Category Selection (new):** Atmospheric/Soft Focus (f/4–f/5.6), selected as f/5. entity_05 (kitchen/window) is Supporting/Environmental with no independent communication weight ("stays atmospheric" per HierarchyPlan), and AttentionPlan does not call for single-element isolation — neither Environmental Context nor Commercial Isolation criteria apply, so the default Atmospheric category governs. This replaces Trial_01's f/2.2.
- **`pose_variation_required: false`** — single human subject; the Multi-Subject Pose Variation Requirement does not trigger.
- **DOF realism:** bokeh tied to 50mm / f/5 with a named falloff curve consistent with the Atmospheric category; ingredient legibility and kitchen context are both protected.
- **Hierarchy protects strategy:** the pack is held at Secondary with kitchen-object treatment, enforcing Strategy's forbidden `SupplementHero` positioning.
- **Boundary:** no messaging, narrative, or scene-construction changes — SceneContract treated as source truth; HierarchyPlan/AttentionPlan/VisualFlowPlan/LightingPlan/MaterialPlan/AtmosphericPlan content unchanged from Trial_01.

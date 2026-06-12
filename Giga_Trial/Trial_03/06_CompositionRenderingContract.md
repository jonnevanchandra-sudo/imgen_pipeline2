# Composition & Rendering Contract
**Brand:** GigaSports
**Campaign:** Gigasports Pickle Club Community
**Framework:** Composition & Rendering Framework
**Stage:** 6 — Visual Expression

---

## Inputs Consumed

- **Reality Model:** Realistic
- **Scene Entities:** entity_01 (subject group), entity_02 (paddles), entity_03 (court/net), entity_04 (venue), entity_05 (GigaSports logo — reference-locked to asset_01)
- **Depth Structure:** Foreground: subjects + paddles / Midground: court + net / Background: venue + brand
- **Preservation Contracts:** entity_01 Critical, entity_05 High (brand legibility in background — reproduced from reference)
- **Focal Priority (from Art Direction):** Human faces and social interaction first

---

## Global Priority Order

Narrative Clarity > Hierarchy Stability > Attention Guidance > Emotional Reinforcement > Visual Beauty

---

```json
{
  "CompositionRenderingContract": {

    "HierarchyPlan": [
      {
        "element": "entity_01",
        "hierarchy_level": "Primary",
        "reason": "Subject group is the emotional carrier — social connection moment is the primary communication. Human faces and body language must dominate visual weight.",
        "source": "Narrative"
      },
      {
        "element": "entity_02",
        "hierarchy_level": "Secondary",
        "reason": "Paddles establish sport identity and pickleball context — subordinate to the human social moment.",
        "source": "Narrative"
      },
      {
        "element": "entity_03",
        "hierarchy_level": "Secondary",
        "reason": "Court and net ground the scene physically and communicate active venue context.",
        "source": "Environmental"
      },
      {
        "element": "entity_05",
        "hierarchy_level": "Supporting",
        "reason": "GigaSports logo must be legible but must not interrupt the primary social narrative. Background placement preserves brand presence. Reproduced from reference_asset_01 — accuracy depends on reference image being attached, not on prompt description alone.",
        "source": "Preservation"
      },
      {
        "element": "entity_04",
        "hierarchy_level": "Supporting",
        "reason": "Venue provides depth, warmth, and authenticity. Atmospheric role only.",
        "source": "Environmental"
      }
    ],

    "AttentionPlan": {
      "entry_element": "entity_01 — faces and social interaction of subject group",
      "attention_progression": [
        "entity_01 (faces and expressed emotion — laughter, gesture, eye contact)",
        "entity_02 (paddles in hand — sport context established)",
        "entity_03 (court surface and net — venue confirmed)",
        "entity_05 (GigaSports logo — brand recognized)",
        "entity_04 (venue environment — scene settled)"
      ],
      "exit_element": "entity_04 — venue background depth",
      "mechanisms": [
        "luminance_contrast",
        "sharpness_hierarchy",
        "gaze_vectors",
        "depth_separation"
      ],
      "reason": "Subject group receives maximum luminance and sharpness. Background depth separation ensures venue and brand element recede naturally. Gaze vectors between subjects pull the viewer into the social dynamic."
    },

    "VisualFlowPlan": {
      "flow_direction": "radiating_outward",
      "flow_pattern": "radiating from subject group center outward toward environment",
      "supports": ["AttentionPlan"],
      "reason": "Radiating flow from the subject group communicates that everything exists in relationship to the social moment — court, venue, and brand are context for the people."
    },

    "CameraPlan": {
      "perspective_intent": "eye_level",
      "framing_intent": "medium_shot",
      "distance_intent": "near",
      "supports": ["HierarchyPlan"],
      "source": "Emotion",
      "reason": "Eye-level perspective is critical to Equality and Partnership subject relationship logic. Medium shot allows faces to be readable while including body language and environmental context. Near distance maintains intimacy."
    },

    "LightingPlan": {
      "supports": ["HierarchyPlan"],
      "source": "Hierarchy",
      "intent": [
        "subject_separation",
        "emotional_interpretation",
        "depth_perception"
      ],
      "possible_techniques": [
        "soft_ambient_fill_with_directional_key",
        "natural_venue_overhead_lighting_with_subtle_fill"
      ],
      "reason": "Soft warm ambient keeps subject luminance above background without breaking indoor venue atmosphere. Lighting should feel like it belongs to the venue — not studio contrast. Background must remain warm enough to keep the logo banner legible through bokeh."
    },

    "MaterialPlan": {
      "supports": ["HierarchyPlan"],
      "source": "Emotion",
      "intent": [
        "tactile_credibility",
        "emotional_interpretation"
      ],
      "possible_techniques": [
        "subtle_fabric_texture_on_athletic_wear",
        "matte_paddle_surface_contrast_against_skin",
        "slight_court_surface_texture_for_environmental_grounding"
      ],
      "reason": "Material variation increases perceptual credibility. Prevents image from reading as digitally generated. Material detail is subordinate to human expression."
    },

    "AtmosphericPlan": {
      "supports": ["VisualFlowPlan"],
      "source": "Emotion",
      "intent": [
        "environmental_mood",
        "depth_perception"
      ],
      "possible_techniques": [
        "mild_aerial_perspective_in_venue_background",
        "warm_ambient_glow_from_overhead_venue_lighting"
      ],
      "reason": "Mild atmospheric haze in background increases depth and draws background away from competition with subjects. Warmth reinforces Social Encouragement emotional register. Atmosphere must remain subtle enough not to obscure the brand logo in background — logo must stay identifiable through bokeh."
    },

    "OpticalPlan": {
      "supports": ["AttentionPlan"],
      "source": "Attention",
      "intent": [
        "attention_guidance",
        "perceptual_credibility"
      ],
      "possible_techniques": [
        "shallow_depth_of_field_with_subject_group_in_sharp_focus",
        "natural_bokeh_on_background_venue_and_brand_element"
      ],
      "reason": "Shallow depth of field places subjects in sharp focus while venue and logo fall into readable bokeh. Bokeh depth calibrated to keep entity_05 (GigaSports logo) identifiable even when soft. Reference image attached as reference_asset_01 ensures the logo is accurate regardless of bokeh treatment."
    },

    "RenderingConstraints": {
      "reality_model_compliance": true,
      "preservation_compliance": true,
      "hierarchy_protection": true,
      "brand_asset_note": "entity_05 is reference-locked — reproduction accuracy depends on reference_asset_01 being attached to the API call, not on text description alone"
    }
  }
}
```

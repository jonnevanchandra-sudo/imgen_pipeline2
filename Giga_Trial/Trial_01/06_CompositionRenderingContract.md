# Composition & Rendering Contract
**Brand:** GigaSports
**Campaign:** Gigasports Pickle Club Community
**Framework:** Composition & Rendering Framework
**Stage:** 6 — Visual Expression

---

## Inputs Consumed

- **Reality Model:** Realistic
- **Scene Entities:** entity_01 (subject group), entity_02 (paddles), entity_03 (court/net), entity_04 (venue), entity_05 (GigaSports brand)
- **Depth Structure:** Foreground: subjects + paddles / Midground: court + net / Background: venue + brand
- **Preservation Contracts:** entity_01 Critical, entity_05 High (brand legibility in background)
- **Focal Priority (from Art Direction):** Human faces and social interaction first — must claim cognitive entry before sport context or environment

---

## Global Priority Order

Narrative Clarity > Hierarchy Stability > Attention Guidance > Emotional Reinforcement > Visual Beauty

All composition and rendering decisions derive from this order. Visual beauty is the last consideration.

---

```json
{
  "CompositionRenderingContract": {

    "HierarchyPlan": [
      {
        "element": "entity_01",
        "hierarchy_level": "Primary",
        "reason": "Subject group is the emotional carrier of the campaign — the social connection moment is the primary communication. Human faces and body language must dominate visual weight.",
        "source": "Narrative"
      },
      {
        "element": "entity_02",
        "hierarchy_level": "Secondary",
        "reason": "Paddles establish sport identity and pickleball context — necessary for campaign recognition but subordinate to the human social moment.",
        "source": "Narrative"
      },
      {
        "element": "entity_03",
        "hierarchy_level": "Secondary",
        "reason": "Court and net ground the scene physically and communicate the active venue context. Supports scene readability without competing with subjects.",
        "source": "Environmental"
      },
      {
        "element": "entity_05",
        "hierarchy_level": "Supporting",
        "reason": "GigaSports brand element must be legible but must not interrupt the primary social narrative. Background placement preserves brand presence without contaminating emotional register.",
        "source": "Preservation"
      },
      {
        "element": "entity_04",
        "hierarchy_level": "Supporting",
        "reason": "Venue environment provides depth, warmth, and authenticity. Atmospheric role only — must not attract attention away from subject group.",
        "source": "Environmental"
      }
    ],

    "AttentionPlan": {
      "entry_element": "entity_01 — faces and social interaction of subject group",
      "attention_progression": [
        "entity_01 (faces and expressed emotion — laughter, gesture, eye contact)",
        "entity_02 (paddles in hand — sport context established)",
        "entity_03 (court surface and net — venue confirmed)",
        "entity_05 (GigaSports brand element — brand recognized)",
        "entity_04 (venue environment — scene settled)"
      ],
      "exit_element": "entity_04 — venue background depth",
      "mechanisms": [
        "luminance_contrast",
        "sharpness_hierarchy",
        "gaze_vectors",
        "depth_separation"
      ],
      "reason": "Subject group must receive maximum luminance and sharpness. Background depth separation ensures venue and brand element recede naturally without active effort. Gaze vectors between subjects pull the viewer into the social dynamic and prevent attention from escaping to background elements prematurely."
    },

    "VisualFlowPlan": {
      "flow_direction": "radiating_outward",
      "flow_pattern": "radiating from subject group center outward toward environment",
      "supports": ["AttentionPlan"],
      "reason": "Radiating flow from the subject group center communicates that everything in the image exists in relationship to the social moment — court, venue, and brand are context for the people, not the other way around. This reinforces the Belonging perceptual meaning."
    },

    "CameraPlan": {
      "perspective_intent": "eye_level",
      "framing_intent": "medium_shot",
      "distance_intent": "near",
      "supports": ["HierarchyPlan"],
      "source": "Emotion",
      "reason": "Eye-level perspective is critical to the Equality and Partnership subject relationship logic from Art Direction — the viewer should feel like a peer, not looking up at aspirational subjects or down from a position of detachment. Medium shot allows faces to be clearly readable while including enough body language and environmental context to establish the social and sport setting. Near distance maintains intimacy without isolation."
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
      "reason": "Lighting must keep subject group luminance above background to maintain hierarchy without breaking the realistic indoor venue atmosphere. Soft, warm ambient light reads as a social and welcoming environment — not a competitive stadium or dramatic editorial. Slight subject luminance advantage over background achieved through directional fill rather than artificial studio contrast. Lighting should feel like it belongs to the venue."
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
      "reason": "Material variation increases perceptual credibility and emotional believability. Athletic wear fabric texture, paddle surface, and court material should feel physically real — this supports the realistic reality model and prevents the image from reading as digitally generated. Material detail is subordinate to human expression and should not compete for attention."
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
      "reason": "A mild atmospheric haze in the venue background increases perceived depth and naturally draws the background away from competition with the primary subject group. Warm venue lighting glow reinforces the Social Encouragement emotional register — the environment should feel inviting and energized, not cold or institutional. Atmosphere must remain subtle enough not to obscure the GigaSports brand element in the background."
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
      "reason": "Shallow depth of field places the subject group in sharp focus while the venue and brand element fall into natural but readable bokeh. This is the most efficient attention mechanism for a lifestyle photograph — it is visually natural (does not feel manipulated), it is perceptually credible within the realistic reality model, and it maintains brand element legibility despite background placement. Bokeh depth must be calibrated to keep entity_05 (GigaSports brand) identifiable even when soft."
    },

    "RenderingConstraints": {
      "reality_model_compliance": true,
      "preservation_compliance": true,
      "hierarchy_protection": true
    }
  }
}
```

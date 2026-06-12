# Composition & Rendering Contract
**Brand:** GigaSports
**Campaign:** Gigasports Pickle Club Community
**Framework:** Composition & Rendering Framework
**Stage:** 6 — Visual Expression

---

```json
{
  "CompositionRenderingContract": {

    "HierarchyPlan": [
      {
        "element": "entity_01 — newcomer face and expression",
        "hierarchy_level": "Primary",
        "reason": "The newcomer's expression — the micro-moment of belonging arriving — is the emotional argument of the entire image. If the viewer cannot read the shift from uncertainty to warmth on entity_01's face, the conversion message fails.",
        "source": "Narrative"
      },
      {
        "element": "entity_02 — established member welcome gesture and expression",
        "hierarchy_level": "Primary",
        "reason": "The welcome gesture from entity_02 is the other half of the emotional transaction. Both faces and the direction of the gesture must read simultaneously for the viewer to understand the relational dynamic.",
        "source": "Narrative"
      },
      {
        "element": "entity_03 — pickleball paddles",
        "hierarchy_level": "Secondary",
        "reason": "Sport identity signal — grounds the scene as pickleball, not generic social interaction. Must be identifiable but should not compete with the human emotional moment.",
        "source": "Preservation"
      },
      {
        "element": "entity_04 — indoor court and net",
        "hierarchy_level": "Supporting",
        "reason": "Environmental grounding — confirms the venue is an active pickleball court. Present for context, not for focal attention.",
        "source": "Environmental"
      },
      {
        "element": "entity_05 — GigaSports logo",
        "hierarchy_level": "Supporting",
        "reason": "Brand attribution — must be legible through background bokeh but must not compete with the human welcome moment. Brand appears as the host, not the hero.",
        "source": "Preservation"
      }
    ],

    "AttentionPlan": {
      "entry_element": "entity_01 — newcomer face",
      "attention_progression": [
        "entity_01 — newcomer expression (entry: the emotional register of welcome being received)",
        "entity_02 — established member(s) and welcome gesture (confirmation: who is extending the welcome and how)",
        "entity_03 — paddles (sport context confirmed)",
        "entity_04 — court and net (venue grounded)",
        "entity_05 — GigaSports logo (brand recognized)"
      ],
      "exit_element": "entity_05 — GigaSports brand in background",
      "mechanisms": [
        "sharpness_hierarchy",
        "luminance_contrast",
        "gaze_vectors",
        "depth_separation"
      ],
      "reason": "Sharpness hierarchy places entity_01 and entity_02 in crisp foreground focus while background recedes. Gaze vectors from entity_02 directed at entity_01 create a natural pull toward entity_01's expression as the emotional anchor. Depth separation ensures the background brand element is readable without competing for primary attention."
    },

    "VisualFlowPlan": {
      "flow_direction": "diagonal_clockwise",
      "flow_pattern": "z_pattern",
      "supports": ["AttentionPlan"],
      "reason": "Z-pattern suits Instagram feed scanning behavior. Entry at entity_01 (top-left or top-center of the subjects), cross to entity_02 welcome gesture, down to paddles confirming sport context, exit to background brand element in lower region. The diagonal also mirrors the orientation of two figures facing each other — reinforcing the relational dynamic compositionally."
    },

    "CameraPlan": {
      "perspective_intent": "eye_level",
      "framing_intent": "medium_shot",
      "distance_intent": "near",
      "supports": ["HierarchyPlan"],
      "source": "Emotion",
      "reason": "Eye-level camera communicates equality — the viewer is not observing from above (which would feel voyeuristic or dominant) but from within the group's social space. Medium shot at near distance ensures both entity_01 and entity_02 faces are readable at scroll speed — the welcome moment requires facial legibility to land. Near distance collapses the psychological gap between viewer and subjects, placing the viewer in the social moment rather than outside it."
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
        "soft_overhead_ambient_fill",
        "subtle_warm_key_on_subjects",
        "natural_indoor_venue_light_variation"
      ],
      "reason": "Soft overhead ambient fill with a subtle warm key on the foreground subjects separates entity_01 and entity_02 from the venue background without introducing studio artificiality. Subjects read slightly brighter and warmer than the background — reinforcing hierarchy through luminance while maintaining the authentic indoor sports venue quality. No hard shadows; no dramatic rim lighting; no cinematic contrast that would shift the register from lifestyle to editorial performance."
    },

    "MaterialPlan": {
      "supports": ["HierarchyPlan"],
      "source": "Emotion",
      "intent": [
        "tactile_credibility",
        "emotional_interpretation"
      ],
      "possible_techniques": [
        "fabric_drape_and_wrinkle_on_athletic_wear",
        "natural_skin_texture_variation",
        "matte_surface_behavior_on_paddles"
      ],
      "reason": "Natural fabric behavior on athletic casual clothing increases perceptual credibility — wrinkle and drape signal real movement, not rendered perfection. Natural skin texture (pores, subtle tone variation) on both subjects is essential to the human authenticity required for the welcome moment to feel real. Paddle surface: matte with slight sheen variation, not hyper-polished."
    },

    "AtmosphericPlan": {
      "supports": ["VisualFlowPlan"],
      "source": "Emotion",
      "intent": [
        "depth_perception",
        "environmental_mood"
      ],
      "possible_techniques": [
        "warm_indoor_venue_ambient_haze",
        "natural_background_warm_bokeh"
      ],
      "reason": "Indoor sports venue atmosphere — warm, active, communal. The background recedes into warm bokeh that softens the court and brand element without losing environmental legibility. Atmosphere must communicate 'active social venue,' not 'institutional gymnasium' or 'studio set.' The warmth of the background light reinforces the social warmth of the human moment in the foreground."
    },

    "OpticalPlan": {
      "supports": ["AttentionPlan"],
      "source": "Attention",
      "intent": [
        "attention_guidance",
        "perceptual_credibility"
      ],
      "possible_techniques": [
        "shallow_depth_of_field",
        "natural_bokeh_on_background",
        "bokeh_calibrated_for_logo_legibility"
      ],
      "reason": "Shallow depth of field isolates entity_01 and entity_02 in sharp foreground focus while court and brand element recede into natural warm bokeh. Bokeh on the GigaSports logo must be calibrated so the logo remains identifiable — soft but readable — not so blurred that it becomes a color smear. This is the same optical constraint as Trial 3: brand recognition must survive at background bokeh depth."
    },

    "RenderingConstraints": {
      "reality_model_compliance": true,
      "preservation_compliance": true,
      "hierarchy_protection": true
    }
  }
}
```

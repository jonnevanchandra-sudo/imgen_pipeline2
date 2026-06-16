# Composition & Rendering Contract — Natural Protein Powder (Stage 6.1, Trial_03)

Framework: `6.1 Composition_Rendering.md`
Inputs: SceneContract (Stage 5.2.5, Trial_03) + New Creative Direction (Style / Angle / Distance brief, see Stage 5)
Decision Type: Visual Expression. Priority order: Narrative Clarity > Hierarchy Stability > Attention Guidance > Emotional Reinforcement > Visual Beauty. One human subject present → natural-skin requirement in force; single subject → pose variation requirement not triggered.

```json
{
  "CompositionRenderingContract": {

    "HierarchyPlan": [
      {
        "element": "entity_01",
        "hierarchy_level": "Primary",
        "luminance_priority": "Brightest",
        "reason": "The unguarded savoring moment is the entire communication (Narrative: skepticism → genuine enjoyment); in a frontal waist-up portrait she occupies most of the frame and must read first and brightest.",
        "source": "Narrative"
      },
      {
        "element": "entity_02",
        "hierarchy_level": "Secondary",
        "luminance_priority": "Mid",
        "reason": "The drink is the object of the pleasure and the appetite carrier — held close to her body, well-lit and clearly legible, but subordinate to her face/expression.",
        "source": "Narrative"
      },
      {
        "element": "entity_03",
        "hierarchy_level": "Secondary",
        "luminance_priority": "Mid",
        "reason": "The pack anchors the ad to the product ('clear product focus' in the new brief) but is held to kitchen-object status (Strategy: no SupplementHero) — clearly visible and crisp, not a separately lit hero object.",
        "source": "Preservation"
      },
      {
        "element": "entity_04",
        "hierarchy_level": "Secondary",
        "luminance_priority": "Mid",
        "reason": "Ingredients are the visible proof of 'natural' — identifiable and evenly lit alongside the pack and glass.",
        "source": "Preservation"
      },
      {
        "element": "entity_05",
        "hierarchy_level": "Supporting",
        "luminance_priority": "Dimmest",
        "reason": "The kitchen establishes 'ordinary home life, not a regime' but stays a soft backdrop. Even under bright, even lighting, it must still be exposed at or below entity_01's level so the window/background never outshines the subject.",
        "source": "Environmental"
      }
    ],

    "AttentionPlan": {
      "entry_element": "entity_01",
      "attention_progression": ["entity_01", "entity_02", "entity_03", "entity_04", "entity_05"],
      "exit_element": "entity_05",
      "mechanisms": ["sharpness_hierarchy", "luminance_contrast", "gaze_vectors"],
      "reason": "Attention lands first on the lit, sharp face mid-savor (frontal portrait), then follows her downward gaze and the glass at her lips, across to the pack and ingredients sharing her counter space, and finally releases into the softened kitchen backdrop. Her own gaze vector — directed at the glass, not the lens — does double duty: it guides the viewer's eye and preserves the 'unguarded, not performed to camera' read despite the frontal camera position."
    },

    "VisualFlowPlan": {
      "flow_direction": "top_to_bottom",
      "flow_pattern": "linear_vector",
      "supports": ["AttentionPlan"],
      "reason": "Face → glass/gaze → counter evidence at waist level is a natural downward read in a waist-up frontal portrait, mirroring the act of drinking and ending on the proof — pleasure-first, ingredients-second is preserved even in the new frontal framing."
    },

    "CameraPlan": {
      "perspective_intent": "eye_level",
      "framing_intent": "medium_shot",
      "distance_intent": "mid",
      "focal_length_mm": "85mm",
      "depth_of_field_category": "Atmospheric",
      "aperture_f_stop": "f/4",
      "supports": ["HierarchyPlan"],
      "source": "Hierarchy",
      "reason": "Per the new brief: eye-level, straight-on/direct-forward, undistorted, waist-up half-body framing at a balanced (mid) distance. An 85mm lens at this distance gives a flattering, undistorted portrait perspective typical of high-end fashion-campaign photography, with natural proportions for both the subject and the counter items sharing her frame. The camera is positioned squarely in front of her (frontal/straight-on) — but per the SceneContract, her own gaze stays on the glass, so the frontal camera angle reads as a composed lifestyle-campaign portrait rather than a to-camera performance. Depth of Field Category Selection: entity_02/03/04 are Secondary elements that carry independent communication weight (drink, product, ingredients — all MustSurvive/PreserveWhenPossible), so Commercial Isolation (which requires Secondary/Supporting elements to carry no independent role) does not apply; entity_05 is Supporting/Environmental and the AttentionPlan does not require full background legibility, ruling out Environmental Context. Atmospheric/Soft Focus is the correct default — f/4 (the sharper end of the Atmospheric range) is chosen to honor 'clear product focus' from the new brief while keeping the kitchen backdrop recognizable as a bright, clean space rather than fully dissolving it."
    },

    "LightingPlan": {
      "supports": ["HierarchyPlan"],
      "source": "Emotion",
      "intent": ["depth_perception", "emotional_interpretation", "subject_separation"],
      "possible_techniques": ["bright_even_key_lighting", "soft_fill_to_reduce_shadow", "clean_commercial_lighting"],
      "reason": "Per the new brief's 'bright even lighting' and 'high-end fashion campaign' style: a bright, soft, broadly even key with gentle fill minimizes harsh shadow across the subject and counter, giving a crisp, polished, aspirational-lifestyle look. Even within this brighter overall exposure, entity_01 remains keyed as the brightest point, with entity_02/03/04 close behind and entity_05 (kitchen/window) exposed at or below her level — preserving the luminance hierarchy without reverting to Trial_02's moodier window-light falloff."
    },

    "MaterialPlan": {
      "supports": ["HierarchyPlan"],
      "source": "Emotion",
      "intent": ["tactile_credibility", "emotional_interpretation"],
      "possible_techniques": ["clean_specular_control", "crisp_surface_definition"],
      "human_skin_rendering": "Visible pores and natural tone variation; a relaxed, slightly asymmetric expression mid-savor. 'Crisp and polished, 8k photorealistic' governs surfaces and materials, NOT skin — no airbrushing or beauty-filter smoothing, per the Human Subject Rendering Requirement, which is non-negotiable regardless of style brief.",
      "reason": "The new brief's 'crisp and polished, 8k photorealistic' look is expressed through clean surface definition on the glass, pack, and counter — condensation and thick texture on the glass say 'tastes good'; matte kraft paper, scoop, and fresh produce say 'real food', all rendered with high clarity. Skin must stay textured and real for the unguarded moment to be believed, even as everything around it looks polished."
    },

    "AtmosphericPlan": {
      "supports": ["VisualFlowPlan"],
      "source": "Emotion",
      "intent": ["depth_perception", "environmental_mood"],
      "possible_techniques": ["clean_bright_atmosphere", "high_clarity_air"],
      "reason": "A clean, bright, crisp atmosphere with no haze supports the 'aspirational lifestyle marketing, 8k, photorealistic' register — the scene stays fresh and high-clarity rather than soft/hazy, while the Atmospheric depth-of-field gently separates the subject from the kitchen."
    },

    "OpticalPlan": {
      "supports": ["AttentionPlan"],
      "source": "Attention",
      "intent": ["attention_guidance", "perceptual_credibility"],
      "possible_techniques": ["progressive_bokeh_falloff"],
      "bokeh_behavior": "At 85mm/f4 (Atmospheric/Soft Focus), entity_01 (face and torso), entity_02 (glass at her body), entity_03 (pack), and entity_04 (ingredients) all sit within or near the focal plane and render crisp and fully detailed. entity_05 (kitchen behind her) falls progressively softer with distance — cabinetry lines and the window remain recognizable as bright, clean shapes but lose fine texture, never collapsing into hard cutout bokeh.",
      "reason": "This falloff keeps the 'clear product focus' (drink, pack, ingredients all sharp alongside the subject) while letting the kitchen read as a bright, polished, slightly softened backdrop — consistent with high-end fashion-campaign portraiture and the Atmospheric category."
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

- **Luminance Hierarchy:** entity_01 = Brightest (Primary), entity_02/03/04 = Mid (Secondary, well-lit and crisp), entity_05 = Dimmest (Supporting/backdrop) — preserved even though the overall lighting is brighter and more even than Trial_01/02's window-light treatment.
- **Depth of Field Category Selection:** Atmospheric/Soft Focus (f/4–f/5.6), selected at **f/4**. entity_02/03/04 carry independent communication weight, so Commercial Isolation is ruled out; entity_05 doesn't need full legibility, so Environmental Context is ruled out. f/4 (sharper end of Atmospheric) honors "clear product focus" from the new brief.
- **Camera (85mm, eye-level, medium/waist-up, mid distance):** directly implements the user's Angle/Distance brief (straight-on, neutral height, natural proportions, undistorted, half-body). The frontal camera position is reconciled with ArtDirection's "not performed to camera" requirement via entity_01's gaze remaining on the glass, not the lens.
- **Style brief vs. Human Subject Rendering Requirement:** "crisp and polished, 8k photorealistic" is interpreted as governing surfaces/materials/clarity, not skin — natural skin texture remains mandatory per `6.1 Composition_Rendering.md` regardless of style language.
- **`pose_variation_required: false`** — single human subject.
- **Boundary:** no messaging, narrative, or scene-construction changes — SceneContract (Trial_03) treated as source truth. All adjustments versus Trial_02 trace to the new Style/Angle/Distance brief and remain inside Composition & Rendering's "Visual Expression" remit.

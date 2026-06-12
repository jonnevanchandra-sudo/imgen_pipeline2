# Composition & Rendering Contract
**Brand:** Nike
**Campaign:** Nike Chill Run Club
**Framework:** Composition & Rendering v1.0
**Stage:** 6 — Visual Expression

---

## Inputs Consumed

- Reality Model: Realistic
- SceneContract entities: entity_01 (subjects), entity_02 (shoes), entity_03 (Nike apparel), entity_04 (HK evening environment)
- Depth Structure: Subjects foreground → Path midground → HK city background
- Focal Priority: Social dynamic between subjects → HK environment → Nike branding
- NarrativeIntent: Social vitality and belonging — warm, accessible, real
- Format: 4:5 vertical Instagram, top 10% and bottom 20% reserved for copy

---

```json
{
  "CompositionRenderingContract": {

    "HierarchyPlan": [
      {
        "element": "entity_01 — subject group faces and social interaction",
        "hierarchy_level": "Primary",
        "reason": "The social dynamic between subjects is the primary communication — viewer must immediately read human warmth, genuine interaction, and peer-level belonging. Faces and expression are the evidence of the narrative.",
        "source": "Narrative"
      },
      {
        "element": "entity_01 — full bodies in running motion including entity_02 (shoes)",
        "hierarchy_level": "Secondary",
        "reason": "Running context must be readable — this is not a standing portrait. Visible running posture, arms, and footwear confirm that movement is happening and that Nike running gear is being worn.",
        "source": "Narrative + Preservation"
      },
      {
        "element": "entity_04 — Hong Kong evening environment",
        "hierarchy_level": "Secondary",
        "reason": "HK location context is critical to campaign identity — the city must be recognizable as Hong Kong evening. Placed second so it frames and amplifies the subjects without competing.",
        "source": "Emotional + Environmental"
      },
      {
        "element": "entity_03 — Nike brand apparel element",
        "hierarchy_level": "Supporting",
        "reason": "Brand presence must be visible but not dominant. Seen in the natural context of a subject's clothing — perceived as part of the scene, not the focus of the image.",
        "source": "Preservation"
      }
    ],

    "AttentionPlan": {
      "entry_element": "entity_01 — faces and social dynamic (foreground center)",
      "attention_progression": [
        "entity_01 faces — immediate entry point; social energy and expression read first",
        "entity_01 bodies and running posture — eye travels down to confirm movement and running context",
        "entity_02 running shoes — feet and shoes confirm Nike running gear as part of the motion",
        "entity_04 HK environment — eye moves to background to read location and evening atmosphere"
      ],
      "exit_element": "entity_04 — HK city evening environment (background)",
      "mechanisms": [
        "sharpness_hierarchy — subjects in sharp focus, HK background in soft focus",
        "luminance_contrast — subjects naturally brighter under evening ambient light relative to background",
        "depth_separation — clear foreground/background separation reinforces subject dominance",
        "gaze_vectors — subjects' inward eye-lines pull viewer attention into the group social dynamic"
      ],
      "reason": "Attention must enter at the human faces — the social energy is the message. Running context is confirmed by the body. Brand is noticed but not sought. City location is read as atmospheric context after the human story is established."
    },

    "VisualFlowPlan": {
      "flow_direction": "top_to_bottom",
      "flow_pattern": "linear_vector",
      "supports": ["AttentionPlan"],
      "reason": "4:5 vertical format naturally drives top-to-bottom eye movement. Attention enters at faces (upper foreground), travels down the bodies through running posture to shoes, then expands to the HK environment in the background. This linear top-to-bottom flow is compatible with Instagram scroll behavior and keeps the hierarchy stable and readable."
    },

    "CameraPlan": {
      "perspective_intent": "eye_level",
      "framing_intent": "medium_shot",
      "distance_intent": "near",
      "supports": ["HierarchyPlan"],
      "source": "Hierarchy + Emotion",
      "reason": "Eye-level camera communicates equality — viewer stands alongside subjects, not observing from above or looking up at aspirational figures. This is the belonging relationship: these are peers, not figures to admire from a distance. Medium shot at near distance ensures faces are fully readable (primary hierarchy) while including enough of the body to confirm running motion and Nike footwear (secondary hierarchy). The 4:5 vertical format supports this framing — bodies fill the frame vertically without excessive negative space."
    },

    "LightingPlan": {
      "supports": ["HierarchyPlan"],
      "source": "Emotion + Hierarchy",
      "intent": [
        "subject_separation — subjects distinguished from HK background through natural luminance differential",
        "emotional_interpretation — warm evening light communicates social warmth and the feeling of a reclaimed evening",
        "depth_perception — foreground subjects brighter than background city environment"
      ],
      "LightingIntent": "Warm evening ambient light consistent with Hong Kong outdoor running at blue hour or early night. Subjects are naturally lit by a combination of city ambient glow and the last warmth of the fading day. The light is soft and directional — coming from slightly in front of and to one side, consistent with walking toward the city's ambient glow. Subjects are distinctly brighter and warmer than the background city environment without requiring artificial lighting. The lighting feels like a real HK evening, not a studio or a cinematic production.",
      "LightingRendering": "Warm color temperature (amber to gold) on subjects' skin and clothing from the combined effect of city ambient and evening sky. HK background city lights beginning to appear — warm orange and white point sources softly diffused in the background. No harsh shadows on faces. Natural rim separation where city light catches the back edges of subjects moving through the environment. Skin tones warm and well-rendered — natural and real.",
      "possible_techniques": [
        "city_ambient_fill — warm, omnidirectional fill from surrounding city lights",
        "evening_sky_backlight — soft warm backlight from sky gradient above and behind subjects"
      ],
      "reason": "The warm evening light serves the narrative directly: it communicates that this evening belongs to the subjects — it is beautiful, warm, and alive. The natural brightness differential between lit subjects and softer background city reinforces hierarchy without creating artificial separation."
    },

    "MaterialPlan": {
      "supports": ["HierarchyPlan"],
      "source": "Hierarchy + Emotion",
      "intent": [
        "tactile_credibility — all materials read as physically real",
        "emotional_interpretation — athletic apparel that feels worn and alive, not showroom-fresh"
      ],
      "MaterialBehavior": "Athletic apparel shows natural movement behavior — fabric drapes and shifts with running motion. Slight wrinkle and fold visible in clothing consistent with active movement. Nike shoes show natural material texture — mesh uppers, rubber soles — with slight motion dynamism from the running gait. Skin texture is natural and human — visible pore texture, natural tone variation, no over-smoothing or idealization. The path surface under subjects shows natural outdoor texture — not pristine, not worn out, but a real running surface.",
      "possible_techniques": [
        "fabric_drape_motion — clothing behaves as if subject is in motion",
        "surface_roughness_variation — path surface shows natural outdoor texture"
      ],
      "reason": "Material credibility is essential to the authenticity imperative. The image must feel photographed, not rendered. Overly perfect materials (too smooth, too uniform, too clean) immediately signal digital generation and break the peer-belonging relationship with the viewer."
    },

    "AtmosphericPlan": {
      "supports": ["VisualFlowPlan"],
      "source": "Emotion + RealityModel",
      "intent": [
        "depth_perception — atmospheric separation between foreground subjects and background HK environment",
        "environmental_mood — Hong Kong evening atmosphere: warm city glow, slight urban haze, the beginning of night"
      ],
      "AtmosphericBehavior": "Soft evening atmosphere in the background — the HK cityscape has a warm, slightly hazy quality consistent with Hong Kong's humid urban evening. City lights in the background are slightly diffused, creating warm atmospheric glow rather than sharp point sources. The foreground subjects are free of atmospheric haze — they are close and clear. The atmospheric depth naturally separates subjects from environment without requiring heavy post-processing.",
      "possible_techniques": [
        "aerial_perspective — natural depth haze in background city environment",
        "city_light_diffusion — warm bokeh glow from HK city lights in background"
      ],
      "reason": "The HK evening atmosphere serves the emotional narrative — this city is alive, warm, and beautiful at this hour. The atmosphere communicates that this is a good time and a good place to be. It also serves hierarchy by keeping background elements atmospherically soft relative to the crisp foreground subjects."
    },

    "OpticalPlan": {
      "supports": ["AttentionPlan"],
      "source": "Attention + RealityModel",
      "intent": [
        "attention_guidance — shallow depth of field isolates subjects in foreground",
        "perceptual_credibility — optical behavior consistent with real photography in this context"
      ],
      "OpticalIntent": "Shallow depth of field consistent with a moderate telephoto or fast prime lens used at near distance. The subject group is in sharp, crisp focus throughout — all subjects in the group must be in focus, not just the nearest one. The path midground is slightly soft. The HK background city environment is in soft, warm bokeh — city lights and architectural forms are visible but diffused. The bokeh quality is natural and circular — no anamorphic oval blur, no artificial optical effects. The HK cityscape and any background signage should remain identifiable as Hong Kong context despite the soft focus — not reduced to unreadable blur.",
      "possible_techniques": [
        "bokeh_blur_isolation — natural bokeh on HK background separates subjects from environment",
        "focus_consistency — all subjects in group in sharp focus simultaneously"
      ],
      "reason": "Optical treatment directly serves the attention hierarchy: crisp subjects, soft city. The optical behavior also signals quality and real photography — this is not a snapshot, this is well-executed lifestyle photography. The bokeh on the HK background must be calibrated to preserve location legibility — the viewer should be able to recognize Hong Kong, not just see colored blur."
    },

    "RenderingConstraints": {
      "reality_model_compliance": true,
      "preservation_compliance": true,
      "hierarchy_protection": true,
      "authenticity_mandate": "Rendering must prioritize human and environmental credibility over visual perfection. Natural skin texture and tone variation on all subjects. Natural motion artifacts in clothing and hair acceptable and preferred. Environmental imperfections (path texture, atmospheric haze) are correct. The image should be indistinguishable from a high-quality photograph taken by a skilled editorial photographer at a real HK evening running event."
    }

  }
}
```

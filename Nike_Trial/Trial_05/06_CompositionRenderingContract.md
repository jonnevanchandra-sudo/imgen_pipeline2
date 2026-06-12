# Composition & Rendering Contract
**Brand:** Nike
**Campaign:** Nike Chill Run Club
**Framework:** Composition & Rendering Framework v6.1
**Stage:** 6 — Visual Expression

---

```json
{
  "CompositionRenderingContract": {

    "HierarchyPlan": [
      {
        "element": "entity_01 + entity_02 — both subjects' faces and upper bodies",
        "hierarchy_level": "Primary",
        "reason": "The emotional argument lives in the subjects' faces — the expression of present-state liberation, the specific absence of the workday, the ease of a body that has found its rhythm. Both faces must be simultaneously readable at scroll speed. Neither subject has precedence — the visual parity of their stride is the whole point of the parallel liberation concept.",
        "source": "Narrative"
      },
      {
        "element": "entity_03 — Nike Novablast 5 mid-stride, ZOOMX midsole in profile",
        "hierarchy_level": "Primary",
        "reason": "This is a product awareness execution. The Novablast 5 must be clearly identifiable mid-stride — not a shoe glimpsed in passing, but a shoe legible enough that the viewer registers the ZOOMX midsole profile and the Volt Swoosh. The shoe shares Primary hierarchy with the subjects' faces because it is the visual and narrative bridge between viewer and the liberation they are watching. Hierarchy is split, not reduced — faces carry the emotion, shoe carries the argument.",
        "source": "Campaign"
      },
      {
        "element": "entity_04 — HK harbor golden hour atmosphere",
        "hierarchy_level": "Supporting",
        "reason": "The environment communicates when and where this liberation is available. It must read as Hong Kong at golden hour — warm, open, the city giving itself over to people who chose to move through it. It should not compete with the subjects for visual attention. The golden hour light is a supporting character: it wraps the subjects, it is not a spectacle in itself.",
        "source": "Environmental"
      }
    ],

    "AttentionPlan": {
      "entry_element": "subjects' faces — the expression of liberation (simultaneous entry at entity_01 and entity_02)",
      "attention_progression": [
        "entity_01 + entity_02 faces — expression of present-state ease and motion (simultaneous entry)",
        "entity_03 — Novablast 5 mid-stride, ZOOMX midsole profile and Volt Swoosh (sport identity and product recognition)",
        "entity_04 — HK harbor golden hour atmosphere (environmental grounding: this is Hong Kong, this is available to you)"
      ],
      "exit_element": "entity_04 — the warm atmospheric haze of HK harbor, implying the world beyond the frame",
      "mechanisms": [
        "sharpness_hierarchy — subjects and shoes in crisp foreground focus, background in warm bokeh",
        "luminance_contrast — golden hour backlight creates subtle rim separation on subjects against the warm background",
        "gaze_direction — subjects face forward (direction of motion), drawing viewer's eye through the frame in the same direction",
        "stride_geometry — the elongated stride lines of both subjects create a strong diagonal visual force through the frame"
      ],
      "reason": "The split-primary hierarchy (faces AND shoes) requires careful attention management. The shoe is kept in sharp focus mid-stride — same depth layer as the subjects — so it reads naturally rather than as a product insert. The stride diagonal pulls the eye through the frame: entry at faces, trace down through arms and torso, arrive at feet and shoes, exit through the HK environment behind them."
    },

    "VisualFlowPlan": {
      "flow_direction": "diagonal_downward — from faces to feet, following the natural line of a running body in full stride",
      "flow_pattern": "diagonal_linear",
      "supports": ["AttentionPlan"],
      "reason": "The human body in full stride creates a natural diagonal from face to foot. In a 4:5 vertical format, this diagonal fills the frame efficiently. The viewer's eye enters at the face, traces the running body down through torso, leg, and shoe, and exits into the HK environment. This reinforces the kinesthetic narrative: the motion of viewing the image mirrors the motion of running — continuous, directional, forward."
    },

    "CameraPlan": {
      "perspective_intent": "slightly_below_eye_level",
      "framing_intent": "medium_full_shot — subjects visible from head to shoe in full stride, ensuring both face and full shoe silhouette are readable in a single frame",
      "distance_intent": "near_to_medium — subjects fill the foreground; faces readable at Instagram mobile size; Novablast 5 ZOOMX midsole profile readable in the same frame",
      "angle_to_subjects": "slight_three_quarter — subjects run at approximately 30–45 degrees to the camera, not head-on and not purely side profile. This angle simultaneously shows: both faces in readable expression, the full stride including foot extension, and the lateral ZOOMX midsole profile of at least one shoe",
      "focal_length_mm": "50mm",
      "aperture_f_stop": "f/2.8",
      "supports": ["HierarchyPlan"],
      "source": "Hierarchy + Campaign",
      "reason": "The challenge is showing both readable faces AND a legible Novablast 5 shoe profile in a single medium shot. A head-on shot loses the shoe profile. A pure side shot loses the faces. The slight three-quarter angle at below-eye-level is the compositional solution: it places the camera at a height that looks slightly up at the subjects (creating energy and dynamism) while the 30–45 degree body orientation allows the lateral shoe to read. Below-eye-level also emphasizes the stride — feet come closer to the camera than in a straight-on eye-level shot. 50mm at f/2.8 is the natural-perspective, documentary-lens choice: it renders the subjects at near-true proportions (no wide-angle distortion on faces or stride), and f/2.8 gives enough depth of field to hold both subjects and the shoe sharp at this distance while still separating them from the harbor background."
    },

    "LightingPlan": {
      "supports": ["HierarchyPlan"],
      "source": "Emotion + Hierarchy",
      "intent": [
        "subject_separation_via_backlight",
        "golden_hour_warmth_on_skin",
        "shoe_midsole_legibility_via_rim_light"
      ],
      "possible_techniques": [
        "golden_hour_backlight_rim_on_subjects — sun low and behind/beside subjects creates warm rim separation against the atmospheric background",
        "ambient_reflected_fill_on_face — open sky fills the shadow side of faces so expressions remain readable despite the backlight",
        "warm_directional_sidelight — golden hour sun hitting subjects from the side, creating warm skin tones and natural texture without hard shadows",
        "Volt_midsole_catching_warm_light — the white ZOOMX foam base catches golden ambient light; Volt Swoosh and pods read in the same light"
      ],
      "reason": "Golden hour backlight creates the most powerful natural subject separation available — subjects glow against the warm haze of the HK harbor. It also communicates the time of day (the city at late afternoon, not morning) and reinforces the kinesthetic liberation narrative: this is the best hour of the day, the body's hour. The white ZOOMX midsole catches golden light naturally — the warmth enriches rather than obscures the Volt accents. The key challenge is ensuring faces are readable: the ambient fill from the open sky above must be strong enough to prevent the faces from being silhouetted against the backlight."
    },

    "MaterialPlan": {
      "supports": ["HierarchyPlan"],
      "source": "Authenticity",
      "intent": [
        "tactile_credibility_on_subjects",
        "shoe_material_accuracy"
      ],
      "possible_techniques": [
        "natural_skin_texture — pores, subtle tone variation, perspiration-adjacent moisture consistent with running",
        "fabric_in_motion — athletic wear moving with stride: slight flutter, natural drape shift, not static",
        "engineered_mesh_translucency — the Novablast 5 black mesh upper has a semi-translucent quality in direct light; should render as lightweight mesh, not solid fabric",
        "ZOOMX_foam_surface — the white midsole foam has a slightly matte, cushioned surface quality distinct from rubber; should render as foam, not plastic"
      ],
      "human_skin_rendering": "Both subjects' faces show visible pore texture and natural tone variation under the golden hour light, with a light perspiration sheen consistent with running pace — not a glossy or oiled look. Natural asymmetry in each subject's expression and features. No airbrushing, no beauty-filter smoothing, no porcelain skin. Skin must read as photographed, not retouched.",
      "reason": "Material accuracy on the Novablast 5 is required for product recognition. The ZOOMX foam has a specific visual texture — slightly matte and soft-edged — that distinguishes it from a generic rubber midsole. The engineered mesh upper is visually lightweight and semi-transparent, which communicates the shoe's modern construction. Both must read correctly in the golden hour light for the shoe to be identifiable as the specific model. Skin is also a material in this scene — given two close-up human subjects, unrealistically smooth skin would be the fastest signal that the image is AI-generated, undermining the editorial-photography reality model."
    },

    "AtmosphericPlan": {
      "supports": ["VisualFlowPlan"],
      "source": "Emotion",
      "intent": [
        "golden_hour_warmth",
        "HK_harbor_depth",
        "kinesthetic_energy"
      ],
      "possible_techniques": [
        "warm_golden_atmospheric_haze — the HK harbor background has a soft warm glow consistent with golden hour light scattering through urban air",
        "directional_light_rays_optional — subtle god-ray quality if compositionally appropriate, not dominant",
        "motion_context — if subjects are at full stride, slight motion blur on the non-leading foot or swinging arm reinforces the kinesthetic reality without compromising face and shoe sharpness"
      ],
      "reason": "The atmosphere communicates Hong Kong's specific outdoor golden hour quality: warm, slightly humid, urban-ambient, the city settling into the evening. This is distinct from a generic outdoor setting. The warmth of the background also creates natural subject separation — the subjects pop against the warm haze — and reinforces the emotional register of the image: this is a beautiful hour, and these people are in it."
    },

    "OpticalPlan": {
      "supports": ["AttentionPlan"],
      "source": "Attention",
      "intent": [
        "sharp_foreground_subjects_and_shoes",
        "warm_atmospheric_background_bokeh",
        "depth_separation"
      ],
      "possible_techniques": [
        "shallow_to_moderate_depth_of_field — both subjects in sharp focus; path surface immediately behind them transitioning to soft; HK harbor background in warm bokeh",
        "foreground_sharpness_priority — entity_01, entity_02, and entity_03 all in crisp focus simultaneously",
        "background_bokeh_calibrated_for_HK_legibility — harbor and skyline shapes readable through warm soft focus, not reduced to unidentifiable color"
      ],
      "bokeh_behavior": "At 50mm f/2.8, both subjects and the Novablast 5 sit within a single sharp depth band. Blur falloff is progressive, not a flat cutout: the path surface within ~1–2m behind the subjects is only mildly softened and still shows surface texture; the mid-distance (approximately 3–8m) softens further; the HK harbor and skyline at full distance render as smooth, warm, rounded bokeh shapes — water and skyline silhouettes still loosely identifiable as harbor/skyline, not reduced to a single flat color wash. No background element should appear uniformly blurred regardless of its actual distance.",
      "reason": "Both subjects must be simultaneously in sharp focus — the parallel liberation concept requires both faces to read clearly. The shoe must also be sharp to support product recognition. A very shallow depth of field that blurs one subject or the shoe would compromise both the narrative and the campaign requirement. The background may be soft — the HK harbor in warm atmospheric bokeh is ideal depth separation — but the entire foreground layer (subjects + shoes) must be crisp, and the softness behind them must follow real depth, not a uniform overlay."
    },

    "RenderingConstraints": {
      "reality_model_compliance": true,
      "preservation_compliance": true,
      "hierarchy_protection": true,
      "product_visibility_requirement": "Nike Novablast 5 ZOOMX midsole profile and Volt Swoosh must be legible mid-stride — this is a hard rendering constraint from CampaignContract ProductSpec",
      "natural_skin_rendering_required": true
    }
  }
}
```

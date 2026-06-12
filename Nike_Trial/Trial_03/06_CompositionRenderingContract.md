# Composition & Rendering Contract
**Brand:** Nike
**Campaign:** Nike Chill Run Club
**Framework:** Composition & Rendering Framework
**Stage:** 6 — Visual Expression

---

```json
{
  "CompositionRenderingContract": {

    "HierarchyPlan": [
      {
        "element": "entity_01 + entity_02 — both subjects' faces and the social connection between them",
        "hierarchy_level": "Primary",
        "reason": "The emotional argument lives in two places simultaneously: the expressions on both faces (present-state liberation — the specific ease of a workday left behind) and the visible social warmth between the two subjects. These two signals together are the image's core claim. Both faces must read clearly at Instagram mobile scroll speed.",
        "source": "Narrative + Strategy"
      },
      {
        "element": "entity_03 — Nike Alphafly 3 mid-stride, midsole in profile",
        "hierarchy_level": "High",
        "reason": "Product awareness is a campaign requirement. The Alphafly 3's midsole stack and Air Zoom pod windows must be legible mid-stride — the shoe is a supporting protagonist, not a footnote. It shares High hierarchy with the social connection; it does not compete with faces for Primary position.",
        "source": "Campaign"
      },
      {
        "element": "entity_04 — HK night cityscape",
        "hierarchy_level": "Supporting",
        "reason": "The city at night is the reward — the environment that makes the liberation feel real. It must read as unmistakably HK at night (city lights, warm glow, harbor atmosphere) without competing with subjects for visual attention. The city is the world they are moving through, not a backdrop.",
        "source": "Narrative"
      }
    ],

    "AttentionPlan": {
      "entry_element": "Both subjects' faces — simultaneous entry; the expression of ease lands first",
      "attention_progression": [
        "entity_01 + entity_02 faces — present-state liberation and social warmth (simultaneous entry)",
        "social connection between subjects — the quality of two people who are genuinely together in this run",
        "entity_03 — Alphafly 3 midsole profile mid-stride (product recognition)",
        "entity_04 — HK night cityscape (environmental reward: this is where you could be tonight)"
      ],
      "exit_element": "entity_04 — the warm ambient glow of HK at night, extending beyond the frame",
      "mechanisms": [
        "sharpness_hierarchy — subjects and shoes in crisp foreground focus; background city in warm night bokeh",
        "luminance_contrast — subjects lit against darker night background; they are the brightest elements in the frame",
        "gaze_and_social_energy — the connection between subjects draws viewer attention to the social dimension before the product",
        "stride_diagonal — body in running stride creates diagonal line from face to foot, guiding eye naturally to the shoe"
      ]
    },

    "VisualFlowPlan": {
      "flow_direction": "diagonal_downward — from faces through running bodies to feet and shoes; and laterally between the two subjects via the social connection",
      "flow_pattern": "dual_diagonal — one diagonal per subject (face to foot) with a horizontal social bridge between them at face level",
      "supports": ["AttentionPlan"],
      "reason": "Two subjects in parallel stride create a natural dual-diagonal in the vertical 4:5 frame. The social connection between their faces creates a horizontal link that anchors attention at the top of the frame. The eye enters at faces, bridges between subjects via the social energy, then traces each body downward to the Alphafly 3 in stride."
    },

    "CameraPlan": {
      "perspective_intent": "eye_level_to_slightly_below — camera at approximately chest height, looking slightly upward; creates forward momentum and a sense that subjects are moving toward and past the viewer; subjects feel present and dynamic, not observed from above",
      "framing_intent": "medium_full_shot — both subjects visible from head to shoe in stride; social connection between their upper bodies and faces is the compositional center; full shoe profile readable in the lower frame",
      "distance_intent": "near_to_medium — subjects fill the foreground; faces readable at Instagram mobile scale; Alphafly 3 midsole profile readable in same frame",
      "angle_to_subjects": "slight_three_quarter — subjects run at approximately 30–45 degrees to the camera, not head-on and not pure side profile; this angle shows both faces in readable expression AND the full lateral shoe profile simultaneously",
      "supports": ["HierarchyPlan"],
      "reason": "The night setting changes the camera calculus relative to a day shot — there is less ambient fill, which means face readability requires the camera to be close enough to capture the subjects before the background city light dominates. The slight three-quarter angle preserves both face visibility and shoe profile in a single frame. Eye-level-to-slightly-below creates energy without the subjects feeling elevated or distanced from the viewer."
    },

    "LightingPlan": {
      "supports": ["HierarchyPlan"],
      "source": "Night City Environment",
      "intent": [
        "subject_separation_from_dark_background",
        "warm_city_light_on_skin",
        "readable_faces_despite_night_setting",
        "shoe_midsole_visibility_at_night"
      ],
      "possible_techniques": [
        "warm_ambient_streetlamp_key_light — the primary light source is city streetlamps; warm amber-orange quality; comes from slightly above and to the side; enriches skin tone without harsh shadow",
        "diffuse_city_glow_fill — the ambient diffuse light from the HK city skyline provides a cooler secondary fill that keeps both faces readable; this warm-cool contrast (warm key + cooler ambient fill) is the specific quality of HK at night",
        "practical_light_sources_in_background — city lights, neon, harbor reflections glow warmly behind the subjects; subjects are brighter and crisper than background by being in foreground",
        "Alphafly_white_midsole_in_city_light — the tall white ZoomX midsole catches and reflects warm city ambient light; reads warmly lit, not clinically white; pod windows visible as contrast detail"
      ],
      "prohibited": [
        "No pure black darkness — HK at night is never fully dark; the city is always glowing",
        "No cold or blue-dominant lighting on faces — city ambient may be cooler but skin tones must read as warm",
        "No studio flash or strobe appearance",
        "No overly dramatic cinematic shadows that make faces unreadable",
        "No day or golden hour lighting — this is a night run"
      ]
    },

    "MaterialPlan": {
      "supports": ["HierarchyPlan"],
      "source": "Authenticity",
      "intent": [
        "tactile_skin_quality_in_city_light",
        "running_fabric_in_motion",
        "Alphafly_material_accuracy"
      ],
      "possible_techniques": [
        "night_skin_texture — natural skin under warm city ambient light; subtle warmth and texture visible; slight perspiration consistent with running",
        "fabric_in_motion — running apparel catching city light in motion; slight flutter, natural fabric movement; lightweight feel visible",
        "ZoomX_foam_surface — the white midsole foam has a matte, slightly textured cushioned quality distinct from rubber or plastic; reads as foam",
        "Flyknit_upper_texture — the thin red upper appears minimal and lightweight; visibly thinner than the midsole base beneath it",
        "pod_window_transparency — the two forefoot Air Zoom pod windows are visible as distinct circular forms through the transparent outsole section"
      ]
    },

    "AtmosphericPlan": {
      "supports": ["VisualFlowPlan"],
      "source": "Narrative + Environment",
      "intent": [
        "HK_night_city_atmosphere",
        "warm_city_light_bokeh",
        "kinesthetic_motion_energy"
      ],
      "possible_techniques": [
        "city_light_bokeh_background — HK harbor and skyline lights render as warm bokeh circles in the background; warmly colored, layered, unmistakably urban and specifically HK",
        "warm_cool_atmospheric_contrast — warm amber from streetlamps vs. cooler blue-tinted city glow; this two-temperature atmosphere is characteristic of HK at night and creates depth",
        "motion_context — slight motion blur on a trailing foot or swinging arm consistent with running speed; reinforces kinesthetic reality without compromising face and shoe sharpness"
      ]
    },

    "OpticalPlan": {
      "supports": ["AttentionPlan"],
      "source": "Attention",
      "intent": [
        "sharp_foreground_subjects_and_shoes",
        "warm_night_bokeh_background",
        "depth_separation_at_night"
      ],
      "possible_techniques": [
        "moderate_depth_of_field — both subjects and their shoes in crisp foreground focus; both must be sharp simultaneously; shallow enough to create depth separation from background city lights",
        "background_bokeh_as_city_lights — HK city lights render as warm bokeh circles behind the subjects; color and pattern of bokeh communicates HK urban night specifically",
        "foreground_sharpness_priority — entity_01, entity_02, and entity_03 all in crisp focus; no subject or shoe sacrificed for background drama"
      ]
    },

    "RenderingConstraints": {
      "reality_model_compliance": true,
      "preservation_compliance": true,
      "hierarchy_protection": true,
      "product_visibility_requirement": "Nike Alphafly 3 ZoomX midsole profile and twin forefoot Air Zoom pod windows must be legible mid-stride — hard rendering constraint from CampaignContract ProductSpec",
      "environment_requirement": "HK night setting is mandatory — not day, not golden hour, not blue hour; active city at night with warm city ambient glow"
    }

  }
}
```

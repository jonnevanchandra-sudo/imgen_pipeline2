# Composition & Rendering Contract
**Brand:** Hong Kong Football Association (HKFA)
**Campaign:** Hong Kong World Cup 2026 — Team Hoodie Launch
**Framework:** Composition & Rendering Framework
**Stage:** 6 — Visual Expression

---

```json
{
  "CompositionRenderingContract": {

    "HierarchyPlan": [
      {
        "element": "entity_01 (+ entity_02 if present) — face(s) and expression(s)",
        "hierarchy_level": "Primary",
        "reason": "The emotional argument of this campaign lives in the face. Quiet, personal pride — the expression of someone who knows where they are from. Faces must read clearly at Instagram mobile scroll speed. The campaign is won or lost at this level.",
        "source": "Narrative + Art Direction"
      },
      {
        "element": "entity_03 — HK World Cup 2026 hoodie, specifically the HKFA dragon crest and red colorway",
        "hierarchy_level": "High",
        "reason": "The hoodie is the product hero and the identity vehicle. The red dominates the frame through color mass. The dragon crest is the identity mark that makes this the HK hoodie and not any red hoodie — it must be legible at the scale the subject appears. Both the color and the crest are required for the product to communicate.",
        "source": "Campaign + ProductSpec"
      },
      {
        "element": "entity_04 — HK urban environment",
        "hierarchy_level": "Supporting",
        "reason": "The city is the argument for why the red hoodie matters. HK behind the subject confirms: this person is from here, the city is theirs, the hoodie belongs to this place. Must read as unmistakably HK without competing with faces or product for visual attention.",
        "source": "Narrative + Strategy"
      }
    ],

    "AttentionPlan": {
      "entry_element": "Subject face — the expression of quiet pride is the emotional hook at scroll speed",
      "attention_progression": [
        "entity_01 face — quiet, personal pride; lands first",
        "entity_03 red hoodie — color mass reads second; red dominates the body",
        "HKFA dragon crest — identity mark reads on the left chest once the hoodie is registered",
        "entity_04 HK environment — city reads in background as the place that makes this moment matter"
      ],
      "exit_element": "entity_04 — HK skyline or harbour extending warmly behind the subject",
      "mechanisms": [
        "sharpness_hierarchy — subject face and hoodie crest in crisp foreground focus; background in atmospheric bokeh",
        "color_dominance — Dragon Red is the dominant color mass in the frame; eye arrives at the hoodie via color before shape",
        "face_as_emotional_anchor — expression is the first thing the viewer reads at human scale",
        "scale_contrast — subject fills foreground; city recedes behind; crest is small but precise against the red body"
      ]
    },

    "VisualFlowPlan": {
      "flow_direction": "vertical_downward — from face to chest (crest) to lower torso; eye enters at face, descends through the red body to the crest",
      "flow_pattern": "face_to_crest — primary diagonal from face down to the dragon crest on left chest; city environment extends horizontally in background",
      "supports": ["AttentionPlan"],
      "reason": "The emotional argument (face) and the product identity (crest) are connected by the red body of the hoodie. The eye naturally flows from the face down the body to the crest — this is the attention path that sells both the person and the product in a single visual motion."
    },

    "CameraPlan": {
      "perspective_intent": "eye_level — camera at approximately face/chest height; subject feels present and equal to the viewer; not looked up at (heroic) or down at (diminished); documentary register",
      "framing_intent": "medium_to_upper_body_shot — subject from approximately waist to top of head; face large enough to read expression; chest large enough for crest to be legible; enough of the hoodie body to read the red colorway fully",
      "distance_intent": "medium — subject fills the central foreground; face readable at Instagram mobile scale; HKFA crest legible at natural scale",
      "angle_to_subjects": "slight_three_quarter or direct — subject faces slightly toward or directly at the viewer (unlike running campaigns, this is a presence/identity shot, not motion); slight three-quarter angle adds depth and life to the pose",
      "supports": ["HierarchyPlan"],
      "reason": "A medium, eye-level, slight-three-quarter framing gives the subject presence without heroic elevation. The face is large enough to carry emotional weight. The chest is large enough for crest legibility. The city environment has space in the background without dominating."
    },

    "LightingPlan": {
      "supports": ["HierarchyPlan"],
      "source": "HK Urban Night Environment",
      "intent": [
        "face_readability_in_city_light",
        "red_hoodie_reads_true_and_warm",
        "crest_visible_against_red_body",
        "HK_night_atmosphere_in_background"
      ],
      "possible_techniques": [
        "warm_city_ambient_key — warm amber-toned streetlamp light as primary; enriches skin tone naturally; red hoodie reads warm and saturated under this light",
        "cooler_city_skyline_fill — diffuse ambient from HK skyline glow provides secondary fill; the warm-cool contrast is specific to HK at night",
        "face_separation_from_background — subject lit warmly against a cooler, softer background; creates natural depth without dramatic shadow",
        "crest_contrast — the HKFA dragon crest badge reads as a slightly different material texture against the red fabric; city light catches it with subtle distinction"
      ],
      "prohibited": [
        "No studio flash or strobe appearance — this must read as outdoor documentary photography",
        "No cold or blue-dominant lighting on skin — city ambient may be mixed but skin tones must read as warm",
        "No purely dark setting — HK at night is never fully dark; the city radiates light",
        "No golden hour or daylight — this is evening to night; city lights are on",
        "No dramatic cinematic rim or split lighting — the emotional register is documentary, not cinematic"
      ]
    },

    "MaterialPlan": {
      "supports": ["HierarchyPlan"],
      "source": "Authenticity + ProductSpec",
      "intent": [
        "hoodie_fabric_reads_as_fabric",
        "crest_reads_as_embroidered_or_woven_badge",
        "skin_texture_under_city_light",
        "HK_environment_texture"
      ],
      "possible_techniques": [
        "hoodie_fabric_quality — the red fabric reads as athletic knit: slight texture, not plastic, not overly shiny; catches city light naturally and shows fold lines at natural wear points",
        "crest_badge_material — the dragon crest reads as a woven or embroidered badge; slightly raised from the fabric surface; distinct texture from the surrounding red knit",
        "drawstring_and_trim_detail — white trim at collar, cuffs, and hem reads as clean contrast stripe; adds product specificity without needing to be perfectly engineered",
        "natural_skin_texture — subject's skin under warm city ambient light; subtle natural texture; not AI-smooth; reads as a real person photographed"
      ]
    },

    "AtmosphericPlan": {
      "supports": ["VisualFlowPlan"],
      "source": "Narrative + Environment",
      "intent": [
        "HK_night_urban_atmosphere",
        "warm_city_glow_in_background",
        "lived_city_texture"
      ],
      "possible_techniques": [
        "city_light_bokeh — HK skyline and harbour lights render as warm bokeh in background; warm amber and cool blue-white city glow; layered and unmistakably urban HK",
        "warm_cool_city_atmosphere — the specific quality of HK at night: warm streetlamp orange + cooler high-rise glow; this two-temperature atmosphere is characteristic and adds authenticity",
        "documentary_grain — slight film-grain character consistent with real photography; reinforces the candid, documentary emotional register of the campaign"
      ]
    },

    "OpticalPlan": {
      "supports": ["AttentionPlan"],
      "source": "Attention",
      "intent": [
        "sharp_subject_face_and_crest",
        "warm_background_bokeh",
        "foreground_depth_separation"
      ],
      "possible_techniques": [
        "moderate_depth_of_field — subject face and hoodie crest in crisp focus; background city in warm atmospheric bokeh; depth separation without extreme lens effect",
        "background_bokeh_as_HK — city lights render as recognizable bokeh circles or streaks that communicate HK specifically; warm color, density, and layering read as this city",
        "foreground_sharpness_priority — face and crest are both sharp; neither sacrificed for background drama"
      ]
    },

    "RenderingConstraints": {
      "reality_model_compliance": true,
      "preservation_compliance": true,
      "hierarchy_protection": true,
      "product_visibility_requirement": "HKFA dragon crest must be legible on the left chest of the hoodie — hard rendering constraint from ProductSpec. Red colorway must dominate the frame through color mass.",
      "environment_requirement": "HK urban environment is mandatory — evening or night setting, city lights active, recognizably HK skyline or harbour character present"
    }

  }
}
```

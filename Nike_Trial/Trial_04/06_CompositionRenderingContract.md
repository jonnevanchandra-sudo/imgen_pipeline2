# Composition & Rendering Contract
**Brand:** Nike
**Campaign:** Nike Chill Run Club — Trial 04
**Framework:** Composition & Rendering Framework
**Stage:** 6 — Visual Expression

---

```json
{
  "CompositionRenderingContract": {

    "HierarchyPlan": [
      {
        "element": "entity_01 and entity_02 — faces and motion",
        "hierarchy_level": "Primary",
        "reason": "The emotional argument of this campaign lives in the faces and bodies in motion. Two people running together — ease, warmth, shared pace. The viewer needs to read both faces and the shared motion at Instagram scroll speed.",
        "source": "Narrative + Art Direction"
      },
      {
        "element": "entity_03 — Nike Alphafly 3 on feet",
        "hierarchy_level": "High",
        "reason": "The shoe is the product hero and the aspirational signal. Must be legible on at least one foot mid-stride — identifiable by stack height, swoosh, and racing silhouette. Not spotlit or isolated, but clearly present as part of the run.",
        "source": "CampaignContract ProductSpec"
      },
      {
        "element": "entity_04 — HK urban night environment",
        "hierarchy_level": "Supporting",
        "reason": "The city confirms: this run is happening in Hong Kong, at night, in the viewer's city. It extends the invitation without competing with the subjects.",
        "source": "Strategy + Narrative"
      }
    ],

    "AttentionPlan": {
      "entry_element": "Faces — the ease and warmth of mid-run social connection lands first",
      "attention_progression": [
        "entity_01 + entity_02 faces — ease in motion, not a performance",
        "Body language in stride — shared pace, close proximity, running together",
        "entity_03 Alphafly 3 — stack height and Swoosh register at foot level",
        "entity_04 HK environment — city lights and skyline complete the context"
      ],
      "exit_element": "HK skyline or harbour lights extending in the background",
      "mechanisms": [
        "sharpness_hierarchy — subjects in crisp foreground focus; background in motion-softened bokeh",
        "motion_language — mid-stride bodies communicate energy without needing to look athletic",
        "face_scale — both faces large enough to read expression and warmth at mobile scroll speed",
        "shoe_visibility — foot at mid-stride naturally exposes lateral shoe face; Swoosh legible"
      ]
    },

    "VisualFlowPlan": {
      "flow_direction": "lateral_then_down — eye enters at faces, reads both subjects horizontally, then descends to shoes at foot level",
      "flow_pattern": "face_pair → shared_stride → shoes → city_behind",
      "reason": "The horizontal pairing of two running subjects creates a natural left-right read at face level, then the eye follows the body downward to the shoes. The vertical 4:5 format supports this face-to-shoe flow."
    },

    "CameraPlan": {
      "perspective_intent": "slight_low_angle or eye_level — camera at approximately chest-to-waist height of running subjects; captures faces, upper body, and mid-stride shoe in a single field of view",
      "framing_intent": "medium_to_three_quarter_body — subjects from approximately mid-thigh to top of head; enough body to read the running stride and shoe; enough face to read expression",
      "distance_intent": "near_to_medium — subjects fill the frame; feels like running alongside them, not watching from the sideline",
      "angle_to_subjects": "slight_lateral or three_quarter — subjects running at slight angle toward or across the camera; both faces partially readable; mid-stride foot exposure natural from this angle",
      "motion_handling": "motion_captured — slight natural blur on limbs in stride is acceptable and increases authenticity; faces remain sharp",
      "reason": "A near-distance, slight-low or eye-level angle with lateral/three-quarter orientation puts the viewer inside the run. Both faces and the Alphafly 3 are readable in this framing. The city recedes naturally into background."
    },

    "LightingPlan": {
      "source": "HK Urban Night Environment",
      "intent": [
        "face_readability_in_city_light",
        "shoe_visible_on_moving_foot",
        "HK_night_atmosphere_behind_subjects"
      ],
      "possible_techniques": [
        "warm_city_ambient_key — warm amber streetlamp light from above and slightly ahead; enriches skin tone; reads warmly on athletic wear",
        "cooler_city_skyline_fill — diffuse ambient from HK skyline; the warm-cool contrast is characteristic of HK at night",
        "motion_fill — subjects slightly brighter than background through luminance contrast, not spotlight",
        "shoe_catch — ambient city light catches the lateral Swoosh and ZoomX stack at mid-stride naturally"
      ],
      "prohibited": [
        "No studio flash or strobe appearance",
        "No dramatic cinematic rim lighting — the register is documentary editorial, not Nike commercial production",
        "No cold or blue-dominant lighting on skin",
        "No golden hour or daylight — this is night",
        "No pure darkness — HK at night radiates city light"
      ]
    },

    "MaterialPlan": {
      "intent": [
        "running_apparel_in_motion",
        "alphafly_shoe_material_identity",
        "skin_texture_under_city_light"
      ],
      "possible_techniques": [
        "athletic_fabric_in_motion — apparel shows natural wind-catch and fold at running pace; not static",
        "ZoomX_foam_material — the midsole reads as lightweight foam: slightly matte, light in color relative to shoe, not rubber or hard plastic",
        "Atomknit_upper_material — thin and close-fitting; the upper conforms to the foot shape at running contact",
        "natural_skin_texture — real skin under warm city ambient; not over-smoothed or AI-idealized"
      ]
    },

    "AtmosphericPlan": {
      "intent": [
        "HK_night_run_atmosphere",
        "city_lights_in_motion_bokeh",
        "warm_cool_urban_air"
      ],
      "possible_techniques": [
        "city_light_bokeh — HK city lights render as warm amber and cool white bokeh streaks in background; motion-softened by the run",
        "warm_cool_city_atmosphere — warm streetlamp orange + cooler high-rise glow; characteristic HK night quality",
        "slight_motion_quality — the image feels taken at pace; slight ambient blur on periphery increases the sense of being inside the run"
      ]
    },

    "OpticalPlan": {
      "intent": [
        "sharp_subject_faces_and_bodies",
        "legible_shoe_at_stride",
        "HK_city_in_warm_motion_bokeh"
      ],
      "possible_techniques": [
        "moderate_to_shallow_depth_of_field — subjects sharp; city background in warm bokeh; shoe on mid-stride foot in sharp-to-moderate focus",
        "slight_motion_blur_on_limbs — natural motion blur on swinging arms and trailing foot increases authenticity without losing face sharpness",
        "background_bokeh_as_HK — city lights form warm recognizable bokeh that communicates HK specifically"
      ]
    },

    "RenderingConstraints": {
      "reality_model_compliance": true,
      "preservation_compliance": true,
      "hierarchy_protection": true,
      "subject_reference_requirement": "entity_01 appearance from reference_asset_01; entity_02 appearance from reference_asset_02 (Karina from aespa). Neither face generated independently.",
      "product_visibility_requirement": "Nike Alphafly 3 must be visible and recognizable on at least one foot mid-stride. Nike Swoosh legible. ZoomX stack height distinctive at running scale.",
      "environment_requirement": "HK outdoor urban at night — city lights active, recognizably HK"
    }

  }
}
```

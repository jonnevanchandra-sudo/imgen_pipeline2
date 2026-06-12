# Composition & Rendering Contract — FIT24 (Stage 6.1)

Framework: `6.1 Composition_Rendering.md`
Inputs: SceneContract (Stage 5.2.5)
Decision Type: Visual Expression — camera, light, hierarchy, flow. Priority order: Narrative Clarity > Hierarchy Stability > Attention Guidance > Emotional Reinforcement > Visual Beauty.

```json
{
  "CompositionRenderingContract": {

    "HierarchyPlan": {
      "primary": "entity_01 (runner, mid-stride on the treadmill)",
      "secondary": "entity_02 (FIT24 window-wall space — logo, treadmill row, window wall, ceiling)",
      "supporting": "Outdoor greenery view visible through the window glass",
      "luminance_priority": {
        "entity_01": "Brightest",
        "entity_02": "Mid",
        "outdoor_view_through_glass": "Dimmest (within frame) but naturally bright as a light source"
      },
      "rationale": "Primary (runner) is exposed as the brightest, clearly lit subject — front/side-lit by daylight from the window wall. The interior of entity_02 (logo, ceiling, treadmill row) sits at mid-luminance, clearly recognizable per its Critical preservation priority. The outdoor view through the glass is treated as supporting/atmospheric: it may render with natural daylight brightness (a realistic light source visible through glass), but framed so it does not dominate the frame's compositional weight — satisfying Primary >= Secondary/Supporting in compositional terms even where the outdoor sky/foliage is technically luminous."
    },

    "AttentionPlan": {
      "primary_mechanism": "luminance_contrast — runner is the clearest, most directly-lit element against the cooler interior tones of entity_02",
      "secondary_mechanisms": [
        "sharpness_hierarchy — runner rendered in critical focus; nearby treadmill row and FIT24 logo also sharp; window glass and outdoor view progressively softer",
        "gaze_vectors — runner's gaze directed forward toward the windows/view, leading the viewer's eye in the same direction, deeper into the frame",
        "directional_lines — the line of treadmills and the window-wall mullions create leading lines that converge toward the outdoor view, reinforcing depth",
        "depth_separation — clear foreground/midground/background layering (per SceneContract.DepthStructure) gives the eye a path: runner -> treadmill row/logo -> window wall -> outdoor greenery"
      ],
      "guardrail": "FIT24 logo (entity_02) must remain identifiable even at a 3/4 angle and reduced sharpness relative to the subject — softening should not be so aggressive that the logo becomes illegible (conflicts with Critical preservation priority); resolved via moderate, not extreme, falloff (see OpticalPlan)."
    },

    "VisualFlowPlan": {
      "entry_point": "Runner's face/upper body (brightest, sharpest, highest-contrast element)",
      "flow_path": "Face/torso -> treadmill console and FIT24 logo on the wall -> window wall and mullion lines -> outdoor greenery view",
      "exit_point": "Soft, bright outdoor greenery beyond the glass — no hard edges or distracting bright spots at the frame's outer corners"
    },

    "CameraPlan": {
      "shot_type": "Medium shot, slight 3/4 angle from the side — observational, not heroic/low-angle hero framing",
      "framing": "Vertical 4:5 (per CampaignContract.ChannelContext), runner positioned off-center (rule-of-thirds), window wall and FIT24 logo visible in the same frame",
      "focal_length_mm": 28,
      "aperture_f_stop": "f/8",
      "depth_of_field_category": "Environmental Context",
      "depth_of_field_rationale": "entity_02 (window wall, FIT24 logo, treadmill row) carries a Critical recognizability requirement and is core to the campaign's message ('train somewhere bright and open'). AttentionPlan does not call for isolating the subject from the environment — the environment IS part of the message. f/8 with a 28mm lens keeps the window wall, logo, and treadmill row legibly sharp while the outdoor view recedes via natural depth falloff."
    },

    "LightingPlan": {
      "key_light": "Natural daylight flooding in through the floor-to-ceiling window wall, lighting the runner from the front/side",
      "fill": "Soft ambient bounce off the polished tile flooring and interior surfaces — low-contrast fill, not a separate studio fill light",
      "accent": "Cool daylight tone throughout, with a subtle warm highlight where direct sun catches the treadmill consoles or flooring",
      "overall_mood": "Bright, airy, calm morning daylight — energizing but not harsh, supporting the 'good start to the day' narrative"
    },

    "MaterialPlan": {
      "human_skin_rendering": "Natural skin texture with visible pores, minor asymmetry, and a light, realistic sheen appropriate to a steady morning run — no airbrushing, no beauty-filter smoothing, no 'AI-perfect' symmetry",
      "glass_surfaces": "Window wall renders with realistic transparency and subtle reflections, not a flat/opaque or mirror-like surface",
      "metal_and_plastic": "Treadmills render with realistic matte/satin black plastic and metal finishes, consistent with the reference",
      "tile_flooring": "Polished, slightly reflective grey/dark tile finish matching the reference",
      "fabric": "Runner's athletic wear shows natural fabric movement and slight sweat-darkening consistent with active running, not a clean/pressed look"
    },

    "AtmosphericPlan": {
      "air_quality": "Clean indoor air, no haze or fog effects",
      "ambient_particulates": "None — avoid dust-mote/god-ray effects that would feel staged"
    },

    "OpticalPlan": {
      "bokeh_behavior": "Progressive, depth-dependent optical falloff tied to focal_length_mm=28 and aperture_f_stop=f/8: entity_01 (runner) and the nearest treadmills/FIT24 logo in critical focus; the window wall and mullions mildly softened — logo and window-wall structure remain legible; the outdoor greenery beyond the glass shows the most softening, recognizable as trees/foliage but without fine detail. No flat/uniform background blur."
    },

    "RenderingConstraints": {
      "natural_skin_rendering_required": true,
      "pose_variation_required": false,
      "pose_variation_note": "Single-subject scene — multi-subject pose variation requirement does not apply"
    },

    "PerceptualValidationAssertions": [
      {
        "assertion": "Skin Naturalism Assertion",
        "check": "The runner's visible skin shows natural texture, pores, and minor asymmetry consistent with a real photograph; no airbrushed or beauty-filtered appearance."
      },
      {
        "assertion": "Depth of Field Realism Assertion",
        "check": "Background blur (window wall and outdoor view) shows progressive, depth-dependent falloff consistent with a 28mm lens at f/8 — not a flat uniform blur — while the FIT24 logo and window-wall structure remain identifiable at mild softening."
      },
      {
        "assertion": "Recognizability Assertion",
        "check": "entity_02 (window wall, green outdoor view, FIT24 logo, treadmill row, exposed ceiling) is identifiable as matching reference_asset_01, per SceneContract preservation priorities."
      }
    ]
  }
}
```

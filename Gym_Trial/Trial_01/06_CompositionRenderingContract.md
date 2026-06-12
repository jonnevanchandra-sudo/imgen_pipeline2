# Composition & Rendering Contract — Anytime Fitness Sai Ying Pun (Stage 6.1)

Framework: `6.1 Composition_Rendering.md`
Inputs: SceneContract (Stage 5.2.5)
Decision Type: Visual Expression — camera, light, hierarchy, flow. Priority order: Narrative Clarity > Hierarchy Stability > Attention Guidance > Emotional Reinforcement > Visual Beauty.

```json
{
  "CompositionRenderingContract": {

    "HierarchyPlan": {
      "primary": "entity_01 (student, mid-rep on the rack)",
      "secondary": "entity_02 (Torque rack + colorful bumper plates) and entity_03 (AF wall + functional rig)",
      "supporting": "entity_04 (broader gym floor — ceiling, treadmill row, additional equipment)",
      "luminance_priority": {
        "entity_01": "Brightest",
        "entity_02": "Mid",
        "entity_03": "Mid",
        "entity_04": "Dimmest"
      },
      "rationale": "Primary (student) is brightest to anchor attention immediately. Secondary entities (rack + AF wall) sit at mid-luminance — bright enough to be clearly recognizable per the Critical/High preservation priorities, but not competing with the subject. Supporting background recedes into the dimmest tier, consistent with Primary >= Secondary/Supporting."
    },

    "AttentionPlan": {
      "primary_mechanism": "luminance_contrast — student is the brightest element against a comparatively dimmer surrounding space",
      "secondary_mechanisms": [
        "sharpness_hierarchy — student rendered in critical focus; rack (entity_02) in the student's hands also sharp; AF wall (entity_03) and background (entity_04) progressively softer",
        "gaze_vectors — student's gaze directed down/inward toward the rack/weight, keeping attention within the frame rather than toward camera or off-frame",
        "depth_separation — clear foreground/midground/background layering (per SceneContract.DepthStructure) gives the eye a natural path: student -> rack -> AF wall -> gym floor"
      ],
      "guardrail": "AF wall (entity_03) must remain identifiable even at reduced sharpness — softening should not be so aggressive that the 'AF' monogram becomes illegible (conflicts with Critical preservation priority); resolved via moderate, not extreme, falloff (see OpticalPlan)."
    },

    "VisualFlowPlan": {
      "entry_point": "Student's face/upper body (brightest, sharpest, highest-contrast element)",
      "flow_path": "Face/torso -> hands and rack (entity_02) -> AF wall and rig (entity_03) in the midground -> gym floor receding into entity_04",
      "exit_point": "Soft background depth (entity_04) — no hard edges or bright spots at frame edges that would pull the eye out of frame"
    },

    "CameraPlan": {
      "shot_type": "Medium shot, slightly low or eye-level angle — observational, not heroic/low-angle hero framing",
      "framing": "Vertical 4:5 (per CampaignContract.ChannelContext), student positioned off-center (rule-of-thirds) to leave room for the AF wall in the midground",
      "focal_length_mm": 35,
      "aperture_f_stop": "f/8",
      "depth_of_field_category": "Environmental Context",
      "depth_of_field_rationale": "entity_02 and entity_03 carry meaningful recognizability/communication roles (CampaignContract requires the gym be recognizable as Anytime Fitness Sai Ying Pun via the AF wall and the specific rack). AttentionPlan does not call for isolating the subject from the environment — the environment is part of the message. f/8 keeps secondary entities legibly sharp while still allowing entity_04 to recede via natural depth falloff."
    },

    "LightingPlan": {
      "key_light": "Practical-feeling overhead LED panels (consistent with the recessed ceiling grid observed in entity_04/reference_asset_01), positioned to fall naturally across the student",
      "fill": "Soft ambient bounce off the black rubber flooring and mirrored surfaces typical of the space — low-contrast fill, not a separate studio fill light",
      "accent": "A subtle warm/cool contrast between the purple-lit functional zone (entity_03) and the cooler white LED-lit main floor (entity_04), used to visually separate midground from background without introducing artificial colored gels",
      "overall_mood": "Even, slightly cool commercial-gym lighting — bright enough to feel safe and welcoming (supports 'approachable' strategy), not moody or dramatic"
    },

    "MaterialPlan": {
      "human_skin_rendering": "Natural skin texture with visible pores, minor asymmetry, and realistic sheen/sweat appropriate to mid-workout exertion — no airbrushing, no beauty-filter smoothing, no 'AI-perfect' symmetry",
      "metal_surfaces": "Rack (entity_02) renders with realistic brushed-metal/painted-steel reflectivity, matching the silver Torque USA finish in the reference",
      "rubber_flooring": "Matte, slightly textured rubber tile finish for both the black main floor and the purple functional-zone flooring",
      "fabric": "Student's athletic wear shows natural fabric wrinkling and slight sweat-darkening consistent with active use, not a clean/pressed look"
    },

    "AtmosphericPlan": {
      "air_quality": "Clean indoor air, no haze or fog effects",
      "ambient_particulates": "None — avoid dust-mote/god-ray effects that would feel staged for a commercial gym setting"
    },

    "OpticalPlan": {
      "bokeh_behavior": "Progressive, depth-dependent optical falloff tied to focal_length_mm=35 and aperture_f_stop=f/8: entity_01 and entity_02 in critical focus; entity_03 (AF wall, midground) only mildly softened — monogram and wordmark remain legible; entity_04 (background gym floor) shows the most softening, with shapes and equipment outlines still recognizable but details (e.g. treadmill screens) not legible. No flat/uniform background blur."
    },

    "RenderingConstraints": {
      "natural_skin_rendering_required": true,
      "pose_variation_required": false,
      "pose_variation_note": "Single-subject scene — multi-subject pose variation requirement does not apply"
    },

    "PerceptualValidationAssertions": [
      {
        "assertion": "Skin Naturalism Assertion",
        "check": "The student's visible skin shows natural texture, pores, and minor asymmetry consistent with a real photograph; no airbrushed or beauty-filtered appearance."
      },
      {
        "assertion": "Depth of Field Realism Assertion",
        "check": "Background blur (entity_04) shows progressive, depth-dependent falloff consistent with a 35mm lens at f/8 — not a flat uniform blur — while entity_03 remains identifiable (AF monogram/wordmark legible) at mild softening."
      },
      {
        "assertion": "Recognizability Assertion",
        "check": "entity_02 (Torque rack + colorful bumper plates) and entity_03 (AF wall, purple flooring, branded rig/bag) are identifiable as matching their respective reference assets, per SceneContract preservation priorities."
      }
    ]
  }
}
```

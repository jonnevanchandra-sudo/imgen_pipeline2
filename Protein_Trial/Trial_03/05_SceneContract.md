# Scene Contract — Natural Protein Powder (Stage 5.2.5, Trial_03)

Framework: `5.2.5 Scene-Assembly.md`
Inputs: ArtDirectionContract (Stage 4, unchanged from Trial_01/02) + CampaignContract.MandatoryRequirements (Stage 1, unchanged) + New Creative Direction (below)

**Run mode:** No reference images uploaded → Reference Asset Extraction **skipped**, no `ReferenceAssetManifest`. No `ClientPreferenceContract`. No `ProductSpec` in the CampaignContract (generic pack). Base Scene Assembly.

## New Creative Direction (this trial)

The user supplied an explicit photographic brief to reshape Stage 5/6:

> **Style:** commercial advertising photography, high-end fashion campaign, crisp and polished, bright even lighting, clear product focus, aspirational lifestyle marketing, 8k, photorealistic
> **Angle:** eye-level angle, straight-on camera perspective, neutral camera height, natural proportions, direct forward viewpoint, undistorted perspective
> **Distance:** medium shot, waist-up portrait, mid-length framing, half-body shot, balanced camera distance, showing upper body and face

This is read as a **camera/rendering treatment upgrade**, not a change to ArtDirectionContract's concept. Concretely, at Stage 5 it means:

- Reframe the scene so entity_01 (the subject) is **dominant in a waist-up, frontal composition** — the counter items (drink, pack, ingredients) move into her immediate hand/counter space so they remain in a half-body frame.
- entity_05 (kitchen) becomes a **bright, clean, aspirational backdrop** rather than a cluttered "lived-in" kitchen — still recognizably a home kitchen (ArtDirection requires "their own kitchen"), but tidier and brighter, consistent with "aspirational lifestyle marketing."
- The camera being positioned frontally/straight-on does **not** mean the subject performs toward it — ArtDirection's ToneGuard ("any performed, to-camera delight collapses credibility") is preserved by keeping entity_01's gaze and attention on the glass/product, not on the lens. Camera framing and subject attention are independent variables.
- Aperture/lighting/focal-length specifics belong to Stage 6 and are not decided here.

```json
{
  "SceneContract": {
    "RealityModel": {
      "type": "Realistic",
      "coherence_rules": {
        "scale": "realistic",
        "perspective": "realistic",
        "anchoring": "required",
        "environmental_behavior": "realistic"
      }
    },

    "Entities": [
      {
        "id": "entity_01",
        "description": "A woman in her early thirties, in relaxed-but-put-together home clothing (soft knit top), standing at her kitchen counter in a frontal, eye-level, waist-up composition — facing toward the camera in body orientation, but her gaze and attention stay down on the glass she holds at chest/waist height, caught mid-savor just after a sip: eyes softened or briefly closed, an unguarded half-smile. Her enjoyment is private and genuine, not performed toward the lens, even though the camera itself sits squarely in front of her.",
        "roles": ["Identity-Bearing", "Structural"],
        "source": "Generated"
      },
      {
        "id": "entity_02",
        "description": "A glass of thick, creamy smoothie — pale oat-vanilla tone with a faint berry swirl, visible texture and body — held close to her body at chest/waist height, near her lips.",
        "roles": ["Symbolic", "Structural"],
        "source": "Generated"
      },
      {
        "id": "entity_03",
        "description": "The protein powder pack — a matte kraft-paper pouch, open, with a clean minimal label free of legible text; a wooden or steel scoop of powder resting beside or in it — positioned on the counter directly beside/in front of her, within the waist-up frame.",
        "roles": ["Brand-Bearing", "Symbolic"],
        "source": "Generated"
      },
      {
        "id": "entity_04",
        "description": "Natural ingredients in just-used (but tidy) arrangement on the counter beside her: a peeled banana, a small scatter of rolled oats, a few fresh berries, a split vanilla pod — recognizable real foods, within the frame at waist level.",
        "roles": ["Symbolic", "Supporting"],
        "source": "Generated"
      },
      {
        "id": "entity_05",
        "description": "A bright, clean, aspirational home kitchen in even daylight — tidy counter and cabinetry, a window out of focus behind her, the kind of polished-but-lived-in kitchen seen in lifestyle marketing.",
        "roles": ["Environmental"],
        "source": "Generated"
      }
    ],

    "Relationships": [
      { "subject": "entity_01", "relation": "holding", "object": "entity_02" },
      { "subject": "entity_03", "relation": "adjacent_to", "object": "entity_04" },
      { "subject": "entity_03", "relation": "resting_on", "object": "entity_05" },
      { "subject": "entity_04", "relation": "resting_on", "object": "entity_05" },
      { "subject": "entity_01", "relation": "standing_at", "object": "entity_05" },
      { "subject": "entity_05", "relation": "visible_behind", "object": "entity_01" }
    ],

    "AnchorRelationships": [
      { "entity_id": "entity_01", "anchor_type": "floor_anchored" },
      { "entity_id": "entity_02", "anchor_type": "held_by_entity_01" },
      { "entity_id": "entity_03", "anchor_type": "surface_anchored (counter)" },
      { "entity_id": "entity_04", "anchor_type": "surface_anchored (counter)" },
      { "entity_id": "entity_05", "anchor_type": "scene_envelope" }
    ],

    "DepthStructure": {
      "foreground": ["entity_01", "entity_02"],
      "midground": ["entity_03", "entity_04"],
      "background": ["entity_05"]
    },

    "RelativeScale": [
      { "entity_id": "entity_01", "reference_entity": "entity_05", "scale_relationship": "Subject is the dominant element in a waist-up portrait frame, facing the camera at natural human scale and proportions." },
      { "entity_id": "entity_02", "reference_entity": "entity_01", "scale_relationship": "Held close to her body at chest/waist height, at natural glass scale." },
      { "entity_id": "entity_03", "reference_entity": "entity_04", "scale_relationship": "Pack sits at true pouch scale on the counter beside the ingredients, within reach of the subject — present and identifiable, visually subordinate to the subject and glass." }
    ],

    "GenerationRequirements": {
      "required_entities": ["entity_01", "entity_02", "entity_03", "entity_04"],
      "required_supporting_objects": ["scoop with powder"],
      "required_environment_elements": ["kitchen counter surface within the waist-up frame", "bright even daylight"]
    },

    "PreservationContracts": [
      {
        "entity_id": "entity_01",
        "preservation_priority": "Critical",
        "recognizability_requirement": "Strong Match",
        "source": "Generated",
        "immutable_attributes": [
          "single subject (not a group)",
          "genuine, unperformed savoring expression — caught mid-moment, not posed to camera, even though the camera angle is frontal",
          "casual home clothing (no athletic wear)",
          "glass held at or near lips — the sip just happened",
          "gaze/attention directed at the glass/moment, not at the camera"
        ],
        "flexible_attributes": [
          "exact age within 25–40, ethnicity, hair",
          "standing position relative to counter",
          "exact garment and color"
        ]
      },
      {
        "entity_id": "entity_02",
        "preservation_priority": "Critical",
        "recognizability_requirement": "Strong Match",
        "source": "Generated",
        "immutable_attributes": [
          "visibly thick, creamy blended texture — reads as real food",
          "natural pale oat-vanilla tone (no artificial neon color)"
        ],
        "flexible_attributes": ["glass shape", "berry swirl present or not", "fill level"]
      },
      {
        "entity_id": "entity_03",
        "preservation_priority": "High",
        "recognizability_requirement": "Approximate Match",
        "source": "Generated",
        "immutable_attributes": [
          "reads instantly as a protein powder pouch (open, scoop present)",
          "matte kraft/natural material — no glossy supplement-tub styling",
          "NO legible text or invented logo on the label"
        ],
        "flexible_attributes": ["pouch proportions", "label color blocking", "scoop material"]
      },
      {
        "entity_id": "entity_04",
        "preservation_priority": "High",
        "recognizability_requirement": "Strong Match",
        "source": "Generated",
        "immutable_attributes": [
          "each ingredient individually recognizable as real food (banana, oats, berries, vanilla pod)",
          "casually present, not a styled commercial flat-lay"
        ],
        "flexible_attributes": ["exact ingredient subset and count", "arrangement"]
      },
      {
        "entity_id": "entity_05",
        "preservation_priority": "Medium",
        "recognizability_requirement": "Loose Match",
        "source": "Generated",
        "immutable_attributes": ["home kitchen, bright even daylight"],
        "flexible_attributes": ["kitchen style — may read as more polished/modern (aspirational) rather than rustic", "background objects", "window position"]
      }
    ]
  }
}
```

> **Omitted by design:** `reference_locked_entities`, `ReferenceAssetManifest`, `client_preference_influence`, `ClientPreferenceConflicts` — no uploaded assets, no client preference contract in this run.

## Downstream Handoff

- Single human subject → Stage 6.1's Multi-Subject Pose Variation Requirement will not trigger (`pose_variation_required: false` expected); Human Subject Rendering Requirement (natural skin) WILL apply — "crisp/polished" style language does NOT override this mandatory requirement.
- entity_03's "no legible text" immutable must survive to the NEGATIVE block.
- entity_01's gaze-on-product / not-on-camera attribute must survive into Stage 6's CameraPlan reasoning so the new frontal/eye-level framing doesn't collapse into "posed to camera."
- The waist-up, frontal reframing pulls entity_03/entity_04 into midground (within-frame, beside the subject) rather than Trial_02's close foreground — Stage 6 should treat entity_01 as visually dominant with the product/ingredients as secondary elements sharing her frame, not separate foreground objects.

# Scene Contract — CLEVER Weight Down "3 PM Office Rescue" (Stage 5.2.5)

Framework: `5.2.5 Scene-Assembly.md`
Inputs: ArtDirectionContract (Stage 4) + CampaignContract.MandatoryRequirements.ProductSpec (Stage 1)
Decision Type: Scene Construction — spatial blueprint and preservation contracts.

**Run mode:** No reference images uploaded → Reference Asset Extraction **skipped**, no `ReferenceAssetManifest`. No `ClientPreferenceContract` (Stage 5.5 skipped — client hasn't responded to the Visual Discovery Package, Stage 1.5). `ProductSpec` IS present in CampaignContract (CLEVER Weight Down) → the named-product-model rule (v5.1) applies: `entity_01` is locked using `ProductSpec.key_visual_identifiers` directly, as a Generated entity (no reference image needed).

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
        "description": "The CLEVER Weight Down product — a stand-up pouch in the brand's soft pink/rose-and-white minimalist packaging, with the CLEVER wordmark and '減重蛋白'/Weight Down naming on the front label, shown alongside (or as) a prepared shake in a glass or shaker bottle. This is the 'already chosen' object in the scene — composed, clean, occupying the resolved foreground position.",
        "roles": ["Brand-Bearing", "Symbolic", "Structural"],
        "source": "Generated"
      },
      {
        "id": "entity_02",
        "description": "A typical HK office 3pm snack-run order — siu mai (steamed pork dumplings) in a takeaway container alongside a cold tea drink (iced lemon tea or bubble tea) in a disposable cup. Presented in an ordinary, slightly worn takeaway manner — not styled. This is the 'passed-over' option, present in the scene but visually receding.",
        "roles": ["Symbolic", "Supporting"],
        "source": "Generated"
      },
      {
        "id": "entity_03",
        "description": "A single human hand, reaching toward or resting near entity_01 — natural skin texture, no face or other identity-bearing features visible. Grounds the scene as an ordinary mid-afternoon moment ('my desk, my 3pm') without introducing a posed human subject.",
        "roles": ["Supporting"],
        "source": "Generated"
      },
      {
        "id": "entity_04",
        "description": "An ordinary HK office desk at mid-afternoon — desk surface with everyday work objects at the edges (e.g. laptop edge, notebook, pen), ambient interior daylight.",
        "roles": ["Environmental"],
        "source": "Generated"
      }
    ],

    "Relationships": [
      { "subject": "entity_03", "relation": "reaching_toward", "object": "entity_01" },
      { "subject": "entity_01", "relation": "resting_on", "object": "entity_04" },
      { "subject": "entity_02", "relation": "resting_on", "object": "entity_04" },
      { "subject": "entity_02", "relation": "positioned_apart_from", "object": "entity_01" },
      { "subject": "entity_04", "relation": "visible_behind", "object": "entity_01" }
    ],

    "AnchorRelationships": [
      { "entity_id": "entity_01", "anchor_type": "surface_anchored (desk)" },
      { "entity_id": "entity_02", "anchor_type": "surface_anchored (desk)" },
      { "entity_id": "entity_03", "anchor_type": "extends_into_frame" },
      { "entity_id": "entity_04", "anchor_type": "scene_envelope" }
    ],

    "DepthStructure": {
      "foreground": ["entity_01", "entity_03"],
      "midground": ["entity_04"],
      "background": ["entity_02"]
    },

    "RelativeScale": [
      { "entity_id": "entity_01", "reference_entity": "entity_04", "scale_relationship": "Product sits at true pouch/shake scale on the desk surface, occupying the dominant foreground position closest to the viewer." },
      { "entity_id": "entity_02", "reference_entity": "entity_01", "scale_relationship": "Snack/drink items are at true takeaway scale, positioned further back or to the side of the desk — present and recognizable but visually subordinate to entity_01." },
      { "entity_id": "entity_03", "reference_entity": "entity_01", "scale_relationship": "Hand is at natural human scale relative to the product, entering the frame to interact with it." }
    ],

    "GenerationRequirements": {
      "required_entities": ["entity_01", "entity_02", "entity_04"],
      "required_supporting_objects": ["entity_03 — single human hand interacting with entity_01"],
      "required_environment_elements": ["office desk surface", "ambient mid-afternoon interior daylight", "incidental everyday work objects at frame edges"]
    },

    "PreservationContracts": [
      {
        "entity_id": "entity_01",
        "preservation_priority": "Critical",
        "recognizability_requirement": "Near Exact",
        "source": "Generated",
        "immutable_attributes": [
          "Product name: CLEVER Weight Down (減重蛋白)",
          "Stand-up pouch packaging (~315g format) in the brand's soft pink/rose-and-white minimalist palette",
          "'CLEVER' wordmark in clean, contemporary all-caps sans-serif on the front label",
          "'減重蛋白' / 'Weight Down' product naming visible on the label",
          "Prepared shake shown as a smooth, uniform beverage in a glass or shaker bottle, color consistent with the depicted flavor"
        ],
        "flexible_attributes": [
          "Specific flavor depicted (matcha latte / chocolate / yogurt / mixed berries) and corresponding shake color",
          "Pouch shown open or closed, scoop present or not",
          "Whether both pouch and prepared shake are shown, or shake only",
          "Exact placement, rotation, and scale on the desk"
        ],
        "client_preference_influence": null
      },
      {
        "entity_id": "entity_02",
        "preservation_priority": "Medium",
        "recognizability_requirement": "Approximate Match",
        "source": "Generated",
        "immutable_attributes": [
          "Recognizable as a typical HK office snack-run order — siu mai (steamed pork dumplings) in a takeaway container and/or a cold tea drink (iced lemon tea or bubble tea) in a disposable cup",
          "Presented in an ordinary, slightly worn takeaway/disposable manner — not styled or elevated"
        ],
        "flexible_attributes": [
          "Exact snack items chosen (siu mai vs. fish balls vs. other common HK snack-run items)",
          "Container/cup design details",
          "Position within the scene (may be partially out of frame)"
        ],
        "client_preference_influence": null
      },
      {
        "entity_id": "entity_03",
        "preservation_priority": "Medium",
        "recognizability_requirement": "Loose Match",
        "source": "Generated",
        "immutable_attributes": [
          "A single human hand, reaching toward or resting on entity_01",
          "Natural skin texture per Stage 6.1 Human Subject Rendering Requirement — no airbrushed/AI-perfect skin",
          "No face or other identity-bearing features visible"
        ],
        "flexible_attributes": [
          "Exact hand position, gesture, skin tone, nail/accessory details",
          "Sleeve/cuff visible or not"
        ],
        "client_preference_influence": null
      },
      {
        "entity_id": "entity_04",
        "preservation_priority": "Medium",
        "recognizability_requirement": "Loose Match",
        "source": "Generated",
        "immutable_attributes": [
          "Reads as an ordinary HK office desk at mid-afternoon, with ambient interior daylight"
        ],
        "flexible_attributes": [
          "Desk material and color",
          "Specific incidental objects present at frame edges",
          "Light source direction and exact time-of-day cues beyond 'afternoon'"
        ],
        "client_preference_influence": null
      }
    ]
  }
}
```

> **Omitted by design:** `reference_locked_entities`, `ReferenceAssetManifest`, `ClientPreferenceConflicts` — no uploaded assets, no client preference contract in this run.

## Downstream Handoff

- entity_01 (CLEVER Weight Down) is the named-product entity from `ProductSpec` — both the product name AND the visual descriptor summary must reach the Prompt Compiler's `brand` key in HIGH, name first, descriptors following.
- entity_01's 'CLEVER' wordmark and '減重蛋白'/Weight Down label text are the only legible-text elements required by the brand; Stage 8's Compression System and NEGATIVE block should constrain text rendering to these specific short strings and forbid any other invented/legible text (per CampaignContract.PlatformConstraints — no other on-image text expected).
- Single human subject is reduced to a hand only (entity_03) → Stage 6.1's Multi-Subject Pose Variation Requirement will not trigger (`pose_variation_required: false` expected); Human Subject Rendering Requirement (natural skin texture) WILL apply to entity_03.
- entity_01 vs. entity_02 spatial relationship (foreground/resolved vs. background/receding) is the scene-construction expression of Art Direction's "Quiet Swap" concept — Composition & Rendering (Stage 6.1) determines how depth-of-field and lighting express this relationship.

# Scene Contract — Natural Protein Powder (Stage 5.2.5)

Framework: `5.2.5 Scene-Assembly.md`
Inputs: ArtDirectionContract (Stage 4) + CampaignContract.MandatoryRequirements (Stage 1)
Decision Type: Scene Construction — spatial blueprint and preservation contracts.

**Run mode:** No reference images uploaded → Reference Asset Extraction **skipped**, no `ReferenceAssetManifest`. No `ClientPreferenceContract` (Stage 5.5 skipped — client hasn't responded to the Visual Discovery Package). No `ProductSpec` in the CampaignContract (generic pack). The stage therefore runs as base Scene Assembly.

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
        "description": "A woman in her early thirties, casual home clothes (soft knit or tee), mid-savor just after a sip of a creamy smoothie — eyes softened or briefly closed, an unguarded half-smile, glass still raised near her lips. Her enjoyment is private, not performed to camera.",
        "roles": ["Identity-Bearing", "Structural"],
        "source": "Generated"
      },
      {
        "id": "entity_02",
        "description": "A glass of thick, creamy smoothie — pale oat-vanilla tone with a faint berry swirl, visible texture and body (clearly blended real food, not thin milk).",
        "roles": ["Symbolic", "Structural"],
        "source": "Generated"
      },
      {
        "id": "entity_03",
        "description": "The protein powder pack — a matte kraft-paper pouch, open, with a clean minimal label free of legible text; a wooden or steel scoop of powder resting beside or in it.",
        "roles": ["Brand-Bearing", "Symbolic"],
        "source": "Generated"
      },
      {
        "id": "entity_04",
        "description": "Natural ingredients in just-used disarray on the counter: a peeled banana, a scatter of rolled oats, a few fresh berries, a split vanilla pod — recognizable real foods, casually placed.",
        "roles": ["Symbolic", "Supporting"],
        "source": "Generated"
      },
      {
        "id": "entity_05",
        "description": "A lived-in home kitchen in morning light — wooden counter, a window out of focus behind, everyday kitchen objects at the edges.",
        "roles": ["Environmental"],
        "source": "Generated"
      }
    ],

    "Relationships": [
      { "subject": "entity_01", "relation": "holding", "object": "entity_02" },
      { "subject": "entity_03", "relation": "adjacent_to", "object": "entity_04" },
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
      "foreground": ["entity_02", "entity_04", "entity_03"],
      "midground": ["entity_01"],
      "background": ["entity_05"]
    },

    "RelativeScale": [
      { "entity_id": "entity_01", "reference_entity": "entity_05", "scale_relationship": "Subject occupies the dominant share of the frame at natural scale, close to the viewer at the counter." },
      { "entity_id": "entity_03", "reference_entity": "entity_04", "scale_relationship": "Pack sits at true pouch scale among the ingredients — present and identifiable, visually subordinate to the subject and glass." }
    ],

    "GenerationRequirements": {
      "required_entities": ["entity_01", "entity_02", "entity_03", "entity_04"],
      "required_supporting_objects": ["scoop with powder"],
      "required_environment_elements": ["wooden counter surface", "morning window light source"]
    },

    "PreservationContracts": [
      {
        "entity_id": "entity_01",
        "preservation_priority": "Critical",
        "recognizability_requirement": "Strong Match",
        "source": "Generated",
        "immutable_attributes": [
          "single subject (not a group)",
          "genuine, unperformed savoring expression — caught mid-moment, not posed to camera",
          "casual home clothing (no athletic wear)",
          "glass held at or near lips — the sip just happened"
        ],
        "flexible_attributes": [
          "exact age within 25–40, ethnicity, hair",
          "standing or leaning at the counter",
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
          "just-used casual placement — not a styled commercial flat-lay"
        ],
        "flexible_attributes": ["exact ingredient subset and count", "arrangement"]
      },
      {
        "entity_id": "entity_05",
        "preservation_priority": "Medium",
        "recognizability_requirement": "Loose Match",
        "source": "Generated",
        "immutable_attributes": ["lived-in home kitchen, morning daylight from a window"],
        "flexible_attributes": ["kitchen style and era", "background objects", "window position"]
      }
    ]
  }
}
```

> **Omitted by design:** `reference_locked_entities`, `ReferenceAssetManifest`, `client_preference_influence`, `ClientPreferenceConflicts` — no uploaded assets, no client preference contract in this run.

## Downstream Handoff

- Single human subject → Stage 6.1's Multi-Subject Pose Variation Requirement will not trigger (`pose_variation_required: false` expected); Human Subject Rendering Requirement (natural skin) WILL apply.
- entity_03's "no legible text" immutable must survive to the NEGATIVE block — fabricated label text is a known generator failure mode.

# Scene Contract — Nike Chill Run Club (Stage 5.2.5)

Framework: 5.2.5 Scene-Assembly.md
Inputs: ArtDirectionContract (Stage 4), CampaignContract.MandatoryRequirements.ProductSpec (Stage 1.1), ClientPreferenceContract (Stage 5.5)

**Reference Asset Extraction Block:** Skipped — no reference images were uploaded for this run. `ReferenceAssetManifest` is therefore omitted entirely.

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
        "description": "A small group (4-5) of diverse Gen Z Hong Kong professionals, mid-jog/walk along a harbourfront promenade, in a mix of remaining office-wear elements (e.g. a blazer slung over a shoulder, a work bag) and athletic gear — visibly transitioning from work mode to run mode.",
        "roles": ["Identity-Bearing"],
        "source": "Generated"
      },
      {
        "id": "entity_02",
        "description": "Nike Pegasus 41 running shoes worn by subjects in entity_01 — engineered mesh upper with Flywire cable overlays, thick React foam midsole with visible lateral crash rail, moderate heel stack with padded collar, lateral Swoosh in a contrasting tone.",
        "roles": ["Brand-Bearing", "Supporting"],
        "source": "Generated"
      },
      {
        "id": "entity_03",
        "description": "Hong Kong harbourfront promenade environment at night — waterfront walkway, railing, Victoria Harbour water, and the dense illuminated skyline of towers beyond.",
        "roles": ["Environmental"],
        "source": "Generated"
      }
    ],

    "Relationships": [
      { "subject": "entity_01", "relation": "located_within", "object": "entity_03" },
      { "subject": "entity_02", "relation": "worn_by", "object": "entity_01" },
      { "subject": "entity_01", "relation": "facing", "object": "entity_01" }
    ],

    "AnchorRelationships": [
      { "entity_id": "entity_01", "anchor_type": "floor_anchored" },
      { "entity_id": "entity_03", "anchor_type": "background_environment" }
    ],

    "DepthStructure": {
      "foreground": ["entity_01", "entity_02"],
      "midground": ["entity_01"],
      "background": ["entity_03"]
    },

    "RelativeScale": [
      { "entity_id": "entity_01", "reference_entity": "entity_03", "scale_relationship": "Subjects occupy a significant, human-scaled portion of the frame; the skyline reads as an expansive backdrop rather than the dominant subject." },
      { "entity_id": "entity_02", "reference_entity": "entity_01", "scale_relationship": "Shoes are scaled naturally to the wearing subject's body, with at least one pair legible in the lower frame." }
    ],

    "GenerationRequirements": {
      "required_entities": ["entity_01", "entity_02", "entity_03"],
      "required_supporting_objects": [
        "A blazer or jacket slung over a shoulder or tied at the waist (office-to-run transition cue)",
        "A small crossbody bag or backpack on one or two subjects",
        "Wireless earbuds on at least one subject"
      ],
      "required_environment_elements": [
        "Promenade railing along the waterfront",
        "Harbour water reflecting city lights",
        "Illuminated tower skyline in the background",
        "Warm-toned streetlights along the promenade"
      ]
    },

    "PreservationContracts": [
      {
        "entity_id": "entity_01",
        "preservation_priority": "Critical",
        "recognizability_requirement": "Strong Match",
        "source": "Generated",
        "immutable_attributes": [
          "Diversity of age, gender, and styling across the group (per BrandContract.Observations)",
          "Natural, candid expressions and mid-motion body language",
          "Visible office-to-run transition styling (partial work attire mixed with athletic wear)"
        ],
        "flexible_attributes": [
          "Exact poses and group arrangement",
          "Specific clothing colors and styles",
          "Exact framing (full body vs. partial)",
          "Lighting tone on subjects"
        ],
        "client_preference_influence": "ClientPreferenceContract selections (ref_A, ref_D) prefer warm ambient lighting and candid, mid-motion, group-friendship framing — these flexible lighting and framing decisions are resolved toward warm/candid rather than cool/posed."
      },
      {
        "entity_id": "entity_02",
        "preservation_priority": "Critical",
        "recognizability_requirement": "Near Exact",
        "source": "Generated",
        "immutable_attributes": [
          "Product model name: Nike Pegasus 41",
          "Thick React foam midsole with visible crash rail along the lateral edge",
          "Engineered mesh upper with Flywire cable overlays at midfoot",
          "Moderate heel stack with slight heel-to-toe drop and padded heel collar",
          "Lateral Swoosh in a contrasting tone on the mesh upper, standard proportions"
        ],
        "flexible_attributes": [
          "Lighting on the shoe surface",
          "Exact rotation / viewing angle",
          "Scale within frame",
          "Lace color",
          "Colorway (not mandated by CampaignContract)",
          "Degree of wear / newness"
        ],
        "client_preference_influence": null
      },
      {
        "entity_id": "entity_03",
        "preservation_priority": "High",
        "recognizability_requirement": "Approximate Match",
        "source": "Generated",
        "immutable_attributes": [
          "Hong Kong harbourfront identity — dense illuminated skyline silhouette beyond the water",
          "Waterfront promenade spatial structure (walkway, railing, water edge)"
        ],
        "flexible_attributes": [
          "Exact crop and framing of skyline",
          "Color temperature of ambient lighting",
          "Atmospheric density (haze, reflections)",
          "Presence of other pedestrians in background"
        ],
        "client_preference_influence": "ClientPreferenceContract favors warm amber ambient tones over cool/neon-dominant treatment, and explicitly flags avoidance of 'cold blue/neon-dominant lighting and overly vast, futuristic cityscape framing' (ref_B rejection) — color temperature and atmospheric density are resolved toward this warm, intimate reading."
      }
    ]
  }
}
```

**Notes:**
- No reference images were supplied, so the Reference Asset Extraction Block was skipped and `ReferenceAssetManifest` is omitted, per v5.2/v5.2.5 rules.
- `reference_locked_entities` is omitted from `GenerationRequirements` for the same reason.
- No `ClientPreferenceConflicts` were identified — the client's warm/intimate preference aligns with `BrandContract.RenderingStyle` (naturalistic realism, authentic atmosphere), so nothing is deferred to Synthesis.
- Both the Nike Pegasus 41 model name and its visual descriptor summary (entity_02 immutable attributes) are flagged to flow through Synthesis to the Prompt Compiler's `brand` key in HIGH, per downstream handoff rules.

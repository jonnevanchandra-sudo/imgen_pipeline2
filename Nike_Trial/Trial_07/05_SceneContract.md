# Scene Contract — Nike Chill Run Club (Stage 5.2.5)

Framework: `5.2.5 Scene-Assembly.md`
Inputs: ArtDirection (Stage 4) + CampaignContract.MandatoryRequirements (Stage 1.1, incl. ProductSpec)
Decision Type: Scene Construction — spatial blueprint and preservation contracts.

**Run mode:** No reference images were uploaded, so the **Reference Asset Extraction Block is SKIPPED** and **no `ReferenceAssetManifest` is produced**. No `ClientPreferenceContract` is available (Stage 5.5 not in this chain), so the stage runs **identically to v5.2** — no `client_preference_influence` and no `ClientPreferenceConflicts`. The CampaignContract **does** carry a `ProductSpec` (Nike Pegasus), so the shoe is locked as a named product-model entity (Near Exact) using its visual descriptors — name alone is unreliable for the generator.

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
        "description": "A small group of four-to-five diverse Hong Kong Gen Z professionals (early–late twenties, mixed gender and styling), mid-stride at a relaxed jogging pace, interacting with each other rather than the camera. Clothing blends office and run modes (a blazer slung over a shoulder or tied at the waist, rolled sleeves under a light running jacket, a crossbody work bag on one or two).",
        "roles": ["Identity-Bearing", "Structural"],
        "source": "Generated"
      },
      {
        "id": "entity_02",
        "description": "Nike Pegasus (latest generation) running shoes worn by at least one subject, visible in the lower frame mid-stride.",
        "roles": ["Brand-Bearing", "Symbolic"],
        "source": "Generated"
      },
      {
        "id": "entity_03",
        "description": "Hong Kong harbourfront promenade at night — a walkway with a railing alongside, the illuminated skyline visible across the water.",
        "roles": ["Environmental"],
        "source": "Generated"
      },
      {
        "id": "entity_04",
        "description": "Dense, warmly lit Hong Kong skyline across the harbour, serving as the distant city backdrop.",
        "roles": ["Environmental", "Supporting"],
        "source": "Generated"
      }
    ],

    "Relationships": [
      { "subject": "entity_01", "relation": "facing", "object": "entity_01" },
      { "subject": "entity_01", "relation": "moving_along", "object": "entity_03" },
      { "subject": "entity_02", "relation": "worn_by", "object": "entity_01" },
      { "subject": "entity_04", "relation": "visible_behind", "object": "entity_01" },
      { "subject": "entity_03", "relation": "adjacent_to", "object": "entity_01" }
    ],

    "AnchorRelationships": [
      { "entity_id": "entity_01", "anchor_type": "floor_anchored" },
      { "entity_id": "entity_02", "anchor_type": "floor_anchored" },
      { "entity_id": "entity_03", "anchor_type": "floor_anchored" },
      { "entity_id": "entity_04", "anchor_type": "horizon_anchored" }
    ],

    "DepthStructure": {
      "foreground": ["entity_01", "entity_02"],
      "midground": ["entity_03"],
      "background": ["entity_04"]
    },

    "RelativeScale": [
      { "entity_id": "entity_01", "reference_entity": "entity_03", "scale_relationship": "Group occupies the dominant share of the frame at natural human scale, standing on the promenade." },
      { "entity_id": "entity_02", "reference_entity": "entity_01", "scale_relationship": "Shoes are true-to-life relative to the wearers; readable but small within the lower frame — secondary to faces." },
      { "entity_id": "entity_04", "reference_entity": "entity_01", "scale_relationship": "Skyline reads as a wide, distant backdrop — visually smaller and set well behind the group." }
    ],

    "GenerationRequirements": {
      "required_entities": ["entity_01", "entity_03"],
      "required_supporting_objects": ["promenade railing", "Nike Pegasus running shoes (entity_02)"],
      "required_environment_elements": ["illuminated HK skyline across water", "night promenade surface", "harbour water"]
    },

    "PreservationContracts": [
      {
        "entity_id": "entity_01",
        "preservation_priority": "Critical",
        "recognizability_requirement": "Strong Match",
        "source": "Generated",
        "immutable_attributes": [
          "group of 4–5 people (not a solo runner)",
          "visibly diverse HK Gen Z professionals, mixed gender",
          "candid peer interaction with each other, not posed to camera",
          "office-to-run hybrid styling",
          "relaxed jogging pace, loose non-competitive body language"
        ],
        "flexible_attributes": [
          "exact number within 4–5",
          "individual poses and expressions",
          "specific garments and colors",
          "exact spacing within the group"
        ]
      },
      {
        "entity_id": "entity_02",
        "preservation_priority": "Critical",
        "recognizability_requirement": "Near Exact",
        "source": "Generated",
        "named_product_model": true,
        "immutable_attributes": [
          "product model name: Nike Pegasus (latest generation, e.g. Pegasus 41)",
          "engineered mesh upper with visible Flywire cable overlays at the midfoot",
          "thick responsive foam midsole with a visible crash rail along the lateral edge",
          "moderately stacked heel with a padded heel collar and slight heel-to-toe drop",
          "lateral Swoosh in a contrasting tone, standard proportions, legible at medium camera distance"
        ],
        "flexible_attributes": [
          "lighting on the shoe surface",
          "exact rotation / viewing angle (mid-stride)",
          "scale within lower frame",
          "lace color (colorway not mandated)",
          "slight degree of natural wear (lifestyle, not box-fresh)"
        ]
      },
      {
        "entity_id": "entity_03",
        "preservation_priority": "High",
        "recognizability_requirement": "Approximate Match",
        "source": "Generated",
        "immutable_attributes": [
          "Hong Kong harbourfront promenade at night",
          "walkway with railing alongside",
          "water and city present"
        ],
        "flexible_attributes": [
          "exact stretch of promenade",
          "railing style",
          "crop and expansion",
          "supporting street furniture"
        ]
      },
      {
        "entity_id": "entity_04",
        "preservation_priority": "Medium",
        "recognizability_requirement": "Loose Match",
        "source": "Generated",
        "immutable_attributes": [
          "dense illuminated city skyline across water",
          "reads as Hong Kong"
        ],
        "flexible_attributes": [
          "exact building arrangement",
          "degree of background blur",
          "light density and color of windows"
        ]
      }
    ]
  }
}
```

> **Omitted by design:** `reference_locked_entities`, `ReferenceAssetManifest`, `client_preference_influence`, and `ClientPreferenceConflicts` are all absent — there are no uploaded reference assets and no client preference contract in this run.

---

## Physical & Preservation Validation

- **Scale:** Group dominant in foreground, shoes true-to-life and subordinate, skyline distant — internally consistent (Realistic model). ✓
- **Perspective / anchoring:** Group and shoes floor-anchored on the promenade; skyline horizon-anchored across the water — no contradictions. ✓
- **Preservation:** Human group locked as Critical/Strong Match (no solo runner, peer interaction immutable); Pegasus locked Critical/Near Exact with **model name + visual descriptors together** so both reach the Prompt Compiler `brand` key in HIGH. ✓
- **Boundary:** No lighting aesthetics, camera, or composition styling decided here — only physical coherence and preservation. ✓

## Downstream Handoff

- Named product model (entity_02): both the **model name** and **visual descriptor summary** must travel through Synthesis and land in the Prompt Compiler's `brand` key (HIGH) — model name first, identifiers following.
- No reference-asset flow and no BRAND_ASSETS obligation downstream.

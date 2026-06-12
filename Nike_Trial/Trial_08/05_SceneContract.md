# Scene Contract — Nike Chill Run Club (Stage 5.2.5)

Framework: `5.2.5 Scene-Assembly.md` (canonical Stage 5)
Inputs: ArtDirectionContract (Stage 4) + CampaignContract `MandatoryRequirements.ProductSpec` (Stage 1.1)
Run note: No reference images were uploaded for this run, so the Reference Asset Extraction Block is skipped — `ReferenceAssetManifest` is omitted entirely. No `ClientPreferenceContract` is available (Stage 1.5/5.5 asynchronous client response not received), so this stage runs identically to v5.2. The named-product preservation path (from v5.1) IS active because CampaignContract contains a `ProductSpec` (Nike Pegasus). Of the two location options carried from Stage 1.1, **West Kowloon Cultural District / Art Park waterfront** is selected as the specific environment — it gives "The Mode Switch" concept an open, energetic plaza/promenade space with a Hong Kong Island skyline backdrop across the harbour, distinct from a dense harbourfront walkway.

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
        "description": "A group of four to five Hong Kong Gen Z professionals, diverse in gender and styling, caught mid-transition from 'office mode' to 'run mode' — moving energetically together, each still carrying one visible trace of the workday (e.g. a blazer draped over a shoulder, a loosened tie, a tote/work bag worn cross-body) layered with Nike running gear.",
        "roles": ["Identity-Bearing"],
        "source": "Generated"
      },
      {
        "id": "entity_02",
        "description": "Nike Pegasus running shoes (latest generation), worn by at least one subject in entity_01, visible mid-stride in the lower frame.",
        "roles": ["Brand-Bearing", "Product"],
        "source": "Generated"
      },
      {
        "id": "entity_03",
        "description": "An open waterfront promenade / plaza in the West Kowloon Cultural District (Art Park character) — wide paved walkway with harbour railing, night ambiance.",
        "roles": ["Environmental"],
        "source": "Generated"
      },
      {
        "id": "entity_04",
        "description": "The Hong Kong Island skyline at night, seen across the harbour — dense cluster of illuminated towers.",
        "roles": ["Environmental"],
        "source": "Generated"
      }
    ],

    "Relationships": [
      { "subject": "entity_01", "relation": "located_on", "object": "entity_03" },
      { "subject": "entity_02", "relation": "worn_by", "object": "entity_01" },
      { "subject": "entity_04", "relation": "visible_behind", "object": "entity_01" },
      { "subject": "entity_04", "relation": "visible_across", "object": "entity_03" }
    ],

    "AnchorRelationships": [
      { "entity_id": "entity_01", "anchor_type": "floor_anchored" },
      { "entity_id": "entity_03", "anchor_type": "ground_plane" },
      { "entity_id": "entity_04", "anchor_type": "horizon_anchored" }
    ],

    "DepthStructure": {
      "foreground": ["entity_01", "entity_02"],
      "midground": ["entity_03"],
      "background": ["entity_04"]
    },

    "RelativeScale": [
      { "entity_id": "entity_01", "reference_entity": "entity_03", "scale_relationship": "Human-scale figures occupying the near portion of an open promenade/plaza; the plaza reads as wide enough to suggest a real public waterfront space, not a tight corridor." },
      { "entity_id": "entity_04", "reference_entity": "entity_01", "scale_relationship": "The skyline sits at true cross-harbour distance — towers read small relative to the group, consistent with the width of Victoria Harbour; it forms a backdrop band, not a nearby structure." }
    ],

    "GenerationRequirements": {
      "required_entities": ["entity_01", "entity_02", "entity_03", "entity_04"],
      "required_supporting_objects": ["harbour-side railing", "promenade paving", "ambient night lighting (lampposts/path lights)"],
      "required_environment_elements": ["West Kowloon waterfront promenade/plaza", "Hong Kong Island skyline across the harbour"]
    },

    "PreservationContracts": [
      {
        "entity_id": "entity_01",
        "preservation_priority": "Critical",
        "recognizability_requirement": "Strong Match",
        "source": "Generated",
        "immutable_attributes": [
          "group of 4-5 people, diverse in gender, ethnicity, and personal styling",
          "each subject visibly carries at least one 'office mode' trace (draped blazer/jacket, loosened tie/collar, rolled sleeves, or a slung tote/work bag)",
          "each subject also wears Nike running gear / activewear, layered with the office trace",
          "body language reads as energized and in-motion, not posed or static",
          "all subjects engaged with each other or the moment, never posed toward camera"
        ],
        "flexible_attributes": [
          "exact poses, stride phase, and gestures per subject",
          "individual clothing colors and styling details",
          "exact facial expressions",
          "exact spacing/arrangement within the group"
        ],
        "client_preference_influence": null
      },
      {
        "entity_id": "entity_02",
        "preservation_priority": "Critical",
        "recognizability_requirement": "Near Exact",
        "source": "Generated",
        "immutable_attributes": [
          "product model name: Nike Pegasus (latest generation, e.g. Pegasus 41)",
          "engineered mesh upper with visible Flywire cable overlays at the midfoot",
          "thick responsive foam midsole with a visible crash rail along the lateral edge",
          "moderately stacked heel with a padded heel collar and slight heel-to-toe drop",
          "lateral Swoosh in a contrasting tone, standard proportions, legible at medium camera distance"
        ],
        "flexible_attributes": [
          "lighting on the shoe surface",
          "exact rotation / viewing angle",
          "scale within frame",
          "lace color",
          "degree of wear / newness (worn-in preferred per visibility_notes)"
        ],
        "client_preference_influence": null
      },
      {
        "entity_id": "entity_03",
        "preservation_priority": "High",
        "recognizability_requirement": "Approximate Match",
        "source": "Generated",
        "immutable_attributes": [
          "open waterfront promenade/plaza character (West Kowloon Art Park type space)",
          "harbour-facing orientation with a railing or edge toward the water",
          "night-time ambiance with ambient path/lamp lighting"
        ],
        "flexible_attributes": [
          "crop and framing",
          "exact paving pattern, planting, and street furniture",
          "presence of incidental background pedestrians"
        ],
        "client_preference_influence": null
      },
      {
        "entity_id": "entity_04",
        "preservation_priority": "High",
        "recognizability_requirement": "Approximate Match",
        "source": "Generated",
        "immutable_attributes": [
          "dense cluster of illuminated high-rise towers, recognizable as a Hong Kong skyline",
          "positioned across open water (harbour) from the promenade",
          "night-time illumination"
        ],
        "flexible_attributes": [
          "exact building shapes and arrangement",
          "color temperature and intensity of skyline lights (subject to luminance hierarchy from Composition & Rendering)",
          "haze/atmospheric softness"
        ],
        "client_preference_influence": null
      }
    ]
  }
}
```

---

## Validation

- ✓ Reference Asset Extraction Block: **skipped** — no reference images uploaded.
- ✓ `ReferenceAssetManifest`: **omitted** — no reference assets present.
- ✓ Named product (Nike Pegasus) locked as `entity_02` with model name AND visual descriptors together (per v5.1 rule), Critical / Near Exact, flowing to Synthesis → Prompt Compiler `brand` key in HIGH.
- ✓ `ClientPreferenceContract`: not available — stage behaves identically to v5.2; no `ClientPreferenceConflicts`.
- ✓ Scale, perspective, and environmental relationships are internally consistent with a Realistic reality model and an open West Kowloon waterfront plaza facing the HK Island skyline.
- ✓ No unresolved spatial or environmental contradictions.
- ✓ Ready for Composition & Rendering.

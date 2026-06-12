# Scene Contract
**Brand:** Nike
**Campaign:** Nike Chill Run Club
**Framework:** Scene Assembly v5.2
**Stage:** 5 — Scene Construction

---

## Reference Asset Extraction Block

**Reference images provided:** 1 (user portrait — neutral expression, grey background, black tank top)
**Running Reference Asset Extraction Block before scene construction.**

---

### Step 1 — Read the image

Directly observed from the uploaded reference photo:

- Male subject, East Asian features, approximately late teens to mid-twenties
- Hair: short, dark black — natural texture, slightly tousled on top, closely cut on sides; no hard fade; natural growth pattern visible
- Facial structure: oval face with defined cheekbones and a squared, proportionate jaw; brow ridge is prominent and well-defined; overall structure is clean-cut and symmetrical
- Eyes: dark brown, double eyelid visible, direct gaze into lens — alert and composed
- Nose: straight, well-proportioned, slightly broad at bridge
- Lips: well-defined, mouth closed, neutral to slight downward set — not tense
- Skin: clear complexion, warm-to-neutral light undertone; no blemishes visible; natural pore texture
- Build: athletic — shoulder width and arm definition visible through black ribbed tank top; frame is lean and proportionate
- Expression: neutral and composed — not smiling, not frowning; a direct, steady quality
- Background: neutral grey (reference context only — does not carry into scene)
- Clothing in reference: black ribbed tank top (reference context only — subject will wear Nike running gear in scene)

### Step 2 — Classify the asset

**Identity-Bearing** — contains a specific individual whose facial identity, physical features, and build must be preserved in the scene. This is the primary identity reference for entity_01 in the scene.

### Step 3 — Assign IDs

- `asset_id`: asset_01
- `entity_id`: entity_01
- `prompt_reference_id`: reference_asset_01

### Step 4 — Extract immutable attributes (from direct observation)

- Gender: male
- Ethnicity: East Asian (HK/Korean-adjacent)
- Age appearance: late teens to mid-twenties
- Hair: short, dark black, natural texture, slightly tousled on top; closely cut sides
- Facial structure: defined cheekbones, squared proportionate jaw, prominent brow ridge, symmetrical features
- Eyes: dark brown, double eyelid, direct and composed gaze
- Nose: straight, slightly broad at bridge
- Skin: clear, warm-to-neutral light undertone
- Build: lean athletic — visible shoulder width and arm definition; proportionate frame
- Expression character: composed, direct, steady — not effusive, not tense

### Step 5 — Flexible attributes

- Specific clothing (will wear Nike running gear in scene)
- Expression in scene (will show present-state liberation appropriate to running context — not the neutral reference expression)
- Body orientation and pose (will be mid-stride running, not portrait stance)
- Lighting on face (adapts to golden hour outdoor conditions)
- Hair exact styling (may shift slightly with running motion)

### Step 6 — Generation rule

Source: Reference Asset
Generation rule: "Reproduce from reference_asset_01 — use the uploaded reference image for entity_01's facial identity, hair, and physical build. Do not generate from training data."

### Step 7 — ReferenceAssetManifest entry

```json
{
  "asset_id": "asset_01",
  "filename": "user_reference_portrait.jpg",
  "type": "Identity-Bearing",
  "prompt_reference_id": "reference_asset_01",
  "attach_to_api_call": true,
  "strictness": "Strong Match"
}
```

---

## Scene Construction

**Visual Concept received from Art Direction:** "In Stride" — two runners (Karina from aespa and the user) at Hong Kong harbor at golden hour, caught mid-stride in synchronized parallel motion. Nike Novablast 5 in Volt / Black / White visible mid-stride. Faces in present-state liberation — not performing for each other.

---

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
        "description": "The user — male subject from reference image. East Asian, late teens to mid-twenties, lean athletic build, short dark black hair, defined facial structure. Running mid-stride in Nike Chill Run Club context. Expression: present-state liberation — composed ease, no tension, face forward and slightly open. Wearing Nike running gear (shorts, light running top) with Nike Novablast 5 in Volt / Black / White on feet.",
        "roles": ["Identity-Bearing"],
        "source": "Reference Asset",
        "asset_id": "asset_01",
        "prompt_reference_id": "reference_asset_01"
      },
      {
        "id": "entity_02",
        "description": "Karina from aespa — female, Korean, approximately 24–26 years old. Known visual characteristics: sculpted facial structure with defined jaw and high cheekbones; large, dark eyes with a clean, precise aesthetic; slim, tall build; dark hair (short to medium length, sleek). Running mid-stride parallel to entity_01, at the same pace and rhythm. Expression: present-state liberation — the specific ease of a face that has stopped processing and is only moving. Wearing Nike running gear with Nike Novablast 5 in Volt / Black / White on feet.",
        "roles": ["Identity-Bearing"],
        "source": "Generated",
        "named_subject": "Karina (from aespa)",
        "named_subject_note": "Named public figure — generation relies on model's training knowledge of this subject's likeness. Visual descriptors provided as fallback."
      },
      {
        "id": "entity_03",
        "description": "Nike Novablast 5 in Volt / Black / White colorway — worn by both entity_01 and entity_02 on their feet mid-stride. The distinctive ZOOMX foam midsole profile (rounded, high-stack, convex bottom) is the shoe's visual identity. Volt Swoosh on lateral side of black engineered mesh upper. Volt rubber outsole pods visible on white midsole base. At minimum one shoe must be in full profile mid-stride showing the complete ZOOMX midsole silhouette.",
        "roles": ["Supporting", "Symbolic", "Brand-Bearing"],
        "source": "Generated",
        "named_product": "Nike Novablast 5",
        "product_spec_ref": "CampaignContract.MandatoryRequirements.ProductSpec[0]"
      },
      {
        "id": "entity_04",
        "description": "Hong Kong waterfront / harbor-adjacent outdoor environment at golden hour — late afternoon, approximately 60–90 minutes before sunset. Warm directional light from a low sun angle. Running path with natural outdoor surface. HK harbor or urban waterfront visible in background — skyline, water, architectural silhouette in warm atmospheric haze. Environment reads as unmistakably Hong Kong without requiring specific landmark identification.",
        "roles": ["Environmental"],
        "source": "Generated"
      }
    ],

    "Relationships": [
      { "subject": "entity_01", "relation": "running_parallel_to", "object": "entity_02" },
      { "subject": "entity_02", "relation": "running_parallel_to", "object": "entity_01" },
      { "subject": "entity_01", "relation": "facing_same_direction_as", "object": "entity_02" },
      { "subject": "entity_03", "relation": "worn_by", "object": "entity_01" },
      { "subject": "entity_03", "relation": "worn_by", "object": "entity_02" },
      { "subject": "entity_04", "relation": "surrounds", "object": "entity_01" },
      { "subject": "entity_04", "relation": "surrounds", "object": "entity_02" },
      { "subject": "entity_04", "relation": "visible_behind", "object": "entity_01" },
      { "subject": "entity_04", "relation": "visible_behind", "object": "entity_02" }
    ],

    "AnchorRelationships": [
      { "entity_id": "entity_01", "anchor_type": "ground_anchored_mid_stride — one foot in contact or near contact with path surface, one foot raised in stride extension" },
      { "entity_id": "entity_02", "anchor_type": "ground_anchored_mid_stride — one foot in contact or near contact with path surface, one foot raised in stride extension" },
      { "entity_id": "entity_03", "anchor_type": "attached_to_subjects — shoe is extension of subject's foot in motion, not a separate prop" },
      { "entity_id": "entity_04", "anchor_type": "ambient_environment — spatially fixed, extends in all directions beyond the frame" }
    ],

    "DepthStructure": {
      "foreground": ["entity_01", "entity_02", "entity_03"],
      "midground": ["entity_04 — running path surface extending behind subjects"],
      "background": ["entity_04 — HK harbor, skyline, atmospheric warm haze at golden hour"]
    },

    "RelativeScale": [
      { "entity_id": "entity_01", "reference_entity": "entity_02", "scale_relationship": "similar — both adult subjects, comparable height; Karina is slightly taller frame" },
      { "entity_id": "entity_03", "reference_entity": "entity_01", "scale_relationship": "proportionate to foot — shoe is attached to subject, scales with body" },
      { "entity_id": "entity_04", "reference_entity": "entity_01", "scale_relationship": "city-scale — harbor and skyline extend far beyond the subjects, environment is vast relative to subject scale" }
    ],

    "GenerationRequirements": {
      "required_entities": [
        "entity_01 — user (male subject from reference image) mid-stride running",
        "entity_02 — Karina from aespa mid-stride running parallel to entity_01"
      ],
      "required_supporting_objects": [
        "entity_03 — Nike Novablast 5 in Volt / Black / White on both subjects' feet, at least one shoe in full ZOOMX midsole profile mid-stride"
      ],
      "required_environment_elements": [
        "entity_04 — Hong Kong waterfront outdoor environment at golden hour; running path surface visible underfoot; HK harbor/skyline in background"
      ],
      "reference_locked_entities": [
        {
          "entity_id": "entity_01",
          "asset_id": "asset_01",
          "prompt_reference_id": "reference_asset_01",
          "rule": "Reproduce entity_01's face and physical build from reference image. Do not generate from training data."
        }
      ]
    },

    "PreservationContracts": [
      {
        "entity_id": "entity_01",
        "preservation_priority": "Critical",
        "recognizability_requirement": "Strong Match",
        "source": "Reference Asset",
        "asset_id": "asset_01",
        "prompt_reference_id": "reference_asset_01",
        "immutable_attributes": [
          "gender: male",
          "ethnicity: East Asian (HK/Korean-adjacent features)",
          "age appearance: late teens to mid-twenties",
          "hair: short dark black, natural texture, slightly tousled on top, close-cut sides",
          "facial structure: defined cheekbones, proportionate squared jaw, prominent brow ridge, symmetrical features",
          "eyes: dark brown, double eyelid, composed and direct quality",
          "skin: clear, warm-to-neutral light undertone",
          "build: lean athletic — visible shoulder width and arm definition, proportionate frame"
        ],
        "flexible_attributes": [
          "expression in scene — will show present-state liberation ease, not the neutral reference expression",
          "body orientation — mid-stride running posture, not portrait stance",
          "clothing — Nike running gear appropriate to scene context",
          "lighting on face — adapts to outdoor golden hour conditions",
          "exact hair positioning — may shift slightly with running motion"
        ],
        "generation_rule": "Use reference_asset_01 for facial identity and build — do not generate from training data"
      },
      {
        "entity_id": "entity_02",
        "preservation_priority": "Critical",
        "recognizability_requirement": "Strong Match",
        "source": "Generated",
        "named_subject": "Karina (from aespa)",
        "immutable_attributes": [
          "gender: female",
          "nationality/ethnicity: Korean",
          "age: approximately 24–26",
          "facial structure: sculpted, defined jaw, prominent high cheekbones, precise symmetry",
          "eyes: large, dark, double eyelid — clean and alert expression quality",
          "build: slim, tall, proportionate — model-adjacent frame",
          "hair: dark (black or very dark brown), sleek — short to medium length",
          "overall aesthetic: clean, precise, girl-crush visual energy without performance intensity"
        ],
        "flexible_attributes": [
          "expression in scene — will show present-state liberation ease appropriate to running context",
          "exact hairstyle styling",
          "clothing — Nike running gear",
          "lighting on face — adapts to golden hour outdoor conditions",
          "exact body orientation — mid-stride running"
        ]
      },
      {
        "entity_id": "entity_03",
        "preservation_priority": "Critical",
        "recognizability_requirement": "Near Exact",
        "source": "Generated",
        "named_product": "Nike Novablast 5",
        "immutable_attributes": [
          "product model name: Nike Novablast 5",
          "sole profile: thick ZOOMX foam midsole with a rounded, convex bottom profile — the midsole is the dominant visual element; bottom curves noticeably rather than sitting flat; scattered black rubber outsole pods on white midsole base; midsole sidewall shows horizontal layered texture",
          "upper construction: lightweight black engineered mesh upper — thin, semi-translucent, minimal overlays; sock-like construction at heel collar",
          "silhouette: high heel stack, pronounced rocker profile from side view; midsole appears wider than upper at forefoot creating visible platform effect",
          "brand mark: Volt (electric yellow-green) Nike Swoosh on lateral side — standard curved proportions, mid-foot placement, contrasting against black upper",
          "colorway: Volt / Black / White — black upper, white ZOOMX midsole, Volt Swoosh and Volt rubber outsole pods"
        ],
        "flexible_attributes": [
          "exact rotation and viewing angle",
          "lighting reflection on midsole surface",
          "scale relative to frame",
          "degree of wear"
        ]
      },
      {
        "entity_id": "entity_04",
        "preservation_priority": "Medium",
        "recognizability_requirement": "Approximate Match",
        "source": "Generated",
        "immutable_attributes": [
          "location: Hong Kong — unmistakably HK waterfront or harbor-adjacent outdoor environment",
          "time: golden hour — late afternoon, approximately 60–90 minutes before sunset; warm directional light at low sun angle",
          "path surface: outdoor running path with natural surface — not treadmill, not indoor track",
          "background: HK harbor or urban waterfront visible — water, skyline, or architectural silhouette in warm atmospheric haze"
        ],
        "flexible_attributes": [
          "specific landmark or location within HK",
          "exact sky coloration",
          "extent of water or skyline visible",
          "path surface material detail",
          "amount of architectural detail in background"
        ]
      }
    ]
  },

  "ReferenceAssetManifest": [
    {
      "asset_id": "asset_01",
      "filename": "user_reference_portrait.jpg",
      "type": "Identity-Bearing",
      "prompt_reference_id": "reference_asset_01",
      "attach_to_api_call": true,
      "strictness": "Strong Match"
    }
  ]
}
```

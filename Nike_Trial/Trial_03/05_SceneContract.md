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
- Hair: short, dark black — natural texture, slightly tousled on top, closely cut on sides; natural growth pattern visible; no hard geometric fade
- Facial structure: oval face with defined cheekbones and a squared, proportionate jaw; brow ridge prominent and well-defined; overall structure is symmetrical and clean-cut
- Eyes: dark brown, double eyelid visible, direct composed gaze into lens — alert and steady
- Nose: straight, well-proportioned, slightly broad at bridge
- Lips: well-defined, mouth closed, neutral to slight downward set — not tense
- Skin: clear complexion, warm-to-neutral light undertone; no blemishes; natural pore texture
- Build: athletic — shoulder width and arm definition visible through black ribbed tank top; frame is lean and proportionate
- Expression: neutral and composed — not smiling, not frowning; direct, steady quality
- Background: neutral grey (reference context only — does not carry into scene)
- Clothing in reference: black ribbed tank top (reference context only — subject will wear Nike running gear in scene)

### Step 2 — Classify the asset

**Identity-Bearing** — contains a specific individual whose facial identity, physical features, and build must be preserved in the scene. Primary identity reference for entity_01.

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
- Eyes: dark brown, double eyelid, direct and composed quality
- Nose: straight, slightly broad at bridge
- Skin: clear, warm-to-neutral light undertone
- Build: lean athletic — visible shoulder width and arm definition; proportionate frame

### Step 5 — Flexible attributes

- Expression in scene (will show present-state liberation ease appropriate to running context)
- Body orientation and pose (will be mid-stride running, not portrait stance)
- Clothing (will wear Nike running gear appropriate to scene)
- Lighting on face (adapts to HK night outdoor conditions)
- Hair exact positioning (may shift slightly with running motion)

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

**Visual Concept received from Art Direction:** "夜跑主角 — Night Run Protagonist" — Two people running through Hong Kong at night. City lights glowing behind them. Faces carry the ease of a mental reset that is actively happening. Genuine social warmth between subjects — two people whose pace has matched, who are here together. The Nike Alphafly 3 visible in stride.

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
        "environmental_behavior": "realistic — night city lighting, ambient glow, no unnatural light sources"
      }
    },

    "Entities": [
      {
        "id": "entity_01",
        "description": "The user — male subject from reference image. East Asian, late teens to mid-twenties, lean athletic build, short dark black hair, defined facial structure. Running mid-stride in HK at night. Expression: present-state liberation ease — open, composed, the specific look of a mind that has stopped processing and a body that has taken over. Wearing Nike running gear (light running top and shorts) with Nike Alphafly 3 in University Red / Black / White on feet.",
        "roles": ["Identity-Bearing"],
        "source": "Reference Asset",
        "asset_id": "asset_01",
        "prompt_reference_id": "reference_asset_01"
      },
      {
        "id": "entity_02",
        "description": "Karina from aespa — running mid-stride alongside entity_01. Expression: the same present-state liberation ease — not performing for the camera, genuinely in the run. Wearing Nike running gear with Nike Alphafly 3 in University Red / Black / White on feet. Social energy between her and entity_01 is visible: they are here together.",
        "roles": ["Identity-Bearing"],
        "source": "Generated",
        "named_subject": "Karina (from aespa)",
        "named_subject_note": "Named public figure — generation relies on model's training knowledge of this subject's likeness. No text description of appearance provided — generator uses its own knowledge."
      },
      {
        "id": "entity_03",
        "description": "Nike Air Zoom Alphafly NEXT% 3 in University Red / Black / White — worn by both entity_01 and entity_02 on their feet mid-stride. Visual identity: extremely tall ZoomX foam midsole in white; two large circular Air Zoom pods visible through transparent forefoot outsole window (the shoe's most distinctive feature); thin red Flyknit upper; pronounced rocker toe geometry; Nike Swoosh on lateral side. At minimum one shoe in full lateral mid-stride profile showing the complete midsole stack and the two forefoot pod windows.",
        "roles": ["Supporting", "Brand-Bearing"],
        "source": "Generated",
        "named_product": "Nike Air Zoom Alphafly NEXT% 3",
        "product_spec_ref": "CampaignContract.MandatoryRequirements.ProductSpec[0]"
      },
      {
        "id": "entity_04",
        "description": "Hong Kong at night — harbourfront or city waterfront outdoor running path. Night city atmosphere: warm amber streetlamps, diffuse glow of the HK skyline, city lights reflected in or adjacent to the harbor water. The city is alive and glowing. Running path surface is real outdoor pavement. The background carries unmistakably HK night character without requiring a specific landmark.",
        "roles": ["Environmental"],
        "source": "Generated"
      }
    ],

    "Relationships": [
      { "subject": "entity_01", "relation": "running_alongside", "object": "entity_02" },
      { "subject": "entity_02", "relation": "running_alongside", "object": "entity_01" },
      { "subject": "entity_01", "relation": "socially_connected_to_in_run", "object": "entity_02" },
      { "subject": "entity_03", "relation": "worn_by", "object": "entity_01" },
      { "subject": "entity_03", "relation": "worn_by", "object": "entity_02" },
      { "subject": "entity_04", "relation": "surrounds_and_extends_behind", "object": "entity_01" },
      { "subject": "entity_04", "relation": "surrounds_and_extends_behind", "object": "entity_02" }
    ],

    "AnchorRelationships": [
      { "entity_id": "entity_01", "anchor_type": "ground_anchored_mid_stride — one foot at or near path surface, one foot raised in stride extension" },
      { "entity_id": "entity_02", "anchor_type": "ground_anchored_mid_stride — one foot at or near path surface, one foot raised in stride extension" },
      { "entity_id": "entity_03", "anchor_type": "attached_to_subjects — shoe is extension of subject foot in motion, not a separate prop" },
      { "entity_id": "entity_04", "anchor_type": "ambient_environment — spatially fixed, extends in all directions; city lights and atmospheric glow at night" }
    ],

    "DepthStructure": {
      "foreground": ["entity_01", "entity_02", "entity_03"],
      "midground": ["entity_04 — running path surface, nearest city elements behind subjects"],
      "background": ["entity_04 — HK harbor, skyline, city lights, atmospheric night glow"]
    },

    "RelativeScale": [
      { "entity_id": "entity_01", "reference_entity": "entity_02", "scale_relationship": "similar — both adult subjects; comparable height with natural variation" },
      { "entity_id": "entity_03", "reference_entity": "entity_01", "scale_relationship": "proportionate to foot — shoe scales with body, not enlarged" },
      { "entity_id": "entity_04", "reference_entity": "entity_01", "scale_relationship": "city-scale — HK skyline and harbor extend far beyond subject scale" }
    ],

    "GenerationRequirements": {
      "required_entities": [
        "entity_01 — user (male, reference image) mid-stride running at night",
        "entity_02 — Karina from aespa mid-stride running alongside entity_01"
      ],
      "required_supporting_objects": [
        "entity_03 — Nike Alphafly 3 University Red on both subjects' feet; at minimum one shoe in full lateral profile showing ZoomX midsole and Air Zoom pod windows"
      ],
      "required_environment_elements": [
        "entity_04 — HK night city environment; outdoor running path; harbor/skyline glow in background"
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
          "ethnicity: East Asian",
          "age appearance: late teens to mid-twenties",
          "hair: short dark black, natural texture, slightly tousled on top, close-cut sides",
          "facial structure: defined cheekbones, squared proportionate jaw, prominent brow ridge, symmetrical features",
          "eyes: dark brown, double eyelid, composed and direct quality",
          "skin: clear, warm-to-neutral light undertone",
          "build: lean athletic — visible shoulder width and arm definition"
        ],
        "flexible_attributes": [
          "expression — present-state liberation ease in running context, not neutral portrait expression",
          "body orientation — mid-stride running posture",
          "clothing — Nike running gear",
          "lighting — adapts to HK night outdoor conditions",
          "exact hair positioning — may shift with running motion"
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
          "identity: Karina from aespa — generator uses its own training knowledge of her likeness"
        ],
        "flexible_attributes": [
          "expression — present-state liberation ease in running context",
          "clothing — Nike running gear",
          "lighting — adapts to HK night outdoor conditions",
          "exact body orientation — mid-stride running"
        ]
      },
      {
        "entity_id": "entity_03",
        "preservation_priority": "Critical",
        "recognizability_requirement": "Near Exact",
        "source": "Generated",
        "named_product": "Nike Air Zoom Alphafly NEXT% 3",
        "immutable_attributes": [
          "product name: Nike Air Zoom Alphafly NEXT% 3",
          "sole profile: extremely tall ZoomX foam midsole in white; two large circular Air Zoom pods visible through transparent forefoot outsole window — pod windows are the most distinctive visual feature",
          "upper: thin minimal Flyknit in University Red — low bulk, form-fitting",
          "silhouette: high heel-to-forefoot stack; pronounced rocker toe geometry curving upward at the toe",
          "brand mark: Nike Swoosh on lateral side against red upper",
          "colorway: University Red upper, white ZoomX midsole, standard Swoosh"
        ],
        "flexible_attributes": [
          "exact rotation and viewing angle",
          "lighting reflection on midsole surface",
          "degree of wear"
        ]
      },
      {
        "entity_id": "entity_04",
        "preservation_priority": "Medium",
        "recognizability_requirement": "Approximate Match",
        "source": "Generated",
        "immutable_attributes": [
          "location: Hong Kong — harbourfront or city waterfront, unmistakably HK night character",
          "time: night — post-work evening; city lights active; never fully dark",
          "lighting character: warm amber streetlamps + diffuse blue-tinted skyline glow + city neon; the specific warm-cool mixture of HK at night",
          "path surface: outdoor running path — real pavement, not indoor or track"
        ],
        "flexible_attributes": [
          "specific HK landmark or location",
          "exact color balance of city lighting",
          "amount of harbor water visible",
          "degree of background bokeh"
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
      "strictness": "Strong Match",
      "usage_note": "Attach to GPT Image 2.0 API call as reference for entity_01's face and physical build. Generator reproduces his facial identity in the night running scene — he will be in Nike running gear and mid-stride, not in the black tank top of the reference portrait."
    }
  ]
}
```

# Scene Contract
**Brand:** GigaSports
**Campaign:** Gigasports Pickle Club Community
**Framework:** Scene Assembly v5.2
**Stage:** 5 — Scene Construction

---

## Reference Asset Extraction Block

**Reference images provided:** 1 (GigaSports logo — orange background, white wordmark)
**Running Reference Asset Extraction Block before scene construction.**

---

### Step 1 — Read the image

Directly observed from the uploaded reference image:

- White wordmark reading "GigaSports" set in a compressed, bold, italic sans-serif typeface — all one word, no space
- The letter "O" in "Sports" is replaced by a stylized globe icon: a circular form showing continental outlines (silhouette of landmasses visible within the circle), maintaining the same cap-height as surrounding letterforms
- Below the wordmark: "BE PROFESSIONAL" set in small, wide-tracked all-caps, centered beneath the wordmark, noticeably smaller than the wordmark text
- All elements are white
- Background is solid orange — this is not part of the logo; it is the reference image background and will not carry through to the scene

### Step 2 — Classify the asset

**Brand-Bearing** — contains the GigaSports wordmark and brand mark. Must be reproduced exactly; any variation (letterform, globe shape, tagline) constitutes a brand error.

### Step 3 — Assign IDs

- `asset_id`: asset_01
- `entity_id`: entity_05
- `prompt_reference_id`: reference_asset_01

### Step 4 — Extract immutable attributes (from direct observation)

- Wordmark text: "GigaSports" — single word, no hyphen, no space
- Typeface style: compressed, bold, italic sans-serif — weight is heavy, letterforms are condensed
- Globe icon: replaces the letter "O" in "Sports" — circular, same cap-height as surrounding letters, shows continental silhouette outlines within
- Tagline: "BE PROFESSIONAL" — small all-caps, wide-tracked, centered directly below wordmark
- Color of all elements: white (all logo components)
- Overall format: horizontal wordmark with inline icon

### Step 5 — Flexible attributes

- Background color: orange in reference image — not locked; logo will appear on a banner or wall surface within the venue scene
- Scale: adapts to scene composition and camera distance
- Placement: adapts to scene layout — wall-mounted or banner-hung in background
- Rendering depth: may be soft in bokeh but must remain legible

### Step 6 — Generation rule

Source: Reference Asset
Generation rule: "Reproduce from reference_asset_01 — do not generate from training data."

### Step 7 — ReferenceAssetManifest entry

```json
{
  "asset_id": "asset_01",
  "filename": "gigasports_logo.jpg",
  "type": "Brand-Bearing",
  "prompt_reference_id": "reference_asset_01",
  "attach_to_api_call": true,
  "strictness": "Exact"
}
```

---

## Scene Construction

**Visual Concept received from Art Direction:** "The Welcome" — the moment a newcomer is received into the community by established members. Human welcome gesture as the emotional center.

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
        "description": "The newcomer — one young HK professional, late 20s to early 30s, in the act of being received by the group. Expression registers the micro-moment of belonging arriving: slight surprise dissolving into warmth and relief. Holding a pickleball paddle loosely.",
        "roles": ["Identity-Bearing"],
        "source": "Generated"
      },
      {
        "id": "entity_02",
        "description": "Established community members — one or two young HK professionals of similar age to entity_01, extending a welcome gesture toward entity_01. High five, arm around shoulder, or direct warm eye contact with open expression. Paddles in their non-greeting hands or at their sides.",
        "roles": ["Identity-Bearing"],
        "source": "Generated"
      },
      {
        "id": "entity_03",
        "description": "Pickleball paddles — held by entity_01 and entity_02. Sport identity signal. Casual grip, not raised in playing position.",
        "roles": ["Supporting", "Symbolic"],
        "source": "Generated"
      },
      {
        "id": "entity_04",
        "description": "Indoor pickleball court — court surface with line markings, net visible in midground. Establishes venue context.",
        "roles": ["Environmental"],
        "source": "Generated"
      },
      {
        "id": "entity_05",
        "description": "GigaSports logo on a banner or wall surface — background element. White wordmark with globe-O icon and BE PROFESSIONAL tagline, reproduced from reference_asset_01.",
        "roles": ["Brand-Bearing"],
        "source": "Reference Asset",
        "asset_id": "asset_01",
        "prompt_reference_id": "reference_asset_01"
      }
    ],

    "Relationships": [
      { "subject": "entity_02", "relation": "facing", "object": "entity_01" },
      { "subject": "entity_02", "relation": "extending_welcome_toward", "object": "entity_01" },
      { "subject": "entity_01", "relation": "receiving_welcome_from", "object": "entity_02" },
      { "subject": "entity_03", "relation": "held_by", "object": "entity_01" },
      { "subject": "entity_03", "relation": "held_by", "object": "entity_02" },
      { "subject": "entity_04", "relation": "visible_behind", "object": "entity_01" },
      { "subject": "entity_05", "relation": "visible_behind", "object": "entity_01" },
      { "subject": "entity_05", "relation": "visible_behind", "object": "entity_02" }
    ],

    "AnchorRelationships": [
      { "entity_id": "entity_01", "anchor_type": "floor_anchored" },
      { "entity_id": "entity_02", "anchor_type": "floor_anchored" },
      { "entity_id": "entity_04", "anchor_type": "floor_surface" },
      { "entity_id": "entity_05", "anchor_type": "wall_anchored" }
    ],

    "DepthStructure": {
      "foreground": ["entity_01", "entity_02", "entity_03"],
      "midground": ["entity_04"],
      "background": ["entity_05"]
    },

    "RelativeScale": [
      { "entity_id": "entity_01", "reference_entity": "entity_02", "scale_relationship": "similar — comparable height and frame, neither dominant" },
      { "entity_id": "entity_04", "reference_entity": "entity_01", "scale_relationship": "larger in physical space but visually subordinate — background and midground" },
      { "entity_id": "entity_05", "reference_entity": "entity_01", "scale_relationship": "visible but not dominant — logo reads through bokeh at background distance" }
    ],

    "GenerationRequirements": {
      "required_entities": ["entity_01 — newcomer receiving welcome", "entity_02 — established member(s) extending welcome"],
      "required_supporting_objects": ["entity_03 — pickleball paddles held by all subjects"],
      "required_environment_elements": ["entity_04 — indoor pickleball court surface and net", "entity_05 — GigaSports logo on venue surface"],
      "reference_locked_entities": [
        {
          "entity_id": "entity_05",
          "asset_id": "asset_01",
          "prompt_reference_id": "reference_asset_01",
          "rule": "Reproduce from reference image. Do not generate from training data."
        }
      ]
    },

    "PreservationContracts": [
      {
        "entity_id": "entity_01",
        "preservation_priority": "Critical",
        "recognizability_requirement": "Strong Match",
        "source": "Generated",
        "immutable_attributes": [
          "age range: late 20s to early 30s",
          "ethnicity: East Asian / Hong Kong context",
          "expression: micro-moment of belonging arriving — surprise dissolving into warmth and relief",
          "body orientation: facing entity_02, receiving the welcome gesture"
        ],
        "flexible_attributes": [
          "specific clothing",
          "exact hairstyle",
          "precise posture beyond orientation",
          "lighting on face"
        ]
      },
      {
        "entity_id": "entity_02",
        "preservation_priority": "Critical",
        "recognizability_requirement": "Strong Match",
        "source": "Generated",
        "immutable_attributes": [
          "age range: late 20s to early 30s",
          "ethnicity: East Asian / Hong Kong context",
          "expression: open, genuinely warm — actively welcoming, not performing for camera",
          "gesture: welcome action directed at entity_01 — high five, arm gesture, or direct warm eye contact",
          "body orientation: facing entity_01"
        ],
        "flexible_attributes": [
          "specific clothing",
          "exact hairstyle",
          "precise form of welcome gesture within the specified gesture types",
          "lighting on face"
        ]
      },
      {
        "entity_id": "entity_03",
        "preservation_priority": "Medium",
        "recognizability_requirement": "Approximate Match",
        "source": "Generated",
        "immutable_attributes": [
          "object type: pickleball paddle — correct paddle shape, not tennis racket or badminton racket",
          "grip: relaxed — held at side or in non-greeting hand, not raised in playing position"
        ],
        "flexible_attributes": [
          "specific paddle brand or color",
          "exact grip position",
          "scale relative to frame"
        ]
      },
      {
        "entity_id": "entity_04",
        "preservation_priority": "Medium",
        "recognizability_requirement": "Approximate Match",
        "source": "Generated",
        "immutable_attributes": [
          "venue type: indoor pickleball court",
          "court elements: line markings on floor surface, net visible in midground"
        ],
        "flexible_attributes": [
          "specific court color",
          "ceiling detail",
          "ambient lighting treatment",
          "extent of court visible in frame"
        ]
      },
      {
        "entity_id": "entity_05",
        "preservation_priority": "High",
        "recognizability_requirement": "Exact Match",
        "source": "Reference Asset",
        "asset_id": "asset_01",
        "prompt_reference_id": "reference_asset_01",
        "immutable_attributes": [
          "wordmark text: GigaSports — compressed bold italic sans-serif, single word",
          "globe icon: replaces the O in Sports — circular, continental silhouette outlines, same cap-height as letterforms",
          "tagline: BE PROFESSIONAL — small all-caps, wide-tracked, centered below wordmark",
          "color: all elements white",
          "format: horizontal wordmark with inline icon"
        ],
        "flexible_attributes": [
          "background surface color (appears on venue wall or banner, not original orange background)",
          "scale within scene",
          "exact placement on wall or banner",
          "rendering depth (may be soft in bokeh but must remain legible)"
        ],
        "generation_rule": "Use reference_asset_01 — do not generate from training data"
      }
    ]
  },

  "ReferenceAssetManifest": [
    {
      "asset_id": "asset_01",
      "filename": "gigasports_logo.jpg",
      "type": "Brand-Bearing",
      "prompt_reference_id": "reference_asset_01",
      "attach_to_api_call": true,
      "strictness": "Exact"
    }
  ]
}
```

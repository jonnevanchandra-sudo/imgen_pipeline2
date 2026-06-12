# Scene Contract
**Brand:** Nike
**Campaign:** Nike Chill Run Club
**Framework:** Scene Assembly Framework v5.0
**Stage:** 5 — Scene Construction

---

## Generation Mode

**Full Generation** — all entities generated from campaign context
Reference image (00_ImageAnalysisContract) is Style/Composition Reference only. No entities are locked from reference assets.

---

## Inputs Consumed

**From Art Direction:**
- VisualIntent: Effortless Social Vitality
- VisualConcept: The Reclaimed Evening — social moment that happens to involve running
- SubjectRelationshipLogic: Belonging + Equality — viewer could step into this group
- FocalPriority: Social dynamic between subjects first; HK environment second; Nike branding third

**From Image Analysis (Composition Reference):**
- Group running formation: 3–4 subjects in a loose cluster running together
- Framing: Full body visible — medium to wide shot including legs and feet in motion
- Camera axis: Eye-level, facing toward approaching group
- Social dynamic: Subjects aware of each other, not posed for camera

**From Campaign Contract:**
- Instagram 4:5 vertical format (1080 x 1350px)
- Safe zones: Top 10% and bottom 20% reserved for post-production copy overlay
- Required: Nike branding on apparel; HK outdoor environment; Gen Z HK Asian subjects

---

## Reality Model

```json
{
  "RealityModel": {
    "type": "Realistic",
    "coherence_rules": {
      "scale": "realistic — human subjects at natural scale relative to environment",
      "perspective": "realistic — no distortion; eye-level camera consistent with natural photography",
      "anchoring": "required — all subjects floor-anchored; no floating or suspended subjects",
      "environmental_behavior": "realistic — Hong Kong evening outdoor environment with natural evening light behavior"
    }
  }
}
```

---

## Entities

```json
{
  "Entities": [
    {
      "id": "entity_01",
      "label": "Subject group — HK Gen Z running peers",
      "roles": ["Identity-Bearing", "Brand-Bearing"],
      "source": "Generated",
      "description": "Group of 3–4 young Hong Kong Gen Z adults, mixed gender, approximately aged 22–28, East Asian ethnicity. Wearing Nike running apparel (at least one subject has visible Nike Swoosh on clothing). Running together as a social group at a comfortable, conversational pace. Subjects are physically close to each other, in loose formation — not a structured lineup. At least two subjects visibly aware of each other — mid-interaction, mid-conversation, or sharing a moment. No subject is posed for the camera."
    },
    {
      "id": "entity_02",
      "label": "Nike running shoes",
      "roles": ["Brand-Bearing", "Supporting"],
      "source": "Generated",
      "description": "Nike running shoes on the feet of subjects. Visible as subjects run — feet and shoes in motion. Nike branding (Swoosh) visible on shoes. Color is flexible to match apparel. Shoes must read as running shoes — not lifestyle sneakers or cross-trainers."
    },
    {
      "id": "entity_03",
      "label": "Nike apparel brand element",
      "roles": ["Brand-Bearing", "Supporting"],
      "source": "Generated",
      "description": "Nike Swoosh or minimal Nike branding visible on at least one subject's clothing. Could be a t-shirt, tank top, or jacket. The brand mark must be visible but not dominant — it reads as part of the subject's outfit, not a product placement foreground. Color and style adapted to match the social, casual athletic register of the campaign."
    },
    {
      "id": "entity_04",
      "label": "Hong Kong evening outdoor environment",
      "roles": ["Environmental", "Structural"],
      "source": "Generated",
      "description": "Hong Kong outdoor evening environment consistent with the campaign setting. Options: Victoria Harbour waterfront path, West Kowloon Cultural District promenade, or an urban park path with HK city skyline visible. Time: evening — blue hour or early night with city lights beginning to emerge. The environment is recognizably Hong Kong — not a generic park or running track. Warm ambient city light and evening atmosphere. The path or ground is visible underfoot where subjects run."
    }
  ]
}
```

---

## Relationships

```json
{
  "Relationships": [
    {
      "subject": "entity_01",
      "relation": "facing_each_other",
      "object": "entity_01",
      "notes": "At least two subjects within the group are oriented toward each other — their bodies and glances directed inward toward the group, not outward toward the camera. They are running together, not running separately in the same direction."
    },
    {
      "subject": "entity_01",
      "relation": "running_toward",
      "object": "camera",
      "notes": "The group collectively moves toward the camera. Camera is positioned in front of and at the same height as the subjects — they are approaching the viewer's position."
    },
    {
      "subject": "entity_01",
      "relation": "wearing",
      "object": "entity_02",
      "notes": "Nike shoes are on the subjects' feet — attached, not separate props."
    },
    {
      "subject": "entity_01",
      "relation": "wearing",
      "object": "entity_03",
      "notes": "Nike apparel is worn on subject body — attached, part of their outfit."
    },
    {
      "subject": "entity_01",
      "relation": "foreground_of",
      "object": "entity_04",
      "notes": "Subject group occupies the foreground plane. HK environment is the background behind and beyond the subjects."
    },
    {
      "subject": "entity_04",
      "relation": "visible_behind",
      "object": "entity_01",
      "notes": "HK cityscape, waterfront, or urban park environment is visible over and behind the subject group — establishing location context without competing with subjects for attention."
    }
  ]
}
```

---

## AnchorRelationships

```json
{
  "AnchorRelationships": [
    {
      "entity_id": "entity_01",
      "anchor_type": "floor_anchored",
      "notes": "All subjects are floor-anchored — feet contact or are clearly grounded relative to the path surface. Mid-stride motion is acceptable — one foot raised in running gait is correct — but subjects must not appear to float or be disconnected from the ground plane."
    },
    {
      "entity_id": "entity_02",
      "anchor_type": "attached_to_entity",
      "target_entity": "entity_01",
      "notes": "Running shoes are attached to subjects' feet — they are part of the subjects, not separate objects."
    },
    {
      "entity_id": "entity_03",
      "anchor_type": "attached_to_entity",
      "target_entity": "entity_01",
      "notes": "Nike apparel is worn by a subject — it moves with the subject's body."
    },
    {
      "entity_id": "entity_04",
      "anchor_type": "environmental",
      "notes": "HK outdoor environment is a fixed spatial container — the ground, path, and background cityscape are anchored to their natural positions. The environment surrounds and extends beyond the subjects."
    }
  ]
}
```

---

## DepthStructure

```json
{
  "DepthStructure": {
    "foreground": [
      "entity_01 — subject group: the 3–4 running subjects. They occupy the primary visual weight of the frame. Faces are readable. Social dynamic between subjects is visible. Feet and running shoes (entity_02) visible in lower foreground as subjects run toward camera.",
      "entity_03 — Nike apparel branding: attached to subjects, visible in the foreground layer as part of subjects' clothing"
    ],
    "midground": [
      "The running path or ground surface extending behind the subjects — provides spatial grounding and confirms the outdoor running context. Texture of the path surface is visible."
    ],
    "background": [
      "entity_04 — Hong Kong evening environment: the city skyline, waterfront, or park with HK urban context visible. This layer is soft in rendering — recognizable as Hong Kong but not competing with the subjects for attention. City lights, evening sky, and architectural silhouettes establish the location."
    ]
  }
}
```

---

## RelativeScale

```json
{
  "RelativeScale": [
    {
      "entity_id": "entity_01",
      "reference": "frame height",
      "scale_relationship": "Subjects should occupy approximately 65–80% of the vertical frame height. This keeps faces readable and social dynamic legible while leaving room for the HK environment to be visible above them. The 4:5 format requires subjects to dominate — this is not a wide landscape shot with people in the distance."
    },
    {
      "entity_id": "entity_02",
      "reference": "entity_01",
      "scale_relationship": "Running shoes are at realistic human proportions relative to subjects — feet and shoes visible at the lower portion of the frame as part of subjects' running bodies."
    },
    {
      "entity_id": "entity_03",
      "reference": "entity_01",
      "scale_relationship": "Nike apparel branding at natural clothing scale — the Swoosh or brand mark is visible at the size it would appear on an actual garment at medium camera distance."
    },
    {
      "entity_id": "entity_04",
      "reference": "entity_01",
      "scale_relationship": "HK environment at environmental scale — the city is large and extends beyond the frame in all directions. Subjects are human-scale figures within the city context. The environment is the world these subjects inhabit; it is not a small backdrop."
    }
  ]
}
```

---

## GenerationRequirements

```json
{
  "GenerationRequirements": {
    "required_entities": [
      "entity_01 — subject group of 3–4 HK Gen Z young adults running together",
      "entity_04 — Hong Kong evening outdoor environment"
    ],
    "required_supporting_objects": [
      "entity_02 — Nike running shoes on subjects (minimum: visible on at least two subjects)",
      "entity_03 — Nike brand mark on at least one subject's clothing"
    ],
    "required_environment_elements": [
      "Outdoor running path or surface — ground visible underfoot",
      "Hong Kong cityscape, waterfront, or urban park environment visible in background",
      "Evening atmosphere — blue hour, city lights emerging, warm ambient glow from city"
    ],
    "format_requirements": [
      "4:5 vertical aspect ratio (1080 x 1350px)",
      "Top 10% of frame: clear of faces, brand elements, and critical visual information — reserved for Cantonese copy overlay",
      "Bottom 20% of frame: clear of faces, brand elements, and critical visual information — reserved for Nike Chill Run Club CTA overlay"
    ]
  }
}
```

---

## PreservationContracts

```json
{
  "PreservationContracts": [
    {
      "entity_id": "entity_01",
      "preservation_priority": "Critical",
      "recognizability_requirement": "Strong Match — subjects must read as young HK Gen Z East Asian adults (22–28) in social running context. Not athletes. Not influencers. Peers.",
      "immutable_attributes": [
        "East Asian ethnicity — subjects must read as Hong Kong young adults",
        "Age range 22–28 — professional-age Gen Z, not students, not older adults",
        "Social group interaction — at least two subjects visibly interacting with each other",
        "Running motion — subjects are mid-stride, not standing or walking",
        "Nike running apparel worn — at least one Nike brand element visible on clothing",
        "Group formation — 3–4 subjects running together, not a solo subject"
      ],
      "flexible_attributes": [
        "Exact gender composition — flexible within a mixed-gender grouping",
        "Exact number of subjects — 3 or 4 acceptable",
        "Specific clothing styles and colors — flexible within Nike athletic apparel register",
        "Exact facial expressions — mid-conversation, mid-laugh, or natural running expression all acceptable",
        "Exact running formation — loose cluster, not a rigid lineup"
      ]
    },
    {
      "entity_id": "entity_03",
      "preservation_priority": "High",
      "recognizability_requirement": "Strong Match — Nike Swoosh or wordmark must be recognizable as Nike brand",
      "immutable_attributes": [
        "Nike Swoosh geometry must be correct and legible",
        "Brand mark must appear on subject's clothing — not as a separate element"
      ],
      "flexible_attributes": [
        "Color of brand mark — adapts to garment color",
        "Position on garment — chest, sleeve, or side all acceptable",
        "Size of brand mark — scales naturally with garment at camera distance"
      ]
    },
    {
      "entity_id": "entity_04",
      "preservation_priority": "High",
      "recognizability_requirement": "Approximate Match — environment must read as Hong Kong outdoor setting. Specific location within HK is flexible.",
      "immutable_attributes": [
        "Environment must be recognizably Hong Kong — harbor, urban park, or city environment with HK skyline character",
        "Time of day must be evening — blue hour or early night with city lights",
        "Environment must be outdoor — not indoor, not studio"
      ],
      "flexible_attributes": [
        "Specific HK location — Victoria Harbour, West Kowloon, or other HK outdoor running area all acceptable",
        "Exact skyline composition",
        "Specific city light arrangement",
        "Weather conditions — clear, light haze, or atmospheric evening all acceptable"
      ]
    }
  ]
}
```

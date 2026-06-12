# Scene Contract
**Brand:** GigaSports
**Campaign:** Gigasports Pickle Club Community
**Framework:** Scene Assembly Framework v5.0
**Stage:** 5 — Scene Construction

---

## Inputs

**Global Pipeline State:**
- Aspect Ratio: 4:5 (Instagram feed post)
- Target Resolution: 1080×1350
- Safe Zones: Top 10% and bottom 20% reserved for text overlay and CTA

**From Art Direction:**
- Visual Intent: Belonging + Human Warmth + Ease
- Visual Concept: Social Encouragement in Motion — candid between-play social moment on pickleball court
- Subject Relationship Logic: Equality and Partnership — viewer as potential peer, not aspirational observer
- Perceptual Meaning: "This feels socially welcoming. These are people like me. I could belong here."
- Focal Priority: Human faces and social interaction first; sport context second

**From Image Analysis (Stage 5.0):**
- asset_01 (gigasports_logo.jpg) → entity_05: Brand-Bearing, Exact Match, reference-locked
- entity_05 source: Reference Asset — do not generate from training data

---

## Asset Analysis

**entity_05 — GigaSports Logo:** Reference asset provided (gigasports_logo.jpg). Classified Brand-Bearing. PreservationContract established in Stage 5.0. Source changes from Generated (Trial_01) to Reference Asset — logo reproduced from reference_asset_01, not hallucinated.

All other entities (entity_01 through entity_04) remain full generation — no reference assets provided for subjects, paddles, court, or venue.

---

## Asset Classification

| Entity ID | Description | Functional Roles | Source |
|-----------|-------------|-----------------|--------|
| entity_01 | Primary subject group — 2–3 young HK professionals mid-social interaction on court | Identity-Bearing, Symbolic | Generated |
| entity_02 | Pickleball paddles — held casually, not in aggressive play position | Supporting, Symbolic | Generated |
| entity_03 | Pickleball court surface and net | Environmental, Structural | Generated |
| entity_04 | Indoor sports venue environment — walls, ceiling, ambient elements | Environmental | Generated |
| entity_05 | GigaSports brand element — logo on banner or wall surface in venue background | Brand-Bearing | **Reference Asset (asset_01)** |

---

## Preservation Contracts

### entity_01 — Subject Group

**Preservation Priority:** Critical
**Recognizability Requirement:** Strong Match

**Immutable Attributes:**
- Age range: 25–35 years old
- Context: Urban HK professional appearance — athletic casual wear, not gym kit, not office attire
- Social dynamic: Genuine interaction — a moment of laughter, conversation, or celebratory gesture between people who are comfortable with each other
- Group size: 2–3 people
- Demographic: Reflects Hong Kong's young professional community — East/Southeast Asian subjects or mixed group natural to HK context

**Flexible Attributes:**
- Exact expressions and poses (must remain in social-warm register)
- Precise clothing items and colors
- Gender composition of group
- Exact spatial positioning within scene

---

### entity_02 — Pickleball Paddles

**Preservation Priority:** High
**Recognizability Requirement:** Approximate Match

**Immutable Attributes:**
- Must be identifiable as pickleball paddles (not tennis rackets, not badminton rackets)
- Must be held casually — at side, in hand between rallies, not mid-swing

**Flexible Attributes:**
- Brand/color of paddles
- Exact number visible
- Angle and orientation

---

### entity_03 — Pickleball Court and Net

**Preservation Priority:** High
**Recognizability Requirement:** Approximate Match

**Immutable Attributes:**
- Court surface must be recognizable as a pickleball/multi-sport court (line markings)
- Net must be present and visible in scene
- Court should communicate an active, real venue

**Flexible Attributes:**
- Court color
- How much of the court is visible
- Perspective angle of court lines

---

### entity_04 — Indoor Sports Venue Environment

**Preservation Priority:** Medium
**Recognizability Requirement:** Loose Match

**Immutable Attributes:**
- Must feel like an indoor sports facility — not a hotel ballroom, not a gym weight room
- Lighting must read as sports venue ambient lighting — not dramatic studio lighting

**Flexible Attributes:**
- Specific architectural details
- Ceiling height and structure
- Presence or absence of other players in background

---

### entity_05 — GigaSports Brand Element

**Preservation Priority:** High
**Recognizability Requirement:** Exact Match
**Source:** Reference Asset (asset_01 — gigasports_logo.jpg)

**Immutable Attributes (from ImageAnalysisContract):**
- Wordmark: 'GigaSports' in bold italic compressed sans-serif
- Globe icon replacing the 'O' in 'Sports' — stylized world map sphere
- 'BE PROFESSIONAL' tagline in small caps centered below wordmark
- White coloring of all logo elements
- Wide horizontal format proportions

**Flexible Attributes:**
- Scale relative to scene
- Exact position on venue wall or banner
- Bokeh rendering depth (may be soft but must remain legible)

**Generation Rule:** Reproduce from reference_asset_01. Do not generate from training data.

---

## Reality Model

**Type:** Realistic

**Coherence Rules:**
- Scale: Realistic — all entities proportional to real-world pickleball venue
- Perspective: Realistic — natural camera perspective, no forced distortion
- Anchoring: Required — all subjects floor-anchored within venue
- Environmental Behavior: Realistic — indoor sports venue lighting, natural spatial relationships

---

## Physical Construction

### Depth Structure

**Foreground:**
- entity_01 (subject group) — faces readable, social dynamic visible
- entity_02 (paddles) — held by subjects, incidentally visible

**Midground:**
- entity_03 (court surface and net) — establishes sport context

**Background:**
- entity_04 (venue environment) — atmospheric depth and mood
- entity_05 (GigaSports logo on banner/wall) — legible but not dominant

---

### Spatial Relationships

| Relationship | Subject | Relation | Object |
|---|---|---|---|
| Social proximity | entity_01a (person 1) | facing / adjacent to | entity_01b (person 2) |
| Physical grounding | entity_01 (group) | floor_anchored | entity_03 (court surface) |
| Court context | entity_01 (group) | positioned near | entity_03 (net area) |
| Brand placement | entity_05 (GigaSports logo) | visible behind | entity_01 (group) |
| Equipment presence | entity_02 (paddles) | held by | entity_01 (group) |

---

### Scale Relationships

| Entity | Reference | Scale Relationship |
|---|---|---|
| entity_01 (subjects) | entity_03 (court/net) | Realistic human scale — subjects occupy primary visual weight |
| entity_02 (paddles) | entity_01 (subjects) | Proportional — standard paddle size relative to human subjects |
| entity_05 (brand element) | entity_04 (venue) | Environmental scale — banner-appropriate, not oversized |

---

### Anchor Relationships

| Entity | Anchor Type |
|---|---|
| entity_01 (subject group) | Floor-anchored to court surface |
| entity_02 (paddles) | Attached-to entity_01 (held by subjects) |
| entity_03 (net) | Floor-anchored — fixed structural element |
| entity_05 (brand element) | Wall-anchored — banner or wall mount in venue background |

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
      { "id": "entity_01", "description": "Group of 2-3 young HK professionals (25-35) in candid social interaction on pickleball court", "roles": ["Identity-Bearing", "Symbolic"], "source": "Generated" },
      { "id": "entity_02", "description": "Pickleball paddles, casually held — not in active play position", "roles": ["Supporting", "Symbolic"], "source": "Generated" },
      { "id": "entity_03", "description": "Pickleball court surface with net", "roles": ["Environmental", "Structural"], "source": "Generated" },
      { "id": "entity_04", "description": "Indoor sports venue environment", "roles": ["Environmental"], "source": "Generated" },
      { "id": "entity_05", "description": "GigaSports logo on banner or wall surface in venue background", "roles": ["Brand-Bearing"], "source": "Reference Asset", "asset_id": "asset_01", "prompt_reference_id": "reference_asset_01" }
    ],

    "Relationships": [
      { "subject": "entity_01a", "relation": "facing", "object": "entity_01b" },
      { "subject": "entity_01", "relation": "adjacent_to", "object": "entity_03" },
      { "subject": "entity_02", "relation": "attached_to", "object": "entity_01" },
      { "subject": "entity_05", "relation": "visible_behind", "object": "entity_01" }
    ],

    "AnchorRelationships": [
      { "entity_id": "entity_01", "anchor_type": "floor_anchored" },
      { "entity_id": "entity_02", "anchor_type": "attached_to_entity", "target_entity": "entity_01" },
      { "entity_id": "entity_03", "anchor_type": "floor_anchored" },
      { "entity_id": "entity_05", "anchor_type": "wall_anchored" }
    ],

    "DepthStructure": {
      "foreground": ["entity_01", "entity_02"],
      "midground": ["entity_03"],
      "background": ["entity_04", "entity_05"]
    },

    "RelativeScale": [
      { "entity_id": "entity_01", "reference_entity": "entity_03", "scale_relationship": "realistic human scale — subjects occupy dominant visual weight" },
      { "entity_id": "entity_02", "reference_entity": "entity_01", "scale_relationship": "proportional paddle size relative to human subjects" },
      { "entity_id": "entity_05", "reference_entity": "entity_04", "scale_relationship": "banner-scale — legible but not dominant relative to venue wall" }
    ],

    "GenerationRequirements": {
      "required_entities": ["entity_01", "entity_02", "entity_03", "entity_05"],
      "required_supporting_objects": [],
      "required_environment_elements": ["entity_04 — indoor sports venue with ambient venue lighting"],
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
        "immutable_attributes": ["Age range 25–35", "HK professional appearance in athletic casual wear", "Candid social interaction dynamic", "Group size 2–3", "East/Southeast Asian or HK-representative demographic"],
        "flexible_attributes": ["Exact expressions and poses", "Specific clothing items", "Gender composition", "Precise spatial positioning"]
      },
      {
        "entity_id": "entity_02",
        "preservation_priority": "High",
        "recognizability_requirement": "Approximate Match",
        "immutable_attributes": ["Must be identifiable as pickleball paddles", "Must be held casually between rallies — not mid-swing"],
        "flexible_attributes": ["Paddle brand and color", "Exact number visible", "Angle and orientation"]
      },
      {
        "entity_id": "entity_03",
        "preservation_priority": "High",
        "recognizability_requirement": "Approximate Match",
        "immutable_attributes": ["Recognizable court surface with line markings", "Net must be present and visible"],
        "flexible_attributes": ["Court color", "Proportion of court visible", "Perspective angle"]
      },
      {
        "entity_id": "entity_05",
        "preservation_priority": "High",
        "recognizability_requirement": "Exact Match",
        "source": "Reference Asset — asset_01 (gigasports_logo.jpg)",
        "immutable_attributes": [
          "Bold italic 'GigaSports' wordmark in compressed sans-serif",
          "Globe icon replacing the O in Sports",
          "'BE PROFESSIONAL' tagline in small caps below wordmark",
          "White coloring on all elements",
          "Wide horizontal format proportions"
        ],
        "flexible_attributes": ["Scale", "Position on wall/banner", "Bokeh rendering depth"],
        "generation_rule": "Use reference_asset_01 — do not generate from training data"
      }
    ]
  }
}
```

# Image Analysis Contract
**Brand:** Nike
**Campaign:** Nike Chill Run Club
**Framework:** Image Analysis Framework v1.0
**Stage:** 5.0 — Asset Extraction

---

## Client Intent Record

> **Note:** Client did not explicitly specify intent. Intent has been inferred from campaign context (HK Gen Z professionals, HK urban night setting) and the nature of the reference image (Western subjects, daytime park, non-HK location). Assumptions documented below — confirm with client before locking.

```
Asset: reference_group_run.jpg
Lock categories: Composition / Template + Style Only
Strictness: Reference Only
Exclusions:
  - Do not carry over subjects — subjects are Caucasian/Western, campaign requires HK Gen Z Asian demographic
  - Do not carry over environment — setting is a non-HK outdoor park; campaign requires Hong Kong urban/waterfront evening setting
  - Do not carry over time of day — reference is daytime; campaign brief specifies HK night scenery
  - Do not carry over Nike "JUST DO IT" shirt as a locked brand element — treat as style reference only for brand presence character
```

---

## ImageAnalysisContract

```json
{
  "ImageAnalysisContract": {

    "Metadata": {
      "brand": "Nike",
      "campaign": "Nike Chill Run Club",
      "framework": "Image Analysis Framework v1.0",
      "stage": "5.0 — Asset Extraction",
      "reference_images_provided": 1,
      "generation_mode": "Full Generation (style-guided)"
    },

    "AssetInventory": [
      {
        "asset_id": "asset_01",
        "filename": "reference_group_run.jpg",
        "classification": ["Composition / Template", "Style Reference"],
        "entity_assignment": "style_reference_only",
        "client_intent": "Reference the group running composition, social dynamic, and photographic style — do not lock any specific subjects, environment, or brand elements"
      }
    ],

    "PreservationContracts": [
      {
        "asset_id": "asset_01",
        "entity_id": "style_reference_only",
        "classification": "Style Reference + Composition Template",
        "preservation_priority": "Flexible",
        "recognizability_requirement": "Reference Only — no elements must be reproduced exactly",

        "observations": [
          "5 young subjects (approximately ages 21–28) running together in a loose horizontal cluster formation",
          "3 female subjects, 2 male subjects",
          "All subjects appear Caucasian/Western — NOT the target demographic for HK campaign",
          "Running at a comfortable social pace — not sprinting, not jogging slowly",
          "Subjects mostly wear black athletic wear; one male wears a Nike 'JUST DO IT' graphic tee",
          "Running shoes visible on all subjects — multiple brands including Nike",
          "Outdoor setting: rubber running path, green grass border, trees and foliage background",
          "Daytime — natural directional sunlight from camera-right creating warm side light and some shadow",
          "Group formation spans the full width of the path — approximately 3 metres wide",
          "Subjects show social awareness of each other: some looking at each other, some ahead",
          "Medium-wide framing: full bodies visible from head to feet with slight headroom",
          "Eye-level camera angle — photographer is at the same height as the running subjects",
          "Camera is directly in front of the group, subjects running toward camera",
          "Setting is NOT Hong Kong — appears to be an Australian or similar Western country park"
        ],

        "immutable_attributes": [],

        "flexible_attributes": [
          {
            "attribute": "Group running formation — 3 to 5 subjects in a loose horizontal cluster",
            "reason": "This composition structure communicates social group energy and should be referenced for the generated scene"
          },
          {
            "attribute": "Full-body medium-wide framing showing legs and feet in motion",
            "reason": "Validates the shot type and framing density — subjects should be readable as running bodies, not just portrait crop"
          },
          {
            "attribute": "Camera facing toward approaching subjects — eye-level, direct axis",
            "reason": "Establishes the viewer-equals relationship — camera at running height, subjects moving toward viewer"
          },
          {
            "attribute": "Social running dynamic — subjects aware of each other, not performing for camera",
            "reason": "Core composition energy to reference: the image reads as a social moment, not a sport performance"
          },
          {
            "attribute": "Nike brand apparel visible on at least one subject",
            "reason": "Confirms brand placement strategy — branding on worn apparel, not as a prop or separate brand element"
          },
          {
            "attribute": "Natural directional light from one side creating warm, realistic illumination",
            "reason": "Photography style reference — naturalistic, editorial, not studio-lit"
          }
        ],

        "uncertainties": [],

        "generation_instruction": "Do NOT reproduce any specific subject, face, body, or environment from this reference. Use this image only to inform: (1) group running composition — loose horizontal cluster of 3–4 subjects running together toward camera; (2) full-body medium-wide framing; (3) eye-level camera axis; (4) social candid energy — subjects engaged with each other, not posed for camera; (5) naturalistic editorial photography style with directional light. Replace subjects with HK Gen Z Asian subjects. Replace environment with Hong Kong evening urban/waterfront setting."
      }
    ],

    "SceneAssemblyHandoff": {
      "entity_source_map": [
        {
          "entity_id": "entity_01",
          "source": "Generated",
          "asset_id": null,
          "generation_mode": "Generate — HK Gen Z Asian subjects, 3–4 people, mixed gender, ages 22–28. Running together in social group. Nike running apparel."
        },
        {
          "entity_id": "entity_02",
          "source": "Generated",
          "asset_id": null,
          "generation_mode": "Generate — Nike running shoes on subjects. Visible at feet during running motion."
        },
        {
          "entity_id": "entity_03",
          "source": "Generated",
          "asset_id": null,
          "generation_mode": "Generate — Nike brand apparel element. Swoosh or minimal Nike mark visible on at least one subject's clothing."
        },
        {
          "entity_id": "entity_04",
          "source": "Generated",
          "asset_id": null,
          "generation_mode": "Generate — Hong Kong outdoor evening environment. Victoria Harbour waterfront, West Kowloon, or urban park with HK city skyline in background. Evening/blue hour light."
        }
      ],
      "partial_generation_note": "All entities are fully generated. This is a Full Generation campaign. The reference image informs composition structure and photographic style only — no elements are reference-locked."
    },

    "ClientConfirmationRequired": [
      {
        "asset_id": "asset_01",
        "attribute": "Client intent assumed as Style + Composition Reference Only",
        "question": "Can you confirm that no elements from the reference image should be locked? Specifically: (1) subjects are not the target demographic — generate new HK Asian subjects? (2) environment should be Hong Kong, not this location? (3) daytime should become evening/night per campaign brief?",
        "blocking": false
      }
    ]

  }
}
```

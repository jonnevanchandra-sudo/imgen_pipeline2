# Scene Contract
**Brand:** Nike
**Campaign:** Nike Chill Run Club — Trial 04
**Framework:** Scene Assembly Framework v5.2
**Stage:** 5 — Scene Construction + Reference Image Extraction

---

## Framework Selection

**v5.2 selected:** Reference images are present (reference_asset_01, reference_asset_02, reference_asset_03) AND a named product model (Nike Alphafly 3) is specified in the CampaignContract. Framework 5.2 absorbs both reference extraction and named product preservation in one stage.

---

## Reference Asset Extraction

### reference_asset_01 — Subject 01 (User)

**File:** user_face.jpg (placeholder — user-provided at generation)
**Classification:** Character-Identity
**Entity assignment:** entity_01
**Strictness:** Exact — subject appearance must match reference_asset_01

| Attribute | Value | Notes |
|---|---|---|
| Subject identity | User (campaign client) | Appearance fully locked to reference image |
| Appearance | See reference_asset_01 | No independent description — all facial and physical appearance deferred to reference |
| Age range | As shown in reference | |

**Immutable:** Full appearance as shown in reference_asset_01 — face, skin tone, general physical appearance
**Flexible:** Exact hairstyling, specific clothing beyond the Alphafly 3, expression (must carry NarrativeContract emotional register)

---

### reference_asset_02 — Subject 02 (Karina from aespa)

**File:** karina_reference.jpg (placeholder — user-provided at generation)
**Classification:** Character-Identity
**Entity assignment:** entity_02
**Strictness:** Exact — subject appearance from reference_asset_02; name anchors generation alongside reference

| Attribute | Value | Notes |
|---|---|---|
| Subject identity | Karina (from aespa) | Named public figure — name used alongside reference for generation anchoring |
| Appearance | See reference_asset_02 | Do not describe appearance independently; reference_asset_02 is the authority |

**Immutable:** Karina's appearance as shown in reference_asset_02 — reproduce from reference, not from training data description
**Flexible:** Exact hairstyling, specific clothing beyond the Alphafly 3, expression (must carry NarrativeContract emotional register)

**Generation note:** The name "Karina from aespa" and reference_asset_02 must both travel to the Prompt Compiler. Name alone may drift toward training-data generalization; reference anchors the specific appearance.

---

### reference_asset_03 — Nike Alphafly 3

**File:** alphafly3_reference.jpg (placeholder — user-provided at generation)
**Classification:** Brand-Bearing / Product Reference
**Entity assignment:** entity_03
**Strictness:** Exact — colorway and key visual identifiers from reference_asset_03

**Attributes extracted by observation and training knowledge:**

| Attribute | Source | Notes |
|---|---|---|
| Model name | Training knowledge | Nike Alphafly 3 — confirmed named product |
| Midsole | Training knowledge | Extreme-stack ZoomX foam — very tall, lightweight, visually dominant height profile |
| Carbon plate | Training knowledge | Full-length carbon fiber plate embedded in midsole — not visible externally but part of the recognizable racing silhouette |
| Upper | Training knowledge | Lightweight Atomknit 3.0 race upper — thin, breathable, close-fitting to foot |
| Swoosh | Training knowledge | Nike Swoosh on lateral midfoot |
| Outsole | Training knowledge | Thin rubber traction pods — not a full-coverage outsole; ground contact is minimal rubber spots |
| Silhouette | Training knowledge | Racing flat with aggressively elevated stack — distinctive forward pitch |
| Colorway | reference_asset_03 | Exact colorway from reference image — do not substitute or generalize |

**Immutable:** Nike Swoosh on lateral side; extreme ZoomX stack height; racing flat silhouette; colorway from reference_asset_03; Alphafly upper construction
**Flexible:** Exact angle at which shoe is visible; whether heel or forefoot is more prominent given mid-run position

---

## ReferenceAssetManifest

```json
[
  {
    "asset_id": "asset_01",
    "filename": "user_face.jpg",
    "type": "Character-Identity",
    "prompt_reference_id": "reference_asset_01",
    "entity_id": "entity_01",
    "attach_to_api_call": true,
    "strictness": "Exact"
  },
  {
    "asset_id": "asset_02",
    "filename": "karina_reference.jpg",
    "type": "Character-Identity",
    "prompt_reference_id": "reference_asset_02",
    "entity_id": "entity_02",
    "attach_to_api_call": true,
    "strictness": "Exact"
  },
  {
    "asset_id": "asset_03",
    "filename": "alphafly3_reference.jpg",
    "type": "Brand-Bearing",
    "prompt_reference_id": "reference_asset_03",
    "entity_id": "entity_03",
    "attach_to_api_call": true,
    "strictness": "Exact"
  }
]
```

---

## Scene Contract

```json
{
  "SceneContract": {

    "FrameworkVersion": "5.2",
    "SelectionReason": "Three reference images provided (subject_01 face, subject_02 face, Nike Alphafly 3) AND a named product model in CampaignContract. All reference extraction and product preservation handled in this stage.",

    "RealityModel": {
      "type": "Photographic Realism",
      "description": "Premium editorial lifestyle photography. Outdoor urban HK environment. Natural ambient evening/night light. Motion-captured aesthetic — feels like a skilled photographer running alongside the subjects. No CGI, no stylization."
    },

    "Entities": [

      {
        "entity_id": "entity_01",
        "label": "Subject 01 — User",
        "type": "Human — Character-Identity Reference",
        "reference": "reference_asset_01",
        "description": "Appearance locked to reference_asset_01. Running mid-stride alongside entity_02 in a HK urban environment at night. Wearing Nike Alphafly 3 (entity_03) on both feet.",
        "preservation_contract": {
          "immutable": [
            "Appearance: see reference_asset_01 — reproduce face and physical appearance from reference, not independently generated",
            "Wearing Nike Alphafly 3 (entity_03) — shoe on both feet",
            "In genuine running motion — mid-stride, not posed"
          ],
          "flexible": [
            "Exact clothing beyond the Alphafly 3",
            "Exact hairstyle unless specified in reference",
            "Expression — must carry ease, warmth, motion; not grimacing, not performing for camera"
          ]
        }
      },

      {
        "entity_id": "entity_02",
        "label": "Subject 02 — Karina from aespa",
        "type": "Human — Character-Identity Reference",
        "reference": "reference_asset_02",
        "name": "Karina from aespa",
        "description": "Karina from aespa — appearance from reference_asset_02. Running mid-stride alongside entity_01. Wearing Nike Alphafly 3 (entity_03) on both feet.",
        "preservation_contract": {
          "immutable": [
            "Identity: Karina from aespa — reproduce from reference_asset_02 with name as generation anchor",
            "Wearing Nike Alphafly 3 (entity_03) — shoe on both feet",
            "In genuine running motion — mid-stride, not posed"
          ],
          "flexible": [
            "Exact clothing beyond the Alphafly 3",
            "Exact hairstyle unless specified in reference",
            "Expression — ease, presence, warmth; not celebrity pose, not performing for camera"
          ]
        }
      },

      {
        "entity_id": "entity_03",
        "label": "Nike Alphafly 3",
        "type": "Named Product — Brand-Bearing Reference",
        "model_name": "Nike Alphafly 3",
        "reference": "reference_asset_03",
        "description": "Worn by both entity_01 and entity_02. Visible mid-run on at least one subject's foot. Colorway from reference_asset_03. Key identifiers: extreme ZoomX stack height, Atomknit upper, Nike Swoosh on lateral side, thin rubber pod outsole, racing flat silhouette.",
        "preservation_contract": {
          "immutable": [
            "Model name: Nike Alphafly 3 — must travel with visual identifiers to Prompt Compiler",
            "Colorway: from reference_asset_03 — reproduce exactly",
            "Extreme ZoomX midsole stack height — the tallest visual element of the shoe profile",
            "Nike Swoosh on lateral side — must be legible on at least one shoe in frame",
            "Racing flat silhouette — forward pitch, elevated stack, recognizable at running scale",
            "Lightweight race upper — thin and close-fitting, not a cushioned training shoe upper"
          ],
          "flexible": [
            "Exact angle of shoe visible — mid-run position determines natural exposure",
            "Whether heel or forefoot is more prominent — depends on stride phase"
          ]
        }
      },

      {
        "entity_id": "entity_04",
        "label": "HK Urban Night Environment",
        "type": "Environment",
        "description": "Hong Kong outdoor urban environment at evening or night. City lights active. Could be harbourfront, Tsim Sha Tsui waterfront, or urban street with visible HK skyline or city density. Warm-cool city light mixture characteristic of HK at night.",
        "preservation_contract": {
          "immutable": [
            "Must be recognizably Hong Kong — not generic Asian night city",
            "Evening or night setting — city lights on",
            "Outdoor — not a treadmill, not an indoor track"
          ],
          "flexible": [
            "Exact HK location — harbourfront, Tsim Sha Tsui, urban street all acceptable",
            "Degree of background bokeh vs. sharpness",
            "Exact city landmarks — HK character is sufficient, specific buildings not required"
          ]
        }
      }

    ],

    "Relationships": [
      {
        "relationship": "entity_01 + entity_02",
        "type": "Running Companions — Equal Presence",
        "description": "Both subjects running together at conversational pace — side by side or in easy near-proximity. Neither leads or trails significantly. The shared motion is the visual subject."
      },
      {
        "relationship": "entity_01 + entity_03 / entity_02 + entity_03",
        "type": "Product-on-Subjects",
        "description": "Both subjects wear the Alphafly 3. Shoe is visible as part of mid-run motion — seen on at least one subject's foot in the stride."
      },
      {
        "relationship": "subjects + entity_04",
        "type": "Subject-in-Environment",
        "description": "Subjects are running through HK — the city is their backdrop and their context. They belong to it. The city at night communicates: this is available to you, here, tonight."
      }
    ],

    "DepthStructure": {
      "foreground": "entity_01 and entity_02 — bodies from approximately mid-thigh to crown; mid-stride; both faces and shoes partially visible",
      "midground": "Running surface — HK pavement or harbourfront path",
      "background": "HK skyline, city lights, harbour or urban density — warm-cool bokeh; unmistakably HK"
    },

    "GenerationRequirements": {
      "subject_reference_preservation": "Both entity_01 and entity_02 appearance must be reproduced from their respective reference images. Do not generate faces independently.",
      "product_name_preservation": "Nike Alphafly 3 model name must travel to Prompt Compiler's product/brand description paired with all key_visual_identifiers and reference_asset_03.",
      "shoe_legibility": "At least one Alphafly 3 must be legible in the frame — Swoosh visible, distinctive stack height readable at running scale.",
      "motion_authenticity": "Both subjects in genuine mid-run stride — not posed running, not standing with running gear."
    }

  }
}
```

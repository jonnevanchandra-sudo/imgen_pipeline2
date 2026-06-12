# Scene Contract
**Brand:** Hong Kong Football Association (HKFA)
**Campaign:** Hong Kong World Cup 2026 — Team Hoodie Launch
**Framework:** Scene Assembly Framework v5.1
**Stage:** 5 — Scene Construction

---

```json
{
  "SceneContract": {

    "FrameworkVersion": "5.1",
    "SelectionReason": "CampaignContract contains a named product model (Hong Kong National Team FIFA World Cup 2026 Hoodie) with ProductSpec. No reference images uploaded. Framework 5.1 locks model name and key visual identifiers together as immutable — name alone is insufficient for image generators to reproduce a specific kit design.",

    "InputsConsumed": {
      "CampaignContract": "HKFA World Cup 2026 CampaignContract v1.1 — Trial 01",
      "StrategyContract": "HKFA World Cup 2026 StrategyContract — Trial 01",
      "NarrativeContract": "HKFA World Cup 2026 NarrativeContract — Trial 01",
      "ArtDirectionContract": "HKFA World Cup 2026 ArtDirectionContract — Trial 01"
    },

    "RealityModel": {
      "type": "Photographic Realism",
      "description": "Premium documentary photography. Outdoor urban environment. Real HK city context. Natural ambient light. No CGI, no stylization, no illustration."
    },

    "Entities": [

      {
        "entity_id": "entity_01",
        "label": "HK Young Adult Subject — Primary",
        "type": "Human",
        "description": "HK young adult, male or female, approximately 20–28 years old. Ethnically East Asian. Real, recognizable as a young HK person — not a model archetype. Wearing the HK World Cup 2026 hoodie.",
        "preservation_contract": {
          "immutable": [
            "Wearing the HK World Cup 2026 team hoodie (entity_03) — product must be on this subject",
            "Expression: quiet, personal pride — not performing for the camera, not triumphant, not neutral; the specific face of someone who knows where they are from",
            "Age range: 20–28"
          ],
          "flexible": [
            "Exact face, hairstyle, and individual appearance — generator determines based on realistic HK young adult",
            "Exact pose: standing, walking, or in relaxed motion — all acceptable; no athletic posture",
            "Exact position in frame relative to entity_02 (if present)"
          ]
        }
      },

      {
        "entity_id": "entity_02",
        "label": "HK Young Adult Subject — Secondary (Optional)",
        "type": "Human",
        "description": "Second HK young adult, opposite gender to entity_01, approximately 20–28 years old. Also wearing the HK World Cup 2026 hoodie. Presence adds collective belonging dimension — two people sharing the same red in the same city.",
        "presence": "Optional — include if it strengthens the collective pride reading; scene works with one or two subjects",
        "preservation_contract": {
          "immutable": [
            "Wearing the HK World Cup 2026 team hoodie (entity_03)",
            "Expression consistent with entity_01 — quiet personal pride, not performed",
            "Age range: 20–28"
          ],
          "flexible": [
            "Exact face, hairstyle, and individual appearance",
            "Exact pose and body position",
            "Gender — opposite to entity_01"
          ]
        }
      },

      {
        "entity_id": "entity_03",
        "label": "HK World Cup 2026 Team Hoodie",
        "type": "Named Product",
        "model_name": "Hong Kong National Team FIFA World Cup 2026 Hoodie",
        "colorway": "Dragon Red / White",
        "preservation_contract": {
          "immutable": [
            "model_name: Hong Kong National Team FIFA World Cup 2026 Hoodie — this name must travel with the visual identifiers through Synthesis to the Prompt Compiler's brand key",
            "HKFA dragon crest badge on the left chest — primary identity mark; must be legible at the image's subject scale",
            "Red body — dominant colorway; the hoodie reads red first; this is the flag color and the campaign's visual anchor",
            "White accents: collar trim, cuff trim, and hem trim distinguish this kit from a generic red hoodie",
            "香港 HONG KONG lettering — present on the hoodie (chest or back yoke); the text confirms HK identity",
            "FIFA World Cup 2026 patch on the right sleeve — confirms the specific edition",
            "Pullover hoodie silhouette with drawstring hood — not a zip-up, not a jacket"
          ],
          "flexible": [
            "Exact rendering of the World Cup 2026 patch fine detail — legibility over accuracy",
            "Whether hood is up or down on subjects — either reads as natural",
            "Exact shade of red within the Dragon Red family — warm red, not orange-red or pink-red"
          ]
        }
      },

      {
        "entity_id": "entity_04",
        "label": "HK Urban Environment",
        "type": "Environment",
        "description": "Recognizable Hong Kong urban environment — harbourfront, Tsim Sha Tsui waterfront, urban street, or city backdrop with skyline visible. HK at its most distinctively itself: dense, layered, warm and cool city light mixture, vertical city scale.",
        "time_of_day": "Evening to night — city lights active, ambient glow, warm-cool light mixture characteristic of HK urban at dusk or after dark",
        "preservation_contract": {
          "immutable": [
            "Must be unmistakably Hong Kong — not generic Asian city, not Singapore, not Shanghai",
            "HK skyline, harbour, or dense urban streetscape must be legible in the background",
            "Evening or night setting — city lights on; not day, not golden hour"
          ],
          "flexible": [
            "Exact location within HK — harbourfront, Tsim Sha Tsui, Wan Chai, urban street all acceptable",
            "Exact background detail — specific buildings need not be identifiable; the character of HK is sufficient",
            "Degree of bokeh vs. sharpness in background"
          ]
        }
      }

    ],

    "Relationships": [
      {
        "relationship": "entity_01 + entity_03",
        "type": "Product-on-Subject",
        "description": "The hoodie is worn by entity_01. The crest is on their chest. The red is the most prominent color on their body. The product is the vehicle for the emotional argument — not displayed, worn."
      },
      {
        "relationship": "entity_02 + entity_03 (if present)",
        "type": "Product-on-Subject",
        "description": "entity_02 also wears the same hoodie. Two subjects in the same red is the visual statement of collective belonging."
      },
      {
        "relationship": "subjects + entity_04",
        "type": "Subject-in-Environment",
        "description": "Subjects are in the HK environment — they belong to it, they are not posed in front of it. The city is theirs. The red hoodie in the city reads as the city's own color worn by the city's own people."
      }
    ],

    "DepthStructure": {
      "foreground": "entity_01 (and entity_02 if present) — bodies from head to lower torso; faces and dragon crest in primary focus layer",
      "midground": "Urban street surface or harbourfront path — physical grounding of subjects in HK",
      "background": "HK skyline, harbor, or urban density — warm bokeh or slightly soft focus; unmistakably HK but not competing with subjects"
    },

    "GenerationRequirements": {
      "product_name_preservation": "The model name 'Hong Kong National Team FIFA World Cup 2026 Hoodie' must travel to the Prompt Compiler's HIGH brand block paired with all key_visual_identifiers. Name alone will not generate the correct kit design — the identifiers define what makes this specific product visually.",
      "crest_legibility": "The HKFA dragon crest must be legible at the scale the subject appears in the frame. This is the primary identity mark — if the crest is illegible, the product is a generic red hoodie.",
      "red_dominance": "The Dragon Red of the hoodie must be the dominant color in the frame — the image is anchored by this red. It should read on first glance before any other detail.",
      "environment_authenticity": "HK environment must read as genuinely HK — not a generic night city. The specific skyline character, harbour, or urban density of HK must be present."
    }

  }
}
```

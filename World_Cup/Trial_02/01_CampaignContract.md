# Campaign Contract
**Brand:** Hong Kong Football Association (HKFA)
**Campaign:** Hong Kong World Cup 2026 — Team Hoodie Launch
**Framework:** Campaign Brief v1.1
**Stage:** 1 — Campaign Definition

---

```json
{
  "CampaignContract": {

    "BusinessObjective": {
      "objective_type": "Product Launch + Cultural Identity Activation",
      "success_metric": "Sell-through of HK World Cup 2026 team hoodie; secondary: social sharing and earned media from local pride activation"
    },

    "CampaignTheme": {
      "theme_token": "代表香港 — Represent HK",
      "theme_description": "The Hong Kong national football team is going to the world stage. This hoodie is how Hong Kong people wear that moment — not as performance gear, but as a declaration: this city is here, this team is ours, we represent."
    },

    "MessageHierarchy": {
      "primary_message": "Wearing this hoodie means you are part of Hong Kong's moment on the world stage — not just a supporter, but a representative of your city",
      "secondary_messages": [
        "The dragon crest and the red belong to everyone who calls Hong Kong home",
        "The World Cup is global — HK's presence on it is local pride made visible",
        "This is not about winning or losing. This is about showing up."
      ],
      "offer_message": "The Hong Kong World Cup 2026 team hoodie — available now"
    },

    "AudienceContext": {
      "primary_audience": "HK young adults aged 18–35 who identify with Hong Kong as home — football fans and non-fans alike; local pride is the bridge",
      "secondary_audience": "Committed HK football supporters and HKFA community members who follow the national team",
      "core_motivation": "Pride in local identity; the desire to be seen as part of something that represents Hong Kong on a global stage",
      "primary_barrier": "HK football is not a dominant cultural conversation — the audience may not follow football but will respond to the pride and identity framing of HK representation at the World Cup"
    },

    "OfferDefinition": {
      "offer_type": "Product Purchase",
      "offer_value": "Limited edition HK national team World Cup 2026 hoodie — the official team kit item representing HK at FIFA World Cup 2026",
      "call_to_action": "Get yours — represent Hong Kong"
    },

    "OfferRole": {
      "priority": "Primary",
      "visibility_requirement": "Required — product must be visible and identifiable in the image"
    },

    "ChannelContext": {
      "primary_channel": "Instagram",
      "placement_type": "Feed post — organic social media"
    },

    "ChannelBehavior": {
      "attention_window": "Short",
      "interaction_model": "Passive",
      "placement_context": "Instagram feed — competing with lifestyle content; the red kit must stop scroll on color alone; Cantonese copy overlay added in post-production"
    },

    "CampaignConstraints": {

      "MessageConstraints": {
        "required_messages": {
          "tokens": ["代表香港", "World Cup 2026", "Local Pride", "Hong Kong Identity"],
          "custom": [
            "Pride framing — not performance or athletic achievement framing",
            "Inclusive: football fans AND non-fans can belong to this campaign",
            "HK identity as the core emotional product — the hoodie is the vehicle for that identity"
          ]
        },
        "forbidden_messages": {
          "tokens": ["Elite performance", "Football skill", "Winning", "Victory"],
          "custom": [
            "Do not frame this as a football performance campaign — it is a cultural identity campaign",
            "Do not use competitive or athletic achievement language",
            "Do not reference football match outcomes or qualification narrative"
          ]
        }
      },

      "BrandConstraints": {
        "required_brand_elements": {
          "tokens": ["HKFA dragon crest", "HK team red", "香港 HONG KONG"],
          "custom": [
            "The HK World Cup hoodie must be prominently visible and identifiable in the image",
            "Dragon crest on the hoodie must be legible",
            "Red colorway must dominate the product presence"
          ]
        },
        "forbidden_positioning": {
          "tokens": ["Exclusive", "Elite athlete", "Performance transformation"],
          "custom": [
            "Do not position the hoodie as performance or technical sportswear — it is cultural identity wear",
            "Do not use professional athlete imagery — this is for everyday HK people"
          ]
        }
      },

      "LegalConstraints": {
        "tokens": [],
        "custom": []
      },

      "PlatformConstraints": {
        "tokens": ["Instagram 4:5 vertical format"],
        "custom": [
          "Output format: 1080 x 1350 pixels, 4:5 aspect ratio",
          "Top 10% of frame: reserved for Cantonese headline copy overlay (post-production)",
          "Bottom 20% of frame: reserved for product name, CTA, and HKFA / World Cup 2026 identifier (post-production)",
          "No critical visual information — faces, dragon crest, product — may appear in reserved zones"
        ]
      }
    },

    "MandatoryRequirements": {
      "required_assets": [
        "HK young adult subject(s) wearing the HK World Cup 2026 team hoodie",
        "Hong Kong outdoor or urban environment — city, harbour, or urban space recognizable as HK"
      ],
      "required_copy": [
        "Cantonese headline copy added in post-production (not embedded in generated image)",
        "HKFA / World Cup 2026 reference visible in post-production overlay"
      ],
      "required_branding": [
        "HKFA dragon crest visible on the hoodie in the generated image",
        "Red colorway of the HK team hoodie clearly visible"
      ],
      "ProductSpec": {
        "model_name": "Hong Kong National Team FIFA World Cup 2026 Hoodie",
        "colorway": "Dragon Red / White",
        "key_visual_identifiers": [
          "HKFA dragon crest badge on the left chest — primary identity mark; must be legible",
          "Red body — the dominant colorway, tied directly to the HK flag",
          "White accents: collar trim, cuff trim, and hem trim in white",
          "香港 HONG KONG lettering — either on the back yoke or front chest below the crest",
          "FIFA World Cup 2026 patch on the right sleeve",
          "Pullover hoodie silhouette with drawstring hood"
        ]
      }
    },

    "CampaignPriority": {
      "primary_objective": "Drive hoodie sales and cultural pride activation among HK young adults",
      "primary_message": "Wearing this hoodie means you represent Hong Kong — football fan or not",
      "primary_offer": "HK World Cup 2026 team hoodie — get yours",
      "primary_constraint": "Must not communicate athletic performance, football skill, or competitive achievement framing — this is a cultural pride and identity campaign"
    }

  }
}
```

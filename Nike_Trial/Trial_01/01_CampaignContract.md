# Campaign Contract
**Brand:** Nike
**Campaign:** Nike Chill Run Club
**Framework:** Campaign Brief v1.0
**Stage:** 1 — Campaign Definition

---

```json
{
  "CampaignContract": {

    "BusinessObjective": {
      "objective_type": "Product Awareness",
      "success_metric": "Brand awareness increase among Gen Z HK working professionals who currently do not run; secondary metric: sign-ups to Nike Chill Run Club events"
    },

    "CampaignTheme": {
      "theme_token": "Nike Chill Run Club",
      "theme_description": "A social running community for HK Gen Z working professionals that frames post-work running as a Mental Reset and social bonding ritual — not athletic training or fitness discipline"
    },

    "MessageHierarchy": {
      "primary_message": "Running after work is a social reset that restores your energy and reclaims your social identity — not a fitness obligation",
      "secondary_messages": [
        "You do not need to be fast, fit, or athletic — Nike Chill Run Club is for everyone",
        "Nike running gear is what you wear when you reclaim your evening",
        "Hong Kong's night cityscape is the backdrop of your after-work reset"
      ],
      "offer_message": "Join Nike Chill Run Club — connect with peers, run at your own pace, and try the latest Nike Pegasus running shoes"
    },

    "AudienceContext": {
      "primary_audience": "Gen Z Hong Kong working professionals, approximately aged 22–30, who currently do not run regularly and do not identify as runners or fitness people",
      "secondary_audience": "Young HK professionals who run occasionally but lack a social running community to make it a consistent part of their life",
      "core_motivation": "Reclaim personal time and social identity beyond their work role; connect with peers in a low-pressure, non-performative social context after work",
      "primary_barrier": "Post-work exhaustion convinces them that any physical or social demand after office hours is one more thing being asked of them — they believe they do not have the energy"
    },

    "OfferDefinition": {
      "offer_type": "Community Event Access",
      "offer_value": "Access to Nike Chill Run Club group runs; opportunity to try the latest Nike Pegasus running shoes in a social setting",
      "call_to_action": "Click link to learn more about Nike Chill Run Club activities and sign up"
    },

    "OfferRole": {
      "priority": "Secondary",
      "visibility_requirement": "Optional"
    },

    "ChannelContext": {
      "primary_channel": "Instagram",
      "placement_type": "Feed post — organic social media"
    },

    "ChannelBehavior": {
      "attention_window": "Short",
      "interaction_model": "Passive",
      "placement_context": "Instagram feed — competing with lifestyle content from peers and brands; must stop scroll within the first second; Cantonese copy overlay will be added in post-production"
    },

    "CampaignConstraints": {

      "MessageConstraints": {
        "required_messages": {
          "tokens": ["Mental Reset", "Social Activity", "After Work", "Chill Run Club"],
          "custom": [
            "Running is accessible and low-pressure — not competitive or achievement-oriented",
            "Cantonese market relevance is required — HK working professional cultural context",
            "The campaign speaks to people who do not currently identify as runners"
          ]
        },
        "forbidden_messages": {
          "tokens": ["Elite performance", "Competitive running", "Speed achievement", "Fitness transformation"],
          "custom": [
            "Do not communicate fitness obligation, athletic standard, or running skill requirement",
            "Do not position Nike Chill Run Club as a training program or performance improvement product"
          ]
        }
      },

      "BrandConstraints": {
        "required_brand_elements": {
          "tokens": ["Nike Swoosh", "Nike branding visible on subjects' apparel"],
          "custom": [
            "Nike running gear (shoes and/or apparel) worn by subjects in image",
            "Brand presence must feel natural to the scene — not a product placement overlay"
          ]
        },
        "forbidden_positioning": {
          "tokens": ["Exclusive", "Elite", "Intimidating", "Aspirational fitness body"],
          "custom": [
            "Do not position Nike as a performance brand in this campaign — position as a lifestyle and community brand"
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
          "Bottom 20% of frame: reserved for Nike Chill Run Club CTA and membership information overlay (post-production)",
          "No critical visual information — faces, brand elements, key action — may appear in these reserved zones"
        ]
      }
    },

    "MandatoryRequirements": {
      "required_assets": [
        "Group of HK Gen Z subjects wearing Nike running gear",
        "Hong Kong outdoor environment (waterfront, urban park, or city path setting)"
      ],
      "required_copy": [
        "Cantonese headline copy added in post-production (not embedded in generated image)",
        "Nike Chill Run Club name or brand reference visible in post-production overlay"
      ],
      "required_branding": [
        "Nike Swoosh or Nike wordmark visible on at least one subject's apparel in the generated image"
      ]
    },

    "CampaignPriority": {
      "primary_objective": "Increase Nike brand awareness among non-running Gen Z HK working professionals",
      "primary_message": "Running after work is a social reset — low-pressure, enjoyable, and for people like you",
      "primary_offer": "Join Nike Chill Run Club",
      "primary_constraint": "Must not communicate athletic pressure, competitive performance, fitness gatekeeping, or any form of exclusive running culture"
    }

  }
}
```

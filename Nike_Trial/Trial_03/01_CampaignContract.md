# Campaign Contract
**Brand:** Nike
**Campaign:** Nike Chill Run Club
**Framework:** Campaign Brief v1.1
**Stage:** 1 — Campaign Definition

---

```json
{
  "CampaignContract": {

    "BusinessObjective": {
      "objective_type": "Brand Awareness",
      "success_metric": "Increase brand awareness and desirability for Nike among Gen Z working professionals in HK who currently do not run"
    },

    "CampaignTheme": {
      "theme_token": "Mental Reset",
      "theme_description": "Running is not sport — it is a social escape valve. After a long HK workday, running with friends is how you transition from drained office mode to person-who-owns-the-city mode."
    },

    "MessageHierarchy": {
      "primary_message": "Running is how you mentally reset after work — and it's better with people",
      "secondary_messages": [
        "You don't need to be fast or athletic. You just need to show up.",
        "The city at night belongs to people who choose to move through it."
      ],
      "offer_message": "Nike Chill Run Club — join the run, reclaim your evening"
    },

    "AudienceContext": {
      "primary_audience": "Gen Z working professionals in Hong Kong, approximately 22–30 years old, currently non-runners — experiencing chronic post-work exhaustion and OT culture; social identity defined largely by work demands",
      "secondary_audience": "Gen Z HK residents who run occasionally but have not found a social running community",
      "core_motivation": "Reclaiming personal time and social connection outside of work identity — wanting to be the main character of their own life, not just an office worker surviving the week",
      "primary_barrier": "Perception that running requires athletic ability, is solitary, or is one more obligation layered onto an already exhausting day"
    },

    "OfferDefinition": {
      "offer_type": "Community Event / Club",
      "offer_value": "Nike Chill Run Club — a social running group for beginners and non-runners; entry tips, peer community, Nike gear trial opportunities",
      "call_to_action": "Join the Chill Run Club — click the link to learn more and register"
    },

    "OfferRole": {
      "priority": "Supporting",
      "visibility_requirement": "Optional"
    },

    "ChannelContext": {
      "primary_channel": "Instagram",
      "placement_type": "Feed post — 4:5 vertical format"
    },

    "ChannelBehavior": {
      "attention_window": "Short",
      "interaction_model": "Passive",
      "placement_context": "Social feed scroll — must earn attention within 2 seconds of thumb pause; emotional resonance must land before any information registers"
    },

    "CampaignConstraints": {
      "MessageConstraints": {
        "required_messages": {
          "tokens": ["CHILL_RUN_CLUB", "MENTAL_RESET"],
          "custom": []
        },
        "forbidden_messages": {
          "tokens": ["ELITE_PERFORMANCE", "SPEED", "COMPETITION"],
          "custom": [
            "No messaging that implies running requires athletic ability or speed",
            "No before/after fitness transformation framing",
            "No race or competition framing of any kind"
          ]
        }
      },
      "BrandConstraints": {
        "required_brand_elements": {
          "tokens": ["NIKE_SWOOSH"],
          "custom": ["Nike brand presence visible on subjects' gear or shoes"]
        },
        "forbidden_positioning": {
          "tokens": ["PRODUCT_HERO_COMPOSITION"],
          "custom": [
            "Running must not read as elite or exclusionary",
            "Ad must feel socially accessible to a non-runner"
          ]
        }
      },
      "LegalConstraints": { "tokens": [], "custom": [] },
      "PlatformConstraints": {
        "tokens": ["INSTAGRAM_SAFE_ZONES"],
        "custom": ["Top 10% and bottom 20% of frame reserved for copy overlay in post-production"]
      }
    },

    "MandatoryRequirements": {
      "required_assets": [
        "Reference portrait of user (entity_01) — attached for facial identity preservation"
      ],
      "required_copy": [],
      "required_branding": ["Nike Swoosh or wordmark visible on at least one subject's gear or shoes"],
      "required_subjects": [
        "entity_01: user (male subject — reference image provided)",
        "entity_02: Karina from aespa (named public figure — no reference image)"
      ],

      "ProductSpec": [
        {
          "product_name": "Nike Air Zoom Alphafly NEXT% 3",
          "product_category": "running shoe",
          "colorway": "University Red / Black / White",
          "key_visual_identifiers": [
            "sole profile: extremely tall ZoomX foam midsole in white — the midsole dominates the shoe's side profile; two large circular Air Zoom pods visible through a transparent window at the forefoot outsole; the twin pods are the shoe's most visually distinctive feature and must be legible in profile",
            "upper construction: thin, minimal Flyknit upper in University Red — lightweight and form-fitting, very low visual bulk; the upper sits narrower than the wide midsole base",
            "silhouette: high heel-to-forefoot stack with pronounced rocker toe geometry — the toe curves upward aggressively when viewed from the lateral side profile; a dramatically futuristic, almost sculpted silhouette",
            "brand mark: Nike Swoosh on the lateral side — standard curved proportions at mid-foot placement, against the red upper"
          ],
          "visibility_requirement": "Required",
          "visibility_notes": "At least one shoe in mid-stride lateral profile showing the full midsole stack and the two forefoot Air Zoom pod windows — these are the shoe's visual identity. Midsole height and pod windows must be readable at mid-frame scale."
        }
      ]
    },

    "CampaignPriority": {
      "primary_objective": "Brand awareness for Nike Chill Run Club among Gen Z HK professionals",
      "primary_message": "Running is a social Mental Reset — not sport, not obligation",
      "primary_offer": "Nike Chill Run Club community event",
      "primary_constraint": "Must feel accessible, social, and non-competitive at first scroll impression"
    }

  }
}
```

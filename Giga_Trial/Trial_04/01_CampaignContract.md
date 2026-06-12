# Campaign Contract
**Brand:** GigaSports
**Campaign:** Gigasports Pickle Club Community
**Framework:** Campaign Brief v1.0
**Stage:** 1 — Campaign Definition

---

```json
{
  "CampaignContract": {
    "BusinessObjective": {
      "objective_type": "Membership Growth",
      "success_metric": "Membership registrations for Gigasports Pickle Club Community — tracked via registration link clicks and sign-ups"
    },
    "CampaignTheme": {
      "theme_token": "Active Networking",
      "theme_description": "Pickleball as the modern social infrastructure for Hong Kong young professionals — an easy, social sport that replaces obligatory networking with genuine human connection"
    },
    "MessageHierarchy": {
      "primary_message": "Pickleball at GigaSports is where Hong Kong young professionals build a real social circle",
      "secondary_messages": [
        "No experience needed — the sport is easy to start",
        "GigaSports is the home of this community"
      ],
      "offer_message": "Join the Gigasports Pickle Club Community — register for membership now"
    },
    "AudienceContext": {
      "primary_audience": "Urban Hong Kong professionals aged 25-40, middle-to-high income, screen-fatigued and socially efficiency-seeking",
      "secondary_audience": "Fitness-adjacent adults in HK interested in social activities with a low athletic barrier",
      "core_motivation": "Authentic social connection — real friendships built through shared experience, not transactional professional networking",
      "primary_barrier": "Perceives sport as requiring athletic competence before social participation is possible"
    },
    "OfferDefinition": {
      "offer_type": "Community Membership Registration",
      "offer_value": "Access to Gigasports Pickle Club — courts, coaching, and a ready-made social community",
      "call_to_action": "立即報名會員 — Register for Membership"
    },
    "OfferRole": {
      "priority": "Secondary",
      "visibility_requirement": "Required"
    },
    "ChannelContext": {
      "primary_channel": "Instagram",
      "placement_type": "Feed Post (4:5 vertical)"
    },
    "ChannelBehavior": {
      "attention_window": "Short",
      "interaction_model": "Passive",
      "placement_context": "Lifestyle and fitness content feed — scroll-stop required within 1-2 seconds; Cantonese copy and CTA applied as text overlay in post-production"
    },
    "CampaignConstraints": {
      "MessageConstraints": {
        "required_messages": {
          "tokens": ["community", "accessible", "social_sport"],
          "custom": ["Pickleball framed as social activity, not athletic training or competition"]
        },
        "forbidden_messages": {
          "tokens": ["elite", "competitive_performance", "exclusive"],
          "custom": [
            "No framing that implies high athletic barrier to entry",
            "No solo individual achievement",
            "No transactional networking language"
          ]
        }
      },
      "BrandConstraints": {
        "required_brand_elements": {
          "tokens": ["GigaSports_logo"],
          "custom": ["GigaSports logo must be visible in the image — reference image provided"]
        },
        "forbidden_positioning": {
          "tokens": ["pure_retail", "product_forward"],
          "custom": ["Brand appears as community host, not retailer — no product-first layout"]
        }
      },
      "LegalConstraints": {
        "tokens": [],
        "custom": ["Hong Kong market context required — no non-HK cultural or location references"]
      },
      "PlatformConstraints": {
        "tokens": ["instagram_safe_zones"],
        "custom": [
          "Top 10% of frame reserved for potential UI overlays",
          "Bottom 20% of frame reserved for Cantonese copy and membership CTA overlay"
        ]
      }
    },
    "MandatoryRequirements": {
      "required_assets": ["GigaSports logo (reference image provided)"],
      "required_copy": ["Cantonese membership CTA applied as overlay in bottom safe zone — post-production"],
      "required_branding": ["GigaSports logo legible in image — must be reproduced from reference asset, not generated from training data"]
    },
    "CampaignPriority": {
      "primary_objective": "Drive membership registration for Gigasports Pickle Club Community",
      "primary_message": "Pickleball at GigaSports is where young HK professionals build a genuine social life",
      "primary_offer": "Join the Pickle Club Community — register now",
      "primary_constraint": "GigaSports logo must appear in image; community-first human framing required; no elite or competitive positioning"
    }
  }
}
```

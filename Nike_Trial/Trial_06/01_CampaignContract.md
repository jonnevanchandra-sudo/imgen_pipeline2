# Campaign Contract — Nike Chill Run Club (v1.1)

Source: `Nike Social Media Brief.md`
Framework: 1.1 Campaign_Brief.md (extends v1.0, adds ProductSpec)

```json
{
  "CampaignContract": {

    "BusinessObjective": {
      "objective_type": "Product Awareness",
      "success_metric": "Increased brand awareness and social engagement (saves, shares, comments) among Gen Z HK working professionals who currently do not run; click-throughs to Chill Run Club sign-up"
    },

    "CampaignTheme": {
      "theme_token": "Nike Chill Run Club — Mental Reset",
      "theme_description": "Reframes running as a low-pressure, social, after-work decompression ritual rather than a competitive athletic pursuit, set against Hong Kong's night skyline."
    },

    "MessageHierarchy": {
      "primary_message": "Running with Nike Chill Run Club is a relaxed way to reset after work — not a race.",
      "secondary_messages": [
        "You don't need to be fast or experienced to join.",
        "It's a social activity — meet new people while you de-stress.",
        "Hong Kong's night skyline becomes your personal backdrop — you're the main character."
      ],
      "offer_message": "Click the link to learn more about Nike Chill Run Club and how to join."
    },

    "AudienceContext": {
      "primary_audience": "Gen Z working professionals in Hong Kong (roughly early-to-mid 20s) who do not currently run, often working long hours including overtime",
      "secondary_audience": "Casual or lapsed runners looking for a low-pressure social running community",
      "core_motivation": "Desire to decompress after a draining workday and to feel a sense of social belonging and personal agency (\"main character\" moment)",
      "primary_barrier": "Perception that running is exhausting, competitive, or only for serious athletes — and that there's no energy left for it after work"
    },

    "OfferDefinition": {
      "offer_type": "Community running club participation / event invitation",
      "offer_value": "Free entry-level run sessions with beginner-friendly tips and the chance to try the latest Nike running shoes",
      "call_to_action": "Click the link to learn more about Nike Chill Run Club and registration details"
    },

    "OfferRole": {
      "priority": "Secondary",
      "visibility_requirement": "Optional"
    },

    "ChannelContext": {
      "primary_channel": "Instagram (Nike HK social media)",
      "placement_type": "Organic social media feed post (single image + Cantonese caption)"
    },

    "ChannelBehavior": {
      "attention_window": "Short",
      "interaction_model": "Passive",
      "placement_context": "Scroll-feed social post; image must communicate the campaign idea within a glance, caption provides supporting context"
    },

    "CampaignConstraints": {
      "MessageConstraints": {
        "required_messages": {
          "tokens": ["Mental Reset", "Social / Inclusive", "No Pressure to Perform"],
          "custom": []
        },
        "forbidden_messages": {
          "tokens": ["Competitive Racing", "Elite Performance Pressure"],
          "custom": ["Do not frame running as a grueling or punishing activity"]
        }
      },
      "BrandConstraints": {
        "required_brand_elements": {
          "tokens": ["Swoosh Logo"],
          "custom": ["Nike running footwear visible in lifestyle context"]
        },
        "forbidden_positioning": {
          "tokens": ["Elitist", "Intimidating"],
          "custom": ["Do not position the club as exclusive or only for serious runners"]
        }
      },
      "LegalConstraints": { "tokens": [], "custom": [] },
      "PlatformConstraints": { "tokens": ["Instagram feed post"], "custom": ["Image must read clearly at small mobile thumbnail size"] }
    },

    "MandatoryRequirements": {

      "required_assets": [
        "Hong Kong night skyline / urban waterfront setting",
        "Group of diverse Gen Z professionals in transition from office wear to running gear"
      ],
      "required_copy": [],
      "required_branding": ["Nike Swoosh logo, used sparingly and prominently"],

      "ProductSpec": [
        {
          "product_name": "Nike Pegasus 41",
          "product_category": "running shoe",
          "colorway": "",
          "key_visual_identifiers": [
            "thick React foam midsole with visible crash rail along the lateral edge",
            "engineered mesh upper with Flywire cable overlays at midfoot",
            "moderate heel stack with slight heel-to-toe drop and padded heel collar",
            "lateral Swoosh in a contrasting tone on the mesh upper, standard proportions"
          ],
          "visibility_requirement": "Required",
          "visibility_notes": "Full shoe silhouette visible on at least one subject in the lower frame as the group moves; Swoosh must remain legible at the image's medium camera distance"
        }
      ]
    },

    "CampaignPriority": {
      "primary_objective": "Build brand awareness among non-running Gen Z HK professionals by reframing running as social decompression",
      "primary_message": "Running with Nike Chill Run Club is a relaxed, social Mental Reset — not a race",
      "primary_offer": "Join Nike Chill Run Club (link in caption)",
      "primary_constraint": "Must not visually communicate competitive or elite athletic pressure"
    }
  }
}
```

---

## Notes on ProductSpec Inclusion

The brief's Visual Direction Suggestions explicitly name "Nike Pegasus" as the product to showcase. Per Campaign Brief v1.1 rules, a named product model with distinctive design merits a `ProductSpec` entry with explicit visual descriptors (model name alone is unreliable for image generators). Colorway is left unmandated (empty string) — the brief does not specify a colorway, so this remains a flexible attribute for downstream Scene Assembly.

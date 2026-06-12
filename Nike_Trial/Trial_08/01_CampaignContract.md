# Campaign Contract — Nike Chill Run Club (Stage 1.1)

Framework: `1.1 Campaign_Brief.md` (v1.1 — adds ProductSpec to MandatoryRequirements)
Input: User-supplied brief (Nike Chill Run Club, Idea 2) — Campaign Overview + Visual Direction Suggestions
Run note: ProductSpec is populated because the Visual Direction Suggestions explicitly call for "the latest Nike running gear (e.g. Nike Pegasus) in a lifestyle context." Per v1.1 rules, the model name is anchored with explicit visual identifiers — the name alone is unreliable for image generators. Strategic reasoning, creative ideas, and execution suggestions from the brief have been stripped; only normalized campaign facts remain. Both candidate locations from the brief (Central Harbourfront / West Kowloon Cultural District) are retained as `required_assets` options — Scene Assembly resolves the specific choice.

```json
{
  "CampaignContract": {

    "BusinessObjective": {
      "objective_type": "Brand Awareness",
      "success_metric": "Increase brand awareness and consideration for Nike among busy Gen Z working professionals in Hong Kong who currently do not run; secondary signal = Chill Run Club engagement/sign-up"
    },

    "CampaignTheme": {
      "theme_token": "ChillRunClub",
      "theme_description": "Running reframed as a 'Mental Reset' and a social activity rather than a grueling sport — Nike Chill Run Club (Idea 2)."
    },

    "MessageHierarchy": {
      "primary_message": "Running is a way to mentally reset and socially recharge after work — not a competitive performance.",
      "secondary_messages": [
        "You don't need to be fast or experienced — all paces and beginners are welcome.",
        "It's a social, inclusive activity done with friends, in the city, after work.",
        "After work, you stop being an office worker and become the main character of your own life."
      ],
      "offer_message": null
    },

    "AudienceContext": {
      "primary_audience": "Hong Kong Gen Z working professionals who currently do not run",
      "secondary_audience": "Running beginners and people looking for a relaxed way to meet new friends",
      "core_motivation": "Mental reset, stress relief, social connection, and a feeling of agency / being the protagonist of their own life",
      "primary_barrier": "Perception that running is exhausting, competitive, or only for fit/fast people; post-work fatigue and low energy"
    },

    "OfferDefinition": {
      "offer_type": null,
      "offer_value": null,
      "call_to_action": null
    },

    "OfferRole": {
      "priority": "Not specified",
      "visibility_requirement": "Not applicable"
    },

    "ChannelContext": {
      "primary_channel": "Social media (Nike HK)",
      "placement_type": "In-feed social post (image)"
    },

    "ChannelBehavior": {
      "attention_window": "Short",
      "interaction_model": "Passive",
      "placement_context": "Scrolled feed; image must communicate before any caption is read"
    },

    "CampaignConstraints": {
      "MessageConstraints": {
        "required_messages": {
          "tokens": ["MentalReset", "Social", "BeginnerFriendly", "MainCharacter"],
          "custom": [
            "Must read as relaxed and inclusive, not competitive",
            "Pace and skill are not the point — comfort, energy, and enjoyment are",
            "Must show a visible transition from 'office mode' (tired) to 'run mode' (vibrant, social)"
          ]
        },
        "forbidden_messages": {
          "tokens": ["CompetitiveRacing", "ElitePerformance", "SpeedPressure"],
          "custom": [
            "Do not frame running as grueling, fast, or a test of fitness",
            "Do not imply the audience must already be fit"
          ]
        }
      },
      "BrandConstraints": {
        "required_brand_elements": {
          "tokens": ["Swoosh", "NikeRunningFootwear"],
          "custom": ["Nike branding present but restrained, per brand restraint norms"]
        },
        "forbidden_positioning": {
          "tokens": ["ProductHero", "HardSell"],
          "custom": ["Product must not become the hero over the human/social story"]
        }
      },
      "LegalConstraints": {
        "tokens": [],
        "custom": ["No competitor brands or trademarks visible"]
      },
      "PlatformConstraints": {
        "tokens": ["SocialFeed"],
        "custom": [
          "Composition must survive feed UI and caption overlays",
          "Format suited to feed (square or vertical crop)"
        ]
      }
    },

    "MandatoryRequirements": {

      "required_assets": [
        "Group of diverse Gen Z Hong Kong professionals, shown transitioning from 'office mode' to 'run mode'",
        "Iconic Hong Kong night scenery — Central Harbourfront or West Kowloon Cultural District"
      ],
      "required_copy": [],
      "required_branding": ["Nike Swoosh visible but restrained"],

      "ProductSpec": [
        {
          "product_name": "Nike Pegasus (latest generation, e.g. Pegasus 41)",
          "product_category": "running shoe",
          "colorway": null,
          "key_visual_identifiers": [
            "engineered mesh upper with visible Flywire cable overlays at the midfoot",
            "thick responsive foam midsole with a visible crash rail along the lateral edge",
            "moderately stacked heel with a padded heel collar and slight heel-to-toe drop",
            "lateral Swoosh in a contrasting tone, standard proportions, legible at medium camera distance"
          ],
          "visibility_requirement": "Optional",
          "visibility_notes": "Full shoe silhouette visible in the lower frame as subjects move; brand mark readable at medium camera distance. Shoe appears in a worn, lifestyle context — never as an isolated studio product shot."
        }
      ]
    },

    "CampaignPriority": {
      "primary_objective": "Brand Awareness — grow Nike awareness among non-running HK Gen Z professionals",
      "primary_message": "Running is a relaxed mental reset and social activity, framed through a high-energy 'Main Character' transition from office to evening",
      "primary_offer": null,
      "primary_constraint": "Must read as relaxed, inclusive, and social — never competitive or performance-pressured"
    }
  }
}
```

---

## Validation Register

- **ObjectiveDefined:** TRUE — Brand Awareness.
- **MessageDefined:** TRUE — Mental Reset / social / Main Character transition, non-competitive.
- **AudienceDefined:** TRUE — HK Gen Z working professionals who don't run.
- **ChannelDefined:** TRUE — social feed, in-feed image post.
- **ConstraintsDefined:** TRUE.
- **ProductSpecDefined:** TRUE — Nike Pegasus with visual identifiers; colorway omitted (not mandated).
- **BoundaryProtected:** TRUE — no strategy, narrative, visual, or execution decisions included.

# Strategy Contract — Nike Chill Run Club (Stage 2)

Framework: 2. Strategy.md v5.0
Inputs: BrandContract (Stage 0), CampaignContract (Stage 1.1)

```json
{
  "StrategyContract": {

    "StrategicObjective": {
      "business_objective": "Increase brand awareness for Nike among Gen Z HK working professionals who currently do not run, by driving engagement with Nike Chill Run Club",
      "strategic_goal": "Make running feel like an accessible, low-stakes act of self-reclamation at the end of a workday — lowering the psychological barrier to a first run"
    },

    "ActivatedDimensions": [
      {
        "dimension": "Accessibility",
        "priority": "Critical",
        "source_anchors": "BrandContract.CoreTensions: Accessibility ↔ Elite Aspiration — this campaign activates the accessibility pole to reach non-runners"
      },
      {
        "dimension": "Transformation",
        "priority": "Critical",
        "source_anchors": "BrandContract.StrategicImplications: 'Personal transformation narratives align strongly with Nike' (0.92)"
      },
      {
        "dimension": "Belonging",
        "priority": "High",
        "source_anchors": "BrandContract.RecurringPatterns: Community Representation (High frequency); Inferences: 'Community is positioned as part of achievement' (0.87)"
      },
      {
        "dimension": "Confidence",
        "priority": "Medium",
        "source_anchors": "BrandContract.BrandIdentity.Personality: Confident, Inspirational"
      }
    ],

    "ContextualTensions": [
      {
        "current_state": "Mentally and physically depleted after a long Hong Kong workday, with no energy left for structured exercise",
        "desired_state": "Lightly re-energized and socially connected, having claimed a small piece of the evening for themselves",
        "tension_type": "psychological",
        "priority": "Critical"
      },
      {
        "current_state": "Believes running is a solitary, demanding pursuit reserved for 'real runners'",
        "desired_state": "Sees running as something approachable they can do casually with friends, no performance expectation",
        "tension_type": "cultural",
        "priority": "High"
      }
    ],

    "BehavioralPositioning": {
      "audience_role": "The exhausted professional who assumes they have nothing left to give at the end of the day",
      "brand_role": "The low-pressure social enabler that reframes a small, achievable action as a meaningful evening reset",
      "behavioral_frame": "Running as Evening Reclamation — a social, unhurried act of taking back a few minutes of the day for oneself",
      "operational_utility": "Free, beginner-friendly group run sessions paired with the chance to try new Nike running shoes, lowering both the social and equipment barriers to a first run"
    },

    "IdentityMigration": {
      "departure_identity": "Depleted Office Worker",
      "arrival_identity": "Evening Main Character — socially present, lightly energized, on their own terms",
      "migration_vector": "activation",
      "behavioral_shift": "From going straight home to collapse, to joining a casual group run along the harbourfront with friends or new acquaintances",
      "primary_barrier": "The belief that running requires energy, skill, or seriousness the audience does not currently have",
      "activation_trigger": "Seeing people who look like them — ordinary, tired-after-work Gen Z professionals — casually enjoying a run as a social moment, not a workout"
    },

    "StrategicDirection": {
      "theme_token": "Reclaim the Evening",
      "strategic_focus": "Activating accessibility and belonging to lower the psychological barrier to a first run, framed as a social Mental Reset rather than exercise",
      "audience_takeaway": "This isn't a workout I have to be ready for — it's a way to feel like myself again at the end of the day, with people like me."
    },

    "StrategicPriority": {
      "primary_dimension": "Accessibility",
      "primary_tension": "Depleted after work ↔ Lightly re-energized and socially connected",
      "primary_behavioral_shift": "From going home to collapse, to joining a casual social run",
      "primary_takeaway": "This is for me, even if I've never run before."
    },

    "MeaningConstraints": {
      "required_meaning": {
        "primary_token": "Accessible Mental Reset",
        "secondary_tokens": ["Social Belonging", "Evening Reclamation"]
      },
      "forbidden_meaning": {
        "primary_token": "Competitive Performance",
        "secondary_tokens": ["Elite Athleticism", "Grueling Effort"]
      },
      "required_tensions": {
        "primary_token": "Depleted ↔ Lightly Re-energized",
        "secondary_tokens": ["Solitary Habit ↔ Shared Activity"]
      },
      "forbidden_resolutions": {
        "primary_token": "Resolution through competitive achievement or athletic dominance",
        "secondary_tokens": ["Resolution through solo performance milestones"]
      }
    },

    "StrategicConstraints": {
      "required_dimensions": {
        "primary_token": "Accessibility",
        "secondary_tokens": ["Belonging", "Transformation"]
      },
      "protected_brand_truths": {
        "primary_token": "Identity before product",
        "secondary_tokens": ["Show don't tell", "Authenticity over spectacle", "Human-first hierarchy"],
        "source_anchors": ["BrandContract.CommunicationPhilosophy", "BrandContract.CreativeTradeoffs", "BrandContract.SacredBrandAssets"]
      },
      "forbidden_positioning": {
        "primary_token": "Elitist or intimidating athletic positioning",
        "secondary_tokens": ["Exclusionary club imagery", "Hyper-competitive framing"]
      },
      "brand_integrity_rules": {
        "primary_token": "Maintain human-centric, identity-driven communication with restrained, editorial visual language",
        "secondary_tokens": ["Preserve diverse, community-oriented subject representation", "Preserve naturalistic realism and controlled color palette"]
      }
    }
  }
}
```

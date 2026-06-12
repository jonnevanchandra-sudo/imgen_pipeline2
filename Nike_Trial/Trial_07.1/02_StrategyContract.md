# Strategy Contract — Nike Chill Run Club (Stage 2)

Framework: `2. Strategy.md` v5.0
Inputs: BrandContract (Stage 0) + CampaignContract (Stage 1.1)
Decision Type: Meaning Selection — which brand truths to activate for this campaign. No narrative, visual, scene, or rendering decisions are made here.

```json
{
  "StrategyContract": {

    "StrategicObjective": {
      "business_objective": "Grow Nike awareness and consideration among busy HK Gen Z professionals who currently do not run.",
      "strategic_goal": "Reframe running from an intimidating performance sport into an accessible, social form of mental recovery — so non-runners feel invited rather than judged."
    },

    "ActivatedDimensions": [
      {
        "dimension": "Community",
        "priority": "Critical",
        "source_anchors": "BrandContract Core Tension 'Individual Achievement ↔ Community Belonging' (0.90); Recurring Pattern 'Community Representation'; Inference 'Community is positioned as part of achievement' (0.87)"
      },
      {
        "dimension": "Accessibility",
        "priority": "Critical",
        "source_anchors": "BrandContract Core Tension 'Accessibility ↔ Elite Aspiration' (0.88); Communication Philosophy 'Low CTA aggressiveness, identity-driven'"
      },
      {
        "dimension": "Transformation",
        "priority": "High",
        "source_anchors": "BrandContract Emotional Role 'catalyst for self-transformation'; Sacred Narrative Asset 'Personal transformation'; Creative Summary 'Become the person you are capable of becoming'"
      },
      {
        "dimension": "Confidence",
        "priority": "Medium",
        "source_anchors": "BrandContract Personality 'Confident'; Audience Aspiration 'More confident'; Confidence Style 'quiet, earned'"
      }
    ],

    "ContextualTensions": [
      {
        "current_state": "Drained, depleted office worker after long OT hours — wants only to collapse",
        "desired_state": "Recharged, present individual who has reclaimed their evening on their own terms",
        "tension_type": "psychological",
        "priority": "Critical"
      },
      {
        "current_state": "Sees running as grueling, competitive, and only for the already-fit",
        "desired_state": "Sees running as a relaxed, low-stakes social activity anyone can join",
        "tension_type": "cultural",
        "priority": "High"
      },
      {
        "current_state": "Isolated / socially flat after a transactional workday",
        "desired_state": "Connected to a welcoming group of peers",
        "tension_type": "psychological",
        "priority": "High"
      }
    ],

    "BehavioralPositioning": {
      "audience_role": "A peer joining friends — not an athlete being tested",
      "brand_role": "Host and enabler of a low-pressure social reset, not a performance coach",
      "behavioral_frame": "Running as Mental Reset — recovery and connection through easy movement",
      "operational_utility": "A relaxed, repeatable after-work ritual that relieves stress and builds belonging, with zero fitness prerequisite"
    },

    "IdentityMigration": {
      "departure_identity": "Depleted office worker with no time or energy for themselves",
      "arrival_identity": "Main character of their own evening — calm, recharged, socially connected",
      "migration_vector": "activation",
      "behavioral_shift": "From collapsing at home after work to choosing an easy social run as a reset",
      "primary_barrier": "Belief that running is exhausting / competitive / requires fitness they don't have",
      "activation_trigger": "An open invitation from peers that promises comfort and belonging over performance"
    },

    "StrategicDirection": {
      "theme_token": "ResetTogether",
      "strategic_focus": "Accessible, social mental recovery through easy movement in the city",
      "audience_takeaway": "Running can be how I unwind and reconnect after work — and I'm welcome exactly as I am."
    },

    "StrategicPriority": {
      "primary_dimension": "Community",
      "primary_tension": "Drained office worker → recharged individual (psychological)",
      "primary_behavioral_shift": "From post-work collapse to an easy social run as a reset",
      "primary_takeaway": "Running is my mental reset, and I belong here without being fast."
    },

    "MeaningConstraints": {
      "required_meaning": {
        "primary_token": "MentalReset",
        "secondary_tokens": ["Belonging", "Accessibility", "Recharge"]
      },
      "forbidden_meaning": {
        "primary_token": "CompetitivePerformance",
        "secondary_tokens": ["SpeedPressure", "EliteFitness", "EnduranceSuffering"]
      },
      "required_tensions": {
        "primary_token": "Depleted→Recharged",
        "secondary_tokens": ["Intimidation→Invitation", "Isolation→Connection"]
      },
      "forbidden_resolutions": {
        "primary_token": "WinningTheRace",
        "secondary_tokens": ["BeatingOthers", "PersonalRecordPressure"]
      }
    },

    "StrategicConstraints": {
      "required_dimensions": {
        "primary_token": "Community",
        "secondary_tokens": ["Accessibility", "Transformation"]
      },
      "protected_brand_truths": {
        "primary_token": "IdentityBeforeProduct",
        "secondary_tokens": ["AuthenticMovement", "HumanFirstHierarchy", "QuietEarnedConfidence"],
        "source_anchors": ["Creative Summary", "Creative Tradeoff 'Identity Building dominant'", "Composition Behavior 'Human-first hierarchy'"]
      },
      "forbidden_positioning": {
        "primary_token": "ProductHero",
        "secondary_tokens": ["HardSell", "PerformanceFlex"]
      },
      "brand_integrity_rules": {
        "primary_token": "RestraintOverHype",
        "secondary_tokens": ["ShowDontTell", "AuthenticityOverSpectacle"]
      }
    }
  }
}
```

---

## Compatibility Assessment

- **Aligned elements:** The campaign's social, low-pressure, mental-recovery framing maps directly onto Nike's latent Community and Accessibility dimensions and the brand's "transformation through movement" truth. No identity mutation is required.
- **Strategic tension handled:** Nike's strongest equity is Performance, but this campaign deliberately activates the *Lifestyle* and *Community* poles of the brand's own Core Tensions rather than inventing a foreign meaning. Per the Conflict Resolution Protocol, Performance is dialed *down* in amplification — not contradicted. The shoe remains genuinely a performance product; the campaign simply doesn't make performance the message.
- **Boundary check:** No narrative arc, visual concept, scene, or rendering instruction is specified here — those remain open for downstream layers.

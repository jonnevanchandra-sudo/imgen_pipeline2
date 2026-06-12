# Strategy Contract — Nike Chill Run Club (Stage 2)

Framework: `2. Strategy.md` v5.0
Inputs: BrandContract (`Nike_Trial/0. Nike_Brand_Contract.md`) + CampaignContract (Stage 1.1)
Decision Type: Meaning Selection — which brand truths to activate for this campaign. No narrative, visual, scene, or rendering decisions are made here.

```json
{
  "StrategyContract": {

    "StrategicObjective": {
      "business_objective": "Grow Nike awareness and consideration among busy HK Gen Z professionals who currently do not run.",
      "strategic_goal": "Reframe running from an intimidating performance sport into an accessible, social, energizing reset — so non-runners feel invited and excited rather than judged."
    },

    "ActivatedDimensions": [
      {
        "dimension": "Transformation",
        "priority": "Critical",
        "source_anchors": "BrandContract Emotional Role 'catalyst for self-transformation'; Sacred Narrative Asset 'Personal transformation'; Creative Summary 'Become the person you are capable of becoming' — directly maps to the brief's 'office mode → run mode' transition"
      },
      {
        "dimension": "Community",
        "priority": "Critical",
        "source_anchors": "BrandContract Core Tension 'Individual Achievement ↔ Community Belonging' (0.90); Recurring Pattern 'Community Representation'; Inference 'Community is positioned as part of achievement' (0.87)"
      },
      {
        "dimension": "Accessibility",
        "priority": "High",
        "source_anchors": "BrandContract Core Tension 'Accessibility ↔ Elite Aspiration' (0.88); Communication Philosophy 'Low CTA aggressiveness, identity-driven'"
      },
      {
        "dimension": "Confidence",
        "priority": "Medium",
        "source_anchors": "BrandContract Personality 'Confident, Energetic'; Audience Aspiration 'More confident'; supports the 'Main Character' framing in the brief's Visual Direction"
      }
    ],

    "ContextualTensions": [
      {
        "current_state": "Drained, depleted office worker at the end of a long workday — low energy, low presence",
        "desired_state": "Energized, vibrant individual who has stepped into the spotlight of their own evening",
        "tension_type": "psychological",
        "priority": "Critical"
      },
      {
        "current_state": "Sees running as grueling, competitive, and only for the already-fit",
        "desired_state": "Sees running as a relaxed, high-energy social activity anyone can join",
        "tension_type": "cultural",
        "priority": "High"
      },
      {
        "current_state": "Anonymous worker, one of many, blending into the after-work crowd",
        "desired_state": "Visible, vibrant individual at the center of a welcoming social moment",
        "tension_type": "psychological",
        "priority": "High"
      }
    ],

    "BehavioralPositioning": {
      "audience_role": "A peer stepping into their own spotlight — not an athlete being tested",
      "brand_role": "Host and stage-setter for a low-pressure, high-energy social transformation",
      "behavioral_frame": "Running as the switch that flips 'office mode' into 'main character mode'",
      "operational_utility": "A repeatable after-work ritual that converts fatigue into energy and connection, with zero fitness prerequisite"
    },

    "IdentityMigration": {
      "departure_identity": "Depleted office worker, faded into the background of the workday",
      "arrival_identity": "Vibrant main character of their own evening — energized, social, visible",
      "migration_vector": "transformation",
      "behavioral_shift": "From dragging through the commute home to choosing an easy, energizing social run that visibly switches their mode",
      "primary_barrier": "Belief that running is exhausting / competitive / requires fitness they don't have",
      "activation_trigger": "An open, low-stakes invitation from peers that promises energy and belonging over performance"
    },

    "StrategicDirection": {
      "theme_token": "MainCharacterReset",
      "strategic_focus": "A visible, high-energy transformation from depleted worker to main character, achieved through accessible social movement",
      "audience_takeaway": "Running can be the moment I switch from background character to main character — and I'm welcome exactly as I am."
    },

    "StrategicPriority": {
      "primary_dimension": "Transformation",
      "primary_tension": "Drained office worker → energized main character (psychological)",
      "primary_behavioral_shift": "From post-work fatigue to an easy social run that flips the day's mode",
      "primary_takeaway": "Running is how I become the main character of my own evening, without needing to be fast."
    },

    "MeaningConstraints": {
      "required_meaning": {
        "primary_token": "MainCharacterTransformation",
        "secondary_tokens": ["MentalReset", "Belonging", "Accessibility"]
      },
      "forbidden_meaning": {
        "primary_token": "CompetitivePerformance",
        "secondary_tokens": ["SpeedPressure", "EliteFitness", "EnduranceSuffering"]
      },
      "required_tensions": {
        "primary_token": "Depleted→Energized",
        "secondary_tokens": ["Background→Foreground", "Intimidation→Invitation"]
      },
      "forbidden_resolutions": {
        "primary_token": "WinningTheRace",
        "secondary_tokens": ["BeatingOthers", "PersonalRecordPressure"]
      }
    },

    "StrategicConstraints": {
      "required_dimensions": {
        "primary_token": "Transformation",
        "secondary_tokens": ["Community", "Accessibility"]
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

- **Aligned elements:** The brief's "office mode → run mode" / "Main Character" framing maps directly onto Nike's latent Transformation dimension and its Creative Summary ("Become the person you are capable of becoming"). Energy and visibility (the "Main Character" feeling) are a natural amplification of Nike's existing "Confident, Energetic" personality traits — no identity invention required.
- **Strategic tension handled:** As in prior runs, Nike's Performance equity is dialed *down* in amplification per the Conflict Resolution Protocol — the energy here is emotional/social ("main character energy"), not athletic performance. The shoe remains a genuine performance product; the campaign simply foregrounds transformation and community over competition.
- **Differentiation from a pure "Recovery" framing:** Where a recovery-led strategy emphasizes calm release, this run leans into the brief's explicit "high-energy, Main Character aesthetic" — Transformation is elevated to Critical priority alongside Community, with Confidence (Medium) supporting the visible-energy beat. This keeps both the relaxed/inclusive requirement and the brief's energetic visual ambition compatible.
- **Boundary check:** No narrative arc, visual concept, scene, or rendering instruction is specified here — those remain open for downstream layers.

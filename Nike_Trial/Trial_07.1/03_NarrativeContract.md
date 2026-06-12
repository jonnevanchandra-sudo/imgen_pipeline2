# Narrative Contract — Nike Chill Run Club (Stage 3)

Framework: `3. Narrative.md` v3
Inputs: BrandContract (Stage 0) + StrategyContract (Stage 2)
Decision Type: Emotional Interpretation — how the campaign meaning should be *experienced*. No visual concepts, scene layout, composition, lighting, or rendering decisions are made here.

```json
{
  "NarrativeContract": {

    "Inputs": {
      "from_strategy": {
        "strategic_direction": "ResetTogether — accessible, social mental recovery through easy movement",
        "identity_migration": "Depleted office worker → main character of their own evening (activation)",
        "behavioral_positioning": "Running as Mental Reset; brand as host, audience as peer",
        "activated_dimensions": ["Community", "Accessibility", "Transformation", "Confidence"]
      },
      "from_brand": {
        "brand_identity": "Enabler of human potential; quiet, earned confidence; identity before product",
        "audience_identity": "Wants to become more capable, confident, and connected without elite intensity"
      }
    },

    "NarrativeLensSelection": {
      "primary_lens": "Emotional Recovery",
      "lens_question": "What emotional burden is being released?",
      "category_of_meaning": "Emotional Restoration",
      "secondary_lens": "Human Connection",
      "secondary_question": "Which relationship creates meaning?",
      "secondary_category": "Relational Meaning",
      "rationale": "The campaign's core promise is releasing the weight of the workday (Emotional Recovery), and the mechanism that makes it feel safe and attainable is doing it with peers (Human Connection). These two lenses together hold the Mental Reset + social truth without drifting into performance or hero framing."
    },

    "CurrentEmotionalState": "Emotionally fatigued and depleted — the flat, heavy feeling of clocking out after a long over-worked day, wanting to shut down rather than do anything for oneself.",

    "PsychologicalFriction": "The belief that the only forms of self-care left at the end of the day are passive collapse, and that anything labeled 'running' would cost more energy than it returns — compounded by the sense that organized exercise is competitive and exposing for someone who isn't fit.",

    "DesiredTransformation": {
      "arc": "emotional fatigue → light recovery",
      "supporting_arcs": [
        "isolation → connection",
        "intimidation → ease"
      ],
      "description": "A gentle exhale: the day's tension lifting through easy movement and easy company, so the run gives energy back rather than taking it. The contrast is emotional (heavy → light), never physical (slow → fast)."
    },

    "IdentityArrival": {
      "who_the_viewer_becomes": "Calm, recharged, and quietly connected — the main character of their own evening rather than a depleted worker.",
      "qualities": ["unwound", "present", "socially at ease", "quietly confident"],
      "accessibility_note": "Aspirational but fully attainable — the arrival identity is reachable tonight, by anyone, with no fitness prerequisite."
    },

    "ViewerTakeaway": {
      "emotional_residue": "This is how I could give my evenings back to myself — and I'd be welcome exactly as I am.",
      "supporting_residue": [
        "This feels light, not grueling.",
        "I wouldn't be doing it alone."
      ]
    },

    "EmotionalIntensity": {
      "level": "Medium",
      "justification": "Lifestyle / wellness positioning with a clear, recognizable transformation calls for Medium intensity — enough emotional progression to feel meaningful, but restrained enough to stay true to Nike's high-restraint, show-don't-tell communication philosophy. Low would feel inert for a social activation; High would over-dramatize a deliberately low-stakes reset."
    },

    "HumanMeaningDomains": ["Emotional restoration", "Belonging", "Calm competence", "Modernity"],

    "CompatibilityValidation": {
      "CompatibleWithBrandIdentity": "True — releases burden and restores capability, consistent with 'enabler of human potential' without performance flexing.",
      "CompatibleWithAudienceIdentity": "True — arrival identity (recharged, connected, quietly confident) matches the audience's stated aspiration.",
      "CompatibleWithStrategicDirection": "True — directly experiences 'ResetTogether'.",
      "CompatibleWithBehavioralPositioning": "True — emotion centers on recovery + peer company, not on the act of training.",
      "CompatibleWithIdentityMigration": "True — depleted worker → main character of the evening, via activation.",
      "NoBrandContradictions": "True",
      "NoStrategicContradictions": "True",
      "EmotionalIntensityAppropriate": "True — Medium fits a wellness/lifestyle social activation."
    }
  }
}
```

---

## Anti-Pattern Check

- No fear-based manipulation, identity shaming, or trauma framing — the friction is everyday fatigue, resolved gently.
- No forced hero narrative or superiority framing — arrival is peer-level and attainable, not triumphant.
- No vague inspirational filler — every emotional beat ties back to the Mental Reset + belonging strategy.

## Boundary Check

- ✓ No visual concepts, metaphors, or symbolism prescribed (left to Art Direction).
- ✓ No subject placement, scene layout, or environment construction (left to Scene Assembly).
- ✓ No camera, lighting, color, or atmosphere instructions (left to Composition & Rendering).
- Provides emotional hierarchy and emphasis only; downstream layers organize and render it independently.

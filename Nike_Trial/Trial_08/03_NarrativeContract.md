# Narrative Contract — Nike Chill Run Club (Stage 3)

Framework: `3. Narrative.md` v3
Inputs: BrandContract (`Nike_Trial/0. Nike_Brand_Contract.md`) + StrategyContract (Stage 2)
Decision Type: Emotional Interpretation — how the campaign meaning should be *experienced*. No visual concepts, scene layout, composition, lighting, or rendering decisions are made here.

```json
{
  "NarrativeContract": {

    "Inputs": {
      "from_strategy": {
        "strategic_direction": "MainCharacterReset — a visible, high-energy transformation from depleted worker to main character through accessible social movement",
        "identity_migration": "Depleted, background office worker → vibrant main character of their own evening (transformation)",
        "behavioral_positioning": "Running as the switch from 'office mode' to 'main character mode'; brand as host and stage-setter",
        "activated_dimensions": ["Transformation", "Community", "Accessibility", "Confidence"]
      },
      "from_brand": {
        "brand_identity": "Enabler of human potential; energetic, confident, identity before product",
        "audience_identity": "Wants to become more capable, confident, and visible without elite intensity"
      }
    },

    "NarrativeLensSelection": {
      "primary_lens": "Aspirational Transformation",
      "lens_question": "Who could the viewer become?",
      "category_of_meaning": "Identity Evolution",
      "secondary_lens": "Human Connection",
      "secondary_question": "Which relationship creates meaning?",
      "secondary_category": "Relational Meaning",
      "rationale": "The brief's central beat — 'office mode' (tired) flipping into 'run mode' (vibrant, social, main character) — is fundamentally an Identity Evolution arc, so Aspirational Transformation leads. Human Connection is the secondary lens because the transformation is witnessed and shared with peers, not a solo glow-up; the group is what makes 'main character energy' feel safe and attainable rather than performative."
    },

    "CurrentEmotionalState": "Emotionally fatigued and faded — the flat, depleted feeling of finishing a long workday, where the viewer feels like a background extra in their own life rather than someone the day belongs to.",

    "PsychologicalFriction": "The belief that the only thing left after work is to disappear into the couch, and that anything labeled 'running' would cost energy rather than give it back — compounded by a quiet fear that organized exercise is competitive, exposing, and not for someone who isn't already 'a runner.'",

    "DesiredTransformation": {
      "arc": "depleted/background → energized/foreground",
      "supporting_arcs": [
        "isolation → connection",
        "intimidation → ease"
      ],
      "description": "A switch-flip: the day's flatness lifting into a burst of energy and visibility, so the run hands energy back rather than draining it. The contrast is emotional and identity-based (faded → vivid, background → main character), never physical (slow → fast)."
    },

    "IdentityArrival": {
      "who_the_viewer_becomes": "Energized, vivid, and socially confident — the main character of their own evening rather than a depleted background figure.",
      "qualities": ["recharged", "visible", "socially at ease", "quietly confident"],
      "accessibility_note": "Aspirational but fully attainable — the arrival identity is reachable tonight, by anyone, with no fitness prerequisite."
    },

    "ViewerTakeaway": {
      "emotional_residue": "This is how I flip the switch from background to main character — and I'd be doing it with people, not alone.",
      "supporting_residue": [
        "This feels energizing, not grueling.",
        "I wouldn't be doing it alone.",
        "This feels like my evening, on my terms."
      ]
    },

    "EmotionalIntensity": {
      "level": "Medium",
      "justification": "The 'main character' transformation calls for clear, recognizable emotional progression — more than the subtle implication of Low intensity — but Nike's high-restraint, show-don't-tell communication philosophy and the campaign's deliberately low-stakes, non-competitive framing rule out High intensity. Medium delivers a felt transformation without tipping into mythic or cinematic over-dramatization."
    },

    "HumanMeaningDomains": ["Personal transformation", "Confidence", "Belonging", "Modernity"],

    "CompatibilityValidation": {
      "CompatibleWithBrandIdentity": "True — energized self-transformation through movement, consistent with 'enabler of human potential' and Nike's energetic personality, without performance flexing.",
      "CompatibleWithAudienceIdentity": "True — arrival identity (energized, visible, confident) matches the audience's stated aspiration to become more confident and capable.",
      "CompatibleWithStrategicDirection": "True — directly experiences 'MainCharacterReset'.",
      "CompatibleWithBehavioralPositioning": "True — emotion centers on the office-to-evening switch plus peer company, not on the act of training.",
      "CompatibleWithIdentityMigration": "True — depleted/background worker → vibrant main character, via transformation.",
      "NoBrandContradictions": "True",
      "NoStrategicContradictions": "True",
      "EmotionalIntensityAppropriate": "True — Medium fits a lifestyle transformation activation."
    }
  }
}
```

---

## Anti-Pattern Check

- No fear-based manipulation, identity shaming, or trauma framing — the friction is everyday fatigue and social anxiety about exercise, resolved gently through peer invitation.
- No forced hero narrative or superiority framing — arrival is energized and visible, but peer-level and attainable, not triumphant or dominant.
- No vague inspirational filler — every emotional beat ties back to the office-mode → main-character transformation and belonging.

## Boundary Check

- ✓ No visual concepts, metaphors, or symbolism prescribed (left to Art Direction).
- ✓ No subject placement, scene layout, or environment construction (left to Scene Assembly).
- ✓ No camera, lighting, color, or atmosphere instructions (left to Composition & Rendering).
- Provides emotional hierarchy and emphasis only; downstream layers organize and render it independently.

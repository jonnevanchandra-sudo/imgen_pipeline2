# Synthesis Contract — Nike Chill Run Club (Stage 7.1)

Framework: `7.1 Synthesis.md` v8.1
Inputs: Campaign (1.1), Brand (0), Strategy (2), Narrative (3), Art Direction (4), Scene (5.2.5), Composition & Rendering (6.1)
Decision Type: Communication Resolution. Synthesis consolidates, resolves, prioritizes, and preserves — it introduces NO new meaning, entities, relationships, or rendering behavior. All decisions below originate upstream.

```json
{
  "SynthesisContract": {

    "ExecutiveSummary": "A small group of diverse Hong Kong Gen Z professionals shares an easy, social evening run along a lit harbourfront promenade — the visual delivers 'running as a welcoming mental reset' through peer connection and warm relief, with the Nike Pegasus present as quiet proof rather than the hero.",

    "CommunicationResolution": {
      "PrimaryCommunication": {
        "statement": "Running is a welcoming way to mentally reset and reconnect after work — and you belong here exactly as you are.",
        "derived_from": {
          "campaign": "Reframe running as a relaxed 'Mental Reset' / social activity for non-runners",
          "brand": "Enabler of human potential; identity before product; quiet earned confidence",
          "strategy": "ResetTogether — Community + Accessibility + Transformation",
          "narrative": "Emotional fatigue → light recovery; isolation → connection",
          "art_direction": "Shared Reset — emotional safety and peer belonging as the subject"
        }
      },
      "SecondaryCommunication": [
        {
          "statement": "This is for everyone — no fitness, speed, or experience required.",
          "supports": "PrimaryCommunication",
          "priority": "High"
        },
        {
          "statement": "After work you become the main character of your own evening.",
          "supports": "PrimaryCommunication",
          "priority": "Medium"
        },
        {
          "statement": "Nike (Pegasus) is part of this easy ritual — present, not pushed.",
          "supports": "PrimaryCommunication",
          "priority": "High"
        }
      ],
      "SuppressedCommunication": [
        { "statement": "Athletic performance / speed / competition", "reason": "Contradicts the Mental Reset framing and Strategy forbidden_meaning 'CompetitivePerformance'." },
        { "statement": "Product as hero / feature sell", "reason": "Violates 'identity before product' and Strategy forbidden_positioning 'ProductHero'." },
        { "statement": "Solo hero-runner narrative", "reason": "Campaign and Scene require a peer group; belonging is the point." }
      ],
      "MemoryAnchor": {
        "statement": "The shared exhale — a group laughing mid-stride on the HK waterfront at night.",
        "justification": "A single, emotionally legible image of relief-in-company is the most memorable and most brand-true distillation of the campaign."
      }
    },

    "ObservableSignalMapping": [
      {
        "communication": "Welcoming mental reset",
        "human_signal": "Relaxed, unguarded faces; mid-laugh; loose shoulders",
        "observable_requirements": ["candid expressions, not posed to camera", "relaxed jogging pace", "non-competitive body language"],
        "Visual Evidence Examples": ["two people glancing at each other mid-laugh", "arms swinging naturally", "a blazer slung over a shoulder"],
        "allocation_priority": "MustSurvive"
      },
      {
        "communication": "You belong / inclusion",
        "human_signal": "Peer-level group interaction, equal footing",
        "observable_requirements": ["group of 4–5, mixed gender and styling", "subjects facing/engaging each other", "no leader/coach dynamic"],
        "Visual Evidence Examples": ["the group clustered loosely, talking", "diverse ages and looks within the group"],
        "allocation_priority": "MustSurvive"
      },
      {
        "communication": "Accessible, not competitive",
        "human_signal": "Easy effort, comfortable pace",
        "observable_requirements": ["conversational jogging pace", "no strained 'race faces'", "office-to-run hybrid clothing"],
        "Visual Evidence Examples": ["they could still talk while moving", "rolled sleeves, a work bag still on"],
        "allocation_priority": "PreserveWhenPossible"
      },
      {
        "communication": "Nike Pegasus present as proof",
        "human_signal": "Footwear naturally worn mid-stride",
        "observable_requirements": ["Pegasus visible in lower frame", "model visual identifiers legible", "lifestyle (worn) context not studio shot"],
        "Visual Evidence Examples": ["mesh upper with Flywire overlays, crash-rail midsole, lateral Swoosh at medium distance"],
        "allocation_priority": "PreserveWhenPossible"
      },
      {
        "communication": "Main character of the evening",
        "human_signal": "Quiet confidence, present and unhurried",
        "observable_requirements": ["subjects own the moment, not performing for camera"],
        "Visual Evidence Examples": ["a calm, self-possessed expression within the social group"],
        "allocation_priority": "SimplifyWhenConstrained"
      }
    ],

    "CommunicationAllocation": [
      {
        "component": "Welcoming mental reset (shared relief)",
        "supports": ["PrimaryCommunication"],
        "priority": "Critical",
        "survival_policy": "MustSurvive",
        "derived_from": ["Narrative", "ArtDirection"],
        "justification": "The core emotional truth; if anything else is lost this must remain."
      },
      {
        "component": "Peer belonging / inclusive group",
        "supports": ["PrimaryCommunication"],
        "priority": "Critical",
        "survival_policy": "MustSurvive",
        "derived_from": ["Strategy", "Scene"],
        "justification": "Belonging is what converts non-runners; the group (not a solo runner) is non-negotiable."
      },
      {
        "component": "Accessible / non-competitive pace",
        "supports": ["SecondaryCommunication"],
        "priority": "High",
        "survival_policy": "PreserveWhenPossible",
        "derived_from": ["Campaign", "Strategy"],
        "justification": "Removes the intimidation barrier."
      },
      {
        "component": "Nike Pegasus as quiet proof",
        "supports": ["SecondaryCommunication"],
        "priority": "High",
        "survival_policy": "PreserveWhenPossible",
        "derived_from": ["Campaign ProductSpec", "Scene PreservationContract"],
        "justification": "Mandatory product presence with correct identifiers, kept subordinate to the human signal."
      },
      {
        "component": "HK harbourfront night setting",
        "supports": ["SecondaryCommunication"],
        "priority": "Medium",
        "survival_policy": "SimplifyWhenConstrained",
        "derived_from": ["Campaign", "Scene"],
        "justification": "Place identity and 'integrated into city life'; may simplify but should read as HK."
      },
      {
        "component": "Main-character quiet confidence",
        "supports": ["SecondaryCommunication"],
        "priority": "Medium",
        "survival_policy": "SimplifyWhenConstrained",
        "derived_from": ["Narrative", "Campaign"],
        "justification": "Reinforces ownership of the evening; secondary to the shared-relief signal."
      },
      {
        "component": "Photographic style register (warm editorial)",
        "supports": ["PrimaryCommunication"],
        "priority": "Low",
        "survival_policy": "RemoveWhenConstrained",
        "derived_from": ["Brand RenderingStyle", "Composition"],
        "justification": "Aesthetic register; may be reduced under token pressure."
      }
    ],

    "ExecutionResolution": {
      "PrimaryExecutionMode": "Candid social-moment realism — a captured-not-staged group beat during an easy run",
      "SupportingExecutionModes": ["Environmental integration into a real HK night setting", "Naturally-worn product presence within the action"],
      "ExecutionRequirements": ["Multiple interacting human subjects", "Observable easy/relaxed effort", "Place legible as Hong Kong at night", "Footwear visible within natural movement"],
      "ExcludedExecutionModes": ["Studio / isolated product shot", "Posed lineup facing camera", "Competitive race depiction", "Solo hero-runner portrait"]
    },

    "HierarchyResolution": {
      "PrimaryFocus": ["entity_01 (the group's shared moment)"],
      "SecondaryFocus": ["entity_02 (Nike Pegasus)", "entity_03 (promenade)"],
      "SupportingFocus": ["entity_04 (skyline)"],
      "AttentionSequence": ["entity_01", "entity_02", "entity_03", "entity_04"]
    },

    "RenderingResolution": {

      "PerceptualRendering": {
        "EmotionalTone": "Warm relief and easy social warmth — a shared exhale, not exertion",
        "Atmosphere": "Lived-in HK evening with faint harbour haze; calm, unforced energy"
      },

      "PhysicalRendering": {
        "RealityModel": "Realistic",
        "CameraIntent": "Eye-level near-full group shot, viewer placed among the group as a peer; at least one subject's shoes enter the lower frame",
        "CameraSpecs": {
          "focal_length_mm": "35mm",
          "aperture_f_stop": "f/2.8"
        },
        "LightingIntent": "Warm directional streetlamp key on the group lifting them above a softer, cooler skyline fill; warm but skin reads natural, not orange",
        "MaterialBehavior": "Real fabric creases, non-glossy surfaces, naturally worn (not box-fresh) footwear",
        "OpticalIntent": "Progressive depth-dependent bokeh consistent with CameraSpecs — railing/near water semi-legible, far skyline soft warm circular bokeh; no flat cutout blur"
      },

      "RenderingQuality": {
        "DetailRendering": "Faces, expressions, and the Pegasus identifiers sharp and legible; background detail softened by depth",
        "TextureRendering": "Visible skin pores and fabric weave; tactile shoe and pavement surfaces",
        "LightingRendering": "Warm key with cooler ambient fill, subject-from-background separation",
        "DepthRendering": "Clear foreground/midground/background separation via focus falloff and haze",
        "CommercialRendering": "Premium editorial realism without studio polish"
      },

      "AuthenticityBehavior": {
        "HumanAuthenticityRendering": "Natural skin texture — pores, subtle tone variation, light post-workday flush; asymmetric candid expressions; nothing beauty-filtered",
        "EnvironmentalAuthenticityRendering": "Slightly uneven promenade paving, ambient light spill, faint evening haze — a real city evening, not a clean set",
        "MaterialAuthenticityRendering": "Fabric creases on jackets and bags; lightly worn shoe texture; matte, non-plastic surfaces",
        "ImperfectionRendering": "Credibility over perfection — preserve slight asymmetries in pose, expression, and styling; do not correct toward symmetry"
      }
    },

    "PreservationResolution": {
      "PreservedEntities": [
        "Group of 4–5 diverse HK Gen Z professionals interacting at peer level (NOT a solo runner)",
        "Nike Pegasus (latest generation) — model name AND visual identifiers: engineered mesh upper with Flywire overlays, thick foam midsole with visible lateral crash rail, moderately stacked padded heel, lateral contrasting Swoosh legible at medium distance"
      ],
      "PreservedContext": [
        "Hong Kong harbourfront promenade at night with skyline across water",
        "Instagram in-feed placement — safe zones must stay clear of faces, Swoosh, and the visible shoe"
      ],
      "PreservedBrandRequirements": [
        "Nike Swoosh present but restrained (no product-hero framing)",
        "Identity before product; human-first hierarchy",
        "Nike Pegasus model name + visual identifiers must reach the Prompt Compiler `brand` key in HIGH, written together (name first, identifiers following)"
      ],
      "PreservedNarrativeRequirements": [
        "Emotional read is relief/recovery and belonging — never effort or competition",
        "Aspirational-but-attainable (peer-level, reachable tonight)"
      ],
      "PreservedConstraints": [
        "No competitor brands or trademarks",
        "Composition survives Instagram UI / caption overlays",
        "Square or vertical crop for feed"
      ]
    }
  }
}
```

---

## Resolution Notes

- **No reference-asset / BRAND_ASSETS obligation** carried forward — the named-product requirement flows as a textual `brand`/HIGH instruction (model name + identifiers), not as a reference-image attachment, because no images were uploaded upstream.
- **Conflict handling:** the inherent Performance↔Lifestyle brand tension is resolved by suppression (athletic performance moved to SuppressedCommunication) rather than by introducing new meaning — consistent with Synthesis boundaries.
- Prompt Compiler can execute using only this Synthesis Contract (no Reference Asset Package required).

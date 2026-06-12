# Synthesis Contract — Nike Chill Run Club (Stage 7.1, Variant: No Lighting Hierarchy)

Framework: `7.1 Synthesis.md` v8.1
Inputs: CampaignContract (1.1) + BrandContract (0) + StrategyContract (2) + NarrativeContract (3) + ArtDirectionContract (4) + SceneContract (5.2.5) — all identical to base `Trial_08` — + **CompositionRenderingContract (6.1, Variant: No Lighting Hierarchy)** from `Variant_NoLightingHierarchy/06_CompositionRenderingContract.md`
Decision Type: Communication Resolution — consolidates all upstream contracts. Introduces no new entities, relationships, actions, environments, or rendering behavior.

**Variant note:** This is a re-run of `Trial_08/07_SynthesisContract.md` against the lighting-hierarchy-free Stage 6.1 variant. The only changes from the base Trial_08 Synthesis are inside `RenderingResolution.PhysicalRendering` and `RenderingResolution.RenderingQuality`: the `LuminanceHierarchy` array is **removed entirely** (it has no source in the variant's `HierarchyPlan`), and `LightingIntent` / `LightingRendering` are rewritten to describe the scene's lighting atmosphere without assigning a brightest/dimmest exposure ranking between entities. `CameraSpecs` (35mm, f/4) are carried verbatim, unchanged. All other sections (`CommunicationResolution`, `ObservableSignalMapping`, `CommunicationAllocation`, `ExecutionResolution`, `HierarchyResolution`, `PreservationResolution`) are unchanged from base Trial_08, since none of them depended on the luminance hierarchy.

```json
{
  "SynthesisContract": {

    "ExecutiveSummary": "A group of HK Gen Z professionals, mid-transition from office mode to run mode, move energetically across a West Kowloon waterfront plaza at night, the HK Island skyline glowing across the harbour behind them. The image communicates an accessible, social, energizing 'mode switch' — running as the moment the workday's depleted background figure becomes the vibrant main character of their own evening, with friends, no fitness required. Nike Pegasus running shoes appear naturally in the lifestyle moment without becoming the hero.",

    "CommunicationResolution": {
      "PrimaryCommunication": {
        "statement": "Running with friends after work is an energizing 'mode switch' — from depleted office worker to vibrant main character — and it's accessible to anyone, not just 'runners.'",
        "derived_from": {
          "campaign": "Required messages: MentalReset, Social, BeginnerFriendly, MainCharacter; office-mode → run-mode transition",
          "brand": "Emotional Role 'catalyst for self-transformation'; Creative Summary 'Become the person you are capable of becoming'",
          "strategy": "StrategicDirection 'MainCharacterReset' — visible, high-energy transformation via accessible social movement",
          "narrative": "DesiredTransformation 'depleted/background → energized/foreground'; IdentityArrival 'energized, visible, socially confident'",
          "art_direction": "VisualConcept 'The Mode Switch' — group caught mid-transition, office traces + run-mode energy, shared with peers"
        }
      },
      "SecondaryCommunication": [
        {
          "statement": "This is a shared, social activity — done with friends, not alone.",
          "supports": "PrimaryCommunication",
          "priority": "High"
        },
        {
          "statement": "You don't need to be fast or already fit to belong here — all paces and energy levels are welcome.",
          "supports": "PrimaryCommunication",
          "priority": "High"
        },
        {
          "statement": "Nike running gear, including the Pegasus, is a natural part of this everyday transformation.",
          "supports": "PrimaryCommunication",
          "priority": "Medium"
        },
        {
          "statement": "This is happening in a real, recognizable Hong Kong setting — the city itself is part of the energy.",
          "supports": "PrimaryCommunication",
          "priority": "Medium"
        }
      ],
      "SuppressedCommunication": [
        {
          "statement": "Athletic performance, racing, or competitive achievement",
          "reason": "Forbidden per CampaignContract MessageConstraints and StrategyContract MeaningConstraints (CompetitivePerformance, SpeedPressure, EliteFitness)"
        },
        {
          "statement": "The Nike Pegasus as the hero/subject of the image",
          "reason": "Forbidden per CampaignContract BrandConstraints (ProductHero) and ArtDirection 'what_it_is_not'"
        },
        {
          "statement": "A solo runner / individual achievement framing",
          "reason": "Conflicts with required Community/Social dimension and SubjectRelationshipLogic (Equality, shared momentum)"
        }
      ],
      "MemoryAnchor": {
        "statement": "The moment your evening becomes yours.",
        "justification": "Compresses NarrativeContract's IdentityArrival and ViewerTakeaway and ArtDirection's 'Mode Switch' concept into a single attainable, non-competitive image of self-transformation — directly supporting the Brand Awareness objective without product-hero framing."
      }
    },

    "ObservableSignalMapping": [
      {
        "communication": "Energized office-to-run mode switch",
        "human_signal": "Visible contrast within the same group/individuals between residual office-mode cues and energetic, in-motion run-mode behavior",
        "observable_requirements": [
          "At least one visible office-mode garment/accessory per subject (draped jacket, loosened tie/collar, slung tote/work bag)",
          "Activewear/running gear worn alongside the office-mode item",
          "Dynamic, in-motion body language (mid-stride, mid-turn, mid-laugh)"
        ],
        "Visual Evidence Examples": [
          "A blazer draped over one shoulder while jogging",
          "A loosened tie flying slightly with movement",
          "A tote bag worn cross-body over an athletic top"
        ],
        "allocation_priority": "Critical"
      },
      {
        "communication": "Social, peer-shared moment",
        "human_signal": "Group cohesion and mutual engagement rather than individual performance or camera-facing posing",
        "observable_requirements": [
          "Multiple subjects (4-5) moving together",
          "Subjects oriented toward or reacting to each other, not the camera",
          "Visible warmth (laughter, glances, relaxed proximity)"
        ],
        "Visual Evidence Examples": [
          "Two subjects glancing at each other mid-laugh",
          "The group moving at a conversational, side-by-side pace"
        ],
        "allocation_priority": "Critical"
      },
      {
        "communication": "Accessible, non-competitive energy",
        "human_signal": "Relaxed, varied effort levels with no competitive signifiers",
        "observable_requirements": [
          "No race bibs, timing devices, or competitive gear",
          "Mixed casual/athletic styling rather than uniform 'serious runner' kit",
          "Expressions read as enjoyment/excitement, not strain"
        ],
        "Visual Evidence Examples": [
          "An easy jog or brisk energetic walk rather than a sprint",
          "Smiling, animated faces"
        ],
        "allocation_priority": "High"
      },
      {
        "communication": "Recognizable Hong Kong night setting",
        "human_signal": "A real, identifiable HK waterfront environment frames the moment",
        "observable_requirements": [
          "Open waterfront promenade/plaza (West Kowloon character)",
          "Illuminated Hong Kong Island skyline visible across the harbour"
        ],
        "Visual Evidence Examples": [
          "Harbour railing in the midground with city lights glowing across the water"
        ],
        "allocation_priority": "High"
      },
      {
        "communication": "Nike Pegasus present in lifestyle context",
        "human_signal": "Footwear is visible as part of the moment, not as a product display",
        "observable_requirements": [
          "Pegasus visible mid-stride in the lower frame on at least one subject",
          "Model's distinguishing features (mesh upper, Flywire overlays, midsole crash rail, lateral Swoosh) legible at medium distance",
          "Worn-in appearance, not box-fresh"
        ],
        "Visual Evidence Examples": [
          "A close-but-not-isolated view of one subject's shoes mid-stride"
        ],
        "allocation_priority": "Medium"
      }
    ],

    "CommunicationAllocation": [
      {
        "component": "GroupModeSwitch",
        "supports": ["PrimaryCommunication"],
        "priority": "Critical",
        "survival_policy": "MustSurvive",
        "derived_from": ["NarrativeContract.DesiredTransformation", "ArtDirectionContract.VisualConcept"],
        "justification": "The visible office-to-run mode switch IS the campaign's central message; without it the image becomes generic lifestyle jogging."
      },
      {
        "component": "SocialCohesion",
        "supports": ["PrimaryCommunication", "SecondaryCommunication[0]"],
        "priority": "Critical",
        "survival_policy": "MustSurvive",
        "derived_from": ["StrategyContract.ActivatedDimensions[Community]", "ArtDirectionContract.SubjectRelationshipLogic"],
        "justification": "Removing the group/peer dynamic collapses the Community dimension and reframes the campaign as individual achievement, which is forbidden."
      },
      {
        "component": "AccessibleEnergy",
        "supports": ["SecondaryCommunication[1]"],
        "priority": "High",
        "survival_policy": "PreserveWhenPossible",
        "derived_from": ["CampaignContract.MessageConstraints.required_messages", "StrategyContract.MeaningConstraints"],
        "justification": "Non-competitive, beginner-friendly tone differentiates this from generic athletic advertising and is core to the Accessibility dimension."
      },
      {
        "component": "HKNightSetting",
        "supports": ["SecondaryCommunication[3]"],
        "priority": "High",
        "survival_policy": "PreserveWhenPossible",
        "derived_from": ["SceneContract.Entities[entity_03, entity_04]"],
        "justification": "A recognizable HK setting grounds the campaign locally and supports the 'city as energy source' framing, but the image still functions if the skyline is softened or partially cropped."
      },
      {
        "component": "PegasusVisibility",
        "supports": ["SecondaryCommunication[2]"],
        "priority": "Medium",
        "survival_policy": "SimplifyWhenConstrained",
        "derived_from": ["CampaignContract.MandatoryRequirements.ProductSpec"],
        "justification": "ProductSpec visibility_requirement is Optional — the shoe should appear when shown, with its identifying details intact (preservation), but its prominence may be simplified before the human/social communication is compromised."
      }
    ],

    "ExecutionResolution": {
      "PrimaryExecutionMode": "Candid, documentary-style lifestyle photography capturing a group of people mid-transition and mid-motion",
      "SupportingExecutionModes": [
        "Environmental establishing context via a real Hong Kong waterfront setting",
        "Incidental, naturally-integrated product visibility"
      ],
      "ExecutionRequirements": [
        "Multiple human subjects sharing a transitional, energized action",
        "Visible juxtaposition of office-mode and run-mode clothing/styling cues",
        "A real, recognizable Hong Kong night waterfront environment"
      ],
      "ExcludedExecutionModes": [
        "Studio or isolated product photography",
        "Posed lineup facing the camera",
        "Competitive race / finish-line imagery",
        "Solo-subject framing"
      ]
    },

    "HierarchyResolution": {
      "PrimaryFocus": ["entity_01"],
      "SecondaryFocus": ["entity_02", "entity_03"],
      "SupportingFocus": ["entity_04"],
      "AttentionSequence": ["entity_01", "entity_02", "entity_03", "entity_04"]
    },

    "RenderingResolution": {

      "PerceptualRendering": {
        "EmotionalTone": "Energized, warm, and socially alive — the relief and excitement of stepping into the evening as someone new.",
        "Atmosphere": "A vibrant Hong Kong night, alive with ambient light from the promenade and the cross-harbour skyline."
      },

      "PhysicalRendering": {
        "RealityModel": "Realistic",
        "CameraIntent": "Eye-level medium shot placing the viewer at peer height within the group, framing roughly waist/knee-up so motion and the Pegasus are visible in the lower frame, with the plaza and skyline visible beyond the group.",
        "CameraSpecs": {
          "focal_length_mm": "35mm",
          "aperture_f_stop": "f/4"
        },
        "LightingIntent": "Warm practical lighting — promenade lamps and ambient city glow — establishes the scene's nighttime atmosphere; the cross-harbour skyline contributes its own illumination as a glowing, lit backdrop. No exposure ranking is specified between the group and the environment; relative brightness is left to natural scene lighting rather than an imposed hierarchy.",
        "MaterialBehavior": "Contrast between structured office-wear textures (blazer weave, shirt collar) and technical activewear/mesh of the Pegasus; natural skin texture across all subjects.",
        "OpticalIntent": "Progressive depth falloff at 35mm/f4 — group, Pegasus, and near railing sharp; plaza surface softens slightly with distance; skyline softened but recognizable as building forms and light glow."
      },

      "RenderingQuality": {
        "DetailRendering": "High fidelity on the group, faces, clothing texture, and Pegasus details; environment rendered with progressively less fine detail with distance.",
        "TextureRendering": "Visible fabric weave on office garments, technical mesh/foam texture on the Pegasus, natural skin texture with pores and tonal variation on all subjects.",
        "LightingRendering": "Warm light from promenade lamps on the group and the plaza; the distant skyline glows with its own lit-window and signage illumination, read as a naturally lit night scene rather than a deliberately ranked exposure; soft directional shadows throughout.",
        "DepthRendering": "Layered foreground (group, shoes) → midground (plaza, railing) → background (skyline) with progressive softening, no flat cutout blur.",
        "CommercialRendering": "Editorial lifestyle photography quality — not a studio or catalog product shot."
      },

      "AuthenticityBehavior": {
        "HumanAuthenticityRendering": "Natural skin texture and asymmetric expressions on all subjects; each subject at an independent point in their stride/gesture cycle — no synchronized or mirrored poses.",
        "EnvironmentalAuthenticityRendering": "Real West Kowloon waterfront plaza details — paving texture, ambient light spill, faint cross-harbour haze.",
        "MaterialAuthenticityRendering": "Worn-in Pegasus shoes (not box-fresh); slightly creased or draped office garments in motion.",
        "ImperfectionRendering": "Candid framing and expression — slightly imperfect composition over polished, posed perfection."
      }
    },

    "PreservationResolution": {
      "PreservedEntities": [
        "entity_01 — group of 4-5 diverse HK Gen Z professionals, each showing one office-mode trace alongside Nike activewear, energized in-motion body language",
        "entity_02 — Nike Pegasus (latest generation): engineered mesh upper with Flywire overlays, foam midsole with lateral crash rail, padded heel collar, contrasting lateral Swoosh"
      ],
      "PreservedContext": [
        "West Kowloon Cultural District waterfront promenade/plaza, night",
        "Hong Kong Island skyline visible across the harbour"
      ],
      "PreservedBrandRequirements": [
        "Swoosh visible but restrained, legible at medium distance",
        "No product-hero framing",
        "No competitor brands or trademarks visible"
      ],
      "PreservedNarrativeRequirements": [
        "Visible depleted/background → energized/foreground transformation",
        "Social, peer-shared framing — no solo subject",
        "Non-competitive, accessible, beginner-welcoming tone"
      ],
      "PreservedConstraints": [
        "No race numbers, bibs, or competitive signifiers",
        "Composition must survive social feed UI and caption overlays",
        "Natural, non-airbrushed skin rendering required",
        "Independent, non-synchronized pose/gait per subject required"
      ]
    }
  }
}
```

---

## Validation

- ✓ All upstream decisions consolidated; no new entities, relationships, actions, environments, or rendering behaviors introduced.
- ✓ `CameraSpecs` (`35mm`, `f/4`) carried verbatim from CompositionRenderingContract's `CameraPlan`, kept as structured values separate from `CameraIntent` prose — unchanged from base Trial_08.
- ✓ **`LuminanceHierarchy` removed** — the variant's Stage 6.1 `HierarchyPlan` carries no `luminance_priority` per entity, so there is nothing to carry verbatim. `LightingIntent` and `LightingRendering` describe atmosphere and light sources without an exposure ranking.
- ✓ Preservation Resolution protects ProductSpec details and named-product identity through to the Prompt Compiler's `brand` key (HIGH) — unchanged.
- ✓ Ready for Prompt Compiler (8.1.1).

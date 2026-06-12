# Synthesis Contract
**Brand:** GigaSports
**Campaign:** Gigasports Pickle Club Community
**Framework:** Synthesis Framework v8.1
**Stage:** 7 — Communication Resolution

---

```json
{
  "SynthesisContract": {

    "ExecutiveSummary": "A candid lifestyle photograph of 2–3 young HK professionals at an indoor GigaSports pickleball court — one newcomer being warmly welcomed by established members. The emotional center is the newcomer's face in the micro-moment when outsider becomes insider: surprise giving way to warmth and relief. Eye-level medium shot. Shallow depth of field places the foreground welcome moment in sharp focus while the indoor venue and GigaSports brand element recede into warm readable bokeh. The image communicates: this community exists, it is warm, and you do not have to earn your way in — you just have to show up. GigaSports logo reproduced from reference_asset_01 — not generated from training data. Instagram 4:5 format with safe zones for Cantonese copy and CTA overlay.",

    "CommunicationResolution": {
      "PrimaryCommunication": {
        "statement": "Joining this community is as simple as showing up — the welcome already exists and it's available to you.",
        "derived_from": {
          "campaign": "Drive membership registration — the image must make joining feel immediate and emotionally low-risk",
          "brand": "GigaSports as sports participation enabler; community and event association as sacred brand asset",
          "strategy": "Your Real Social Life Starts Here — the community already exists; the viewer just hasn't walked in yet",
          "narrative": "Stranger → welcomed participant; belonging arrives through welcome, not through time or skill",
          "art_direction": "The Welcome — the moment someone stops being outside and starts being inside; newcomer's expression as emotional anchor"
        }
      },
      "SecondaryCommunication": [
        {
          "statement": "Pickleball is the social vehicle — easy, casual, not about athletic performance.",
          "supports": "PrimaryCommunication",
          "priority": "High"
        },
        {
          "statement": "GigaSports is where this community lives — the brand creates the context for the connection.",
          "supports": "PrimaryCommunication",
          "priority": "Medium"
        }
      ],
      "SuppressedCommunication": [
        {
          "statement": "Athletic performance and competitive achievement",
          "reason": "Contradicts the social accessibility positioning — would shift identity arrival from 'community member' to 'athlete,' raising the perceived entry barrier"
        },
        {
          "statement": "Solo individual achievement or solo subject",
          "reason": "Directly contradicts the Community dimension and the relational welcome dynamic — the welcome requires at least two subjects"
        },
        {
          "statement": "Exclusive or elite social group",
          "reason": "Contradicts Accessibility and the core conversion insight that the welcome is available to anyone who shows up"
        },
        {
          "statement": "Retail and product promotion",
          "reason": "Contradicts GigaSports' community enabler brand truth; transactional messaging undermines the belonging narrative"
        }
      ],
      "MemoryAnchor": {
        "statement": "The image a viewer would describe as: 'That GigaSports pickleball post where you could see on the person's face the exact moment they realized they belonged.'",
        "justification": "The micro-expression of welcome being received is visually distinctive and emotionally specific — it is a rarer moment to capture than general group warmth, and it encodes the conversion argument directly into a single face."
      }
    },

    "ObservableSignalMapping": [
      {
        "communication": "Welcome is immediate — belonging does not require skill or prior relationship",
        "human_signal": "The newcomer's facial expression captures the transition: tension or slight uncertainty dissolving into warmth and relief — the specific micro-expression of 'I thought I might not fit in, and I do'",
        "observable_requirements": [
          "Newcomer (entity_01) expression reads as emotionally transitional — not purely happy, not anxious, but the specific warm surprise of being received",
          "At least one established member (entity_02) is visibly directing a welcome gesture toward entity_01 — eye contact, high five, arm gesture, or open-body orientation",
          "The direction of the relational energy is clearly from entity_02 toward entity_01 — the welcome is being given, not mutually exchanged between equals"
        ],
        "Visual Evidence Examples": [
          "Newcomer mid-smile, looking at the member who just extended a hand or high five — expression just after contact",
          "One established member with arm around the newcomer's shoulder, both facing slightly toward camera, newcomer's face showing warm surprise",
          "Direct eye contact between newcomer and established member, newcomer's posture slightly open and surprised-but-pleased"
        ],
        "allocation_priority": "MustSurvive"
      },
      {
        "communication": "Pickleball as accessible social activity — sport without intimidation",
        "human_signal": "Paddles present but held casually — sport is the context, not the performance",
        "observable_requirements": [
          "Paddles visible and identifiable as pickleball paddles",
          "Paddle grip relaxed — held loosely at sides or in non-greeting hand",
          "Not raised in playing position; not posed as if about to compete",
          "Court and net visible in background confirming active venue"
        ],
        "Visual Evidence Examples": [
          "Paddle held at hip height or dangling loosely during the welcome gesture",
          "Court lines and net visible behind subjects confirming active indoor pickleball venue"
        ],
        "allocation_priority": "PreserveWhenPossible"
      },
      {
        "communication": "GigaSports as host and enabler of this community",
        "human_signal": "Brand element present in environment — legible but not dominant; brand creates the space, people create the moment",
        "observable_requirements": [
          "GigaSports logo visible on venue wall or banner in background",
          "Logo reproduced accurately from reference — wordmark, globe-O, BE PROFESSIONAL tagline all present",
          "Logo does not interrupt the primary welcome moment",
          "Logo legible through bokeh — soft but recognizable"
        ],
        "Visual Evidence Examples": [
          "GigaSports banner on venue wall behind subjects, warm and soft in bokeh but clearly branded",
          "Logo visible above or beside the net in the midground-to-background depth layer"
        ],
        "allocation_priority": "PreserveWhenPossible"
      }
    ],

    "CommunicationAllocation": [
      {
        "component": "The welcome moment — newcomer receiving genuine inclusion",
        "supports": ["PrimaryCommunication"],
        "priority": "Critical",
        "survival_policy": "MustSurvive",
        "derived_from": ["NarrativeContract", "ArtDirectionContract", "StrategyContract"],
        "justification": "This is the entire emotional argument of the campaign. If the welcome dynamic is lost — if the image reads as two friends at a court rather than a newcomer being received — the conversion message fails entirely."
      },
      {
        "component": "Pickleball sport context — paddles and court",
        "supports": ["SecondaryCommunication — accessible social sport"],
        "priority": "High",
        "survival_policy": "PreserveWhenPossible",
        "derived_from": ["CampaignContract", "SceneContract"],
        "justification": "Without sport context the image becomes generic lifestyle content. Paddles and court signal that this specific community is the pickleball club."
      },
      {
        "component": "GigaSports brand presence",
        "supports": ["SecondaryCommunication — GigaSports as host"],
        "priority": "High",
        "survival_policy": "PreserveWhenPossible",
        "derived_from": ["CampaignContract — required branding", "BrandContract — sacred brand assets", "SceneContract — entity_05 reference locked"],
        "justification": "Brand attribution required. Logo reproduced from reference_asset_01 — must remain legible through bokeh. Accurate reproduction depends on reference image being attached to the API call."
      },
      {
        "component": "Indoor sports venue atmosphere",
        "supports": ["PrimaryCommunication — scene grounding"],
        "priority": "Medium",
        "survival_policy": "SimplifyWhenConstrained",
        "derived_from": ["SceneContract", "CompositionRenderingContract"],
        "justification": "Environmental context confirms the scene as a real, active venue. May be simplified to warm atmospheric background — the court surface and net are sufficient; architectural detail may be sacrificed."
      }
    ],

    "ExecutionResolution": {
      "PrimaryExecutionMode": "Candid lifestyle photograph of a genuine welcome moment — a newcomer being received into the GigaSports pickleball community by established members. The emotional center is the newcomer's face in the transition from outsider to insider. Human connection is the subject; sport is the context; GigaSports is the host.",
      "SupportingExecutionModes": [
        "Sport equipment as passive identity signal — paddles in hand, not in play",
        "Indoor pickleball venue as atmospheric depth layer confirming the community's home",
        "Brand element integrated into venue background — reproduced from reference_asset_01, legible through bokeh"
      ],
      "ExecutionRequirements": [
        "Minimum two subjects — newcomer (entity_01) and at least one established member (entity_02)",
        "Active welcome gesture from entity_02 directed at entity_01 — the relational direction must be clearly established",
        "Newcomer expression showing the micro-moment of welcome being received",
        "Pickleball paddles present and identifiable",
        "Indoor pickleball court setting",
        "GigaSports logo legible in background — reproduced from reference_asset_01",
        "Eye-level camera perspective — viewer placed within the social space, not above it"
      ],
      "ExcludedExecutionModes": [
        "Two established friends interacting — the newcomer dynamic must be visible",
        "Active play shot — no mid-swing, no ball in frame, no competitive energy",
        "Posed group lineup facing camera — contradicts the candid welcome dynamic",
        "Solo subject — contradicts the community and welcome concept entirely",
        "Outdoor setting — contradicts the indoor GigaSports venue",
        "High athletic performance energy — contradicts accessible social positioning"
      ]
    },

    "HierarchyResolution": {
      "PrimaryFocus": [
        "entity_01 — newcomer's face and the expression of welcome being received",
        "entity_02 — established member(s) and the welcome gesture directed at entity_01"
      ],
      "SecondaryFocus": [
        "entity_03 — pickleball paddles (sport identity signal)"
      ],
      "SupportingFocus": [
        "entity_04 — indoor court and net (venue grounding)",
        "entity_05 — GigaSports logo (brand attribution)"
      ],
      "AttentionSequence": [
        "1. Newcomer face — the emotional micro-expression of belonging arriving",
        "2. Welcome gesture from established member — the relational action being extended",
        "3. Paddles in hand — sport context confirmed",
        "4. Court and net — venue grounded as indoor pickleball",
        "5. GigaSports logo — brand recognized as host"
      ]
    },

    "RenderingResolution": {

      "PerceptualRendering": {
        "EmotionalTone": "Warm, socially immediate, and quietly joyful — the emotional register of a moment of genuine welcome. Not euphoric, not performative. The warmth comes from the relational transaction, not from atmosphere alone.",
        "Atmosphere": "Indoor sports venue — active, communal, lived-in. Warm ambient light suggesting an environment that sees a lot of real social activity. Not institutional. Not polished studio."
      },

      "PhysicalRendering": {
        "RealityModel": "Realistic lifestyle photography — indistinguishable from a candid editorial photograph taken at a real GigaSports pickleball club event",
        "CameraIntent": "Eye-level medium shot at near distance. Subjects fill the frame; both faces readable at scroll speed. Camera height communicates social equality — the viewer is in the space, not observing it from above.",
        "LightingIntent": "Soft overhead ambient fill with subtle warm key on foreground subjects. Subjects slightly brighter than background. No studio lighting. No dramatic rim. Lighting reinforces hierarchy without creating artificial quality.",
        "MaterialBehavior": "Natural fabric texture and drape on athletic casual wear. Real skin texture — pores, subtle tone variation, no over-smoothing. Matte surface behavior with slight sheen variation on pickleball paddles. Material variation increases perceptual credibility.",
        "OpticalIntent": "Shallow depth of field. Both entity_01 and entity_02 faces in sharp focus simultaneously — the welcome moment requires both faces to read clearly. Background in warm natural bokeh. GigaSports logo calibrated to remain identifiable through bokeh depth."
      },

      "RenderingQuality": {
        "DetailRendering": "High on subject faces and the welcome gesture — the expression must be granular enough to read emotionally at scroll speed. Medium on paddles and immediate environment. Low on background venue — atmospheric only.",
        "TextureRendering": "Natural skin texture on both subjects — unsmoothed, photographically real. Fabric wrinkles on athletic wear. Court surface grain visible in midground.",
        "LightingRendering": "Soft, warm, indoor. No harsh shadows. No theatrical rim. No artificial fill.",
        "DepthRendering": "Clear foreground-midground-background separation. Subjects crisp; court moderate; venue and brand in warm bokeh.",
        "CommercialRendering": "Professional lifestyle editorial quality — high production value without clinical or artificially polished appearance."
      },

      "AuthenticityBehavior": {
        "HumanAuthenticityRendering": "Unposed expressions — the welcome gesture mid-motion, the newcomer's face mid-transition. No posed smiles held for camera. Natural variation in posture between subjects. Body language driven by the relational dynamic, not the lens.",
        "EnvironmentalAuthenticityRendering": "Real venue imperfections — court line wear, natural ceiling, ambient lighting inconsistency typical of indoor sports facilities. No set-like uniformity.",
        "MaterialAuthenticityRendering": "Fabric drape and wrinkle on athletic clothing. Subtle skin variation — not studio-smoothed. Paddle surface: real material texture, not rendered shine.",
        "ImperfectionRendering": "Credibility over perfection. A slightly asymmetric composition or partially obscured paddle increases believability. The image should feel photographed, not rendered."
      }
    },

    "PreservationResolution": {
      "PreservedEntities": [
        "Newcomer subject (entity_01): the micro-expression of belonging arriving — warm surprise, not generic happiness. This specific emotional register must survive all downstream execution.",
        "Established member(s) (entity_02): the welcome gesture — high five, arm gesture, or direct warm eye contact — directed clearly at entity_01. Relational direction must be unambiguous.",
        "GigaSports brand element (entity_05): reproduced from reference_asset_01 (gigasports_logo.jpg) — compressed bold italic wordmark 'GigaSports', globe icon replacing the O in Sports, 'BE PROFESSIONAL' tagline in small all-caps below. All elements white. Legible through bokeh. Do not generate from training data."
      ],
      "PreservedContext": [
        "Indoor pickleball court venue — net and court markings must confirm the sport context",
        "Instagram 4:5 format (1080×1350px) — top 10% and bottom 20% reserved as text-safe zones for Cantonese copy and CTA overlay"
      ],
      "PreservedBrandRequirements": [
        "GigaSports logo: reproduce from reference_asset_01 — exact wordmark, globe-O icon, BE PROFESSIONAL tagline, all white, on banner or wall surface in venue background. Do not infer or substitute.",
        "Community and participatory brand energy — no elite, exclusive, or purely commercial framing",
        "Human subjects as primary visual element — brand always secondary"
      ],
      "PreservedNarrativeRequirements": [
        "The welcome dynamic must be legible — not a group of established friends, but a newcomer being received",
        "Relational direction: established member(s) extending welcome toward newcomer",
        "Emotional register: warm, immediate, low-key joyful — not performative, not euphoric"
      ],
      "PreservedConstraints": [
        "Cantonese copy and CTA overlay applied in post-production — no critical visual information in top 10% or bottom 20% of frame",
        "No imagery contradicting Hong Kong market context",
        "No active play: no ball in frame, no mid-swing posture, no competitive athletic body language"
      ]
    }
  }
}
```

# Synthesis Contract
**Brand:** GigaSports
**Campaign:** Gigasports Pickle Club Community
**Framework:** Synthesis Framework v8.1
**Stage:** 7 — Communication Resolution

---

```json
{
  "SynthesisContract": {

    "ExecutiveSummary": "A candid, warm lifestyle photograph of 2–3 young HK professionals sharing a genuine social moment on a pickleball court — paddles in hand between rallies, faces expressing authentic laughter or easy conversation. Eye-level medium shot. Shallow depth of field places subjects in sharp focus while the indoor sports venue and GigaSports brand element recede into warm, readable bokeh. The image communicates belonging, accessibility, and the idea that this is what a modern HK professional's social life looks like. Copy and membership CTA overlay in safe zones. GigaSports logo reproduced from reference_asset_01 — not generated from training data.",

    "CommunicationResolution": {
      "PrimaryCommunication": {
        "statement": "This is a community of people like you — active, social, accessible — and GigaSports is where it lives.",
        "derived_from": {
          "campaign": "Drive membership registrations — the image must make the community feel real and joinable",
          "brand": "GigaSports as sports participation enabler; community and event association as sacred brand asset",
          "strategy": "Active Networking — community-through-sport activation; audience takeaway: 'this is the social life I actually want'",
          "narrative": "Transactional obligation → Authentic belonging; viewer takeaway: 'these are people like me, I could belong here'",
          "art_direction": "Social Encouragement in Motion — candid between-play social moment; perceptual meaning: 'this feels socially welcoming'"
        }
      },
      "SecondaryCommunication": [
        {
          "statement": "Pickleball is the sport — easy, social, no experience required.",
          "supports": "PrimaryCommunication",
          "priority": "High"
        },
        {
          "statement": "GigaSports is the host of this community — the brand makes this possible.",
          "supports": "PrimaryCommunication",
          "priority": "Medium"
        }
      ],
      "SuppressedCommunication": [
        {
          "statement": "Athletic performance and competitive achievement",
          "reason": "Contradicts social-first, accessible positioning — would shift identity arrival from 'community member' to 'athlete'"
        },
        {
          "statement": "Retail and product promotion",
          "reason": "Contradicts GigaSports' community enabler brand truth; transactional messaging undermines belonging narrative"
        },
        {
          "statement": "Solo individual heroism",
          "reason": "Directly contradicts Community activated dimension and the group social dynamic"
        }
      ],
      "MemoryAnchor": {
        "statement": "The image a viewer would describe as: 'That pickleball post where the group of young professionals looked like they were genuinely having fun.'",
        "justification": "Candid social warmth in a sport context is visually distinctive within both the pickleball category and the broader HK fitness/lifestyle advertising landscape."
      }
    },

    "ObservableSignalMapping": [
      {
        "communication": "Authentic social belonging",
        "human_signal": "Spontaneous body language between subjects — laughter, easy gesture, eye contact communicating comfort and genuine enjoyment",
        "observable_requirements": [
          "At least two subjects visibly interacting (not both looking at camera)",
          "Facial expressions that read as unposed — open mouth laughter, mid-sentence expression, or relaxed smile",
          "Physical proximity communicating social comfort, not formal distance"
        ],
        "Visual Evidence Examples": [
          "One subject laughing while the other reacts — moment after a missed shot or funny exchange",
          "Two people mid-conversation with paddles at their sides, court visible behind them",
          "A celebratory gesture (fist bump, high five) captured mid-motion"
        ],
        "allocation_priority": "MustSurvive"
      },
      {
        "communication": "Pickleball as accessible social activity",
        "human_signal": "Sport equipment present but held in a casual, non-aggressive way — 'in between playing' not 'about to compete'",
        "observable_requirements": [
          "Paddles visible and identifiable as pickleball paddles",
          "Paddle grip relaxed — at side, held loosely, not raised in playing position",
          "Court and net visible in background confirming venue context"
        ],
        "Visual Evidence Examples": [
          "Paddle held at hip height with relaxed grip during conversation",
          "Court lines and net visible behind subjects confirming active venue"
        ],
        "allocation_priority": "PreserveWhenPossible"
      },
      {
        "communication": "GigaSports as host and enabler of this community",
        "human_signal": "Brand element present in environment — legible but not dominant",
        "observable_requirements": [
          "GigaSports logo visible in venue background on banner or wall",
          "Brand element does not interrupt primary social moment",
          "Logo reproduced accurately from reference — wordmark, globe-O, BE PROFESSIONAL tagline all present"
        ],
        "Visual Evidence Examples": [
          "GigaSports banner on venue wall behind subjects, soft in bokeh but recognizable",
          "Branded court perimeter marking visible in midground"
        ],
        "allocation_priority": "PreserveWhenPossible"
      }
    ],

    "CommunicationAllocation": [
      {
        "component": "Authentic social belonging — subject group interaction",
        "supports": ["PrimaryCommunication"],
        "priority": "Critical",
        "survival_policy": "MustSurvive",
        "derived_from": ["NarrativeContract", "ArtDirectionContract", "StrategyContract"],
        "justification": "Primary communication. If social dynamic is lost, the image fails the campaign objective entirely."
      },
      {
        "component": "Pickleball sport context — paddles and court",
        "supports": ["SecondaryCommunication — pickleball as accessible social activity"],
        "priority": "High",
        "survival_policy": "PreserveWhenPossible",
        "derived_from": ["CampaignContract", "SceneContract"],
        "justification": "Without sport context the image becomes generic lifestyle content. Paddles and court must be visible but may simplify in detail."
      },
      {
        "component": "GigaSports brand presence",
        "supports": ["SecondaryCommunication — GigaSports as host"],
        "priority": "High",
        "survival_policy": "PreserveWhenPossible",
        "derived_from": ["CampaignContract — required branding", "BrandContract — sacred brand assets", "ImageAnalysisContract — asset_01"],
        "justification": "Brand attribution required. Logo reproduced from reference_asset_01 — must remain legible through bokeh. Accurate reproduction depends on reference image being attached to the API call."
      },
      {
        "component": "Indoor sports venue environment",
        "supports": ["PrimaryCommunication — scene grounding"],
        "priority": "Medium",
        "survival_policy": "SimplifyWhenConstrained",
        "derived_from": ["SceneContract", "CompositionRenderingContract"],
        "justification": "Environmental context supports scene credibility. May be simplified to atmospheric background."
      }
    ],

    "ExecutionResolution": {
      "PrimaryExecutionMode": "Candid social lifestyle photography — a genuine between-play interaction moment among a group of young HK professionals on a pickleball court. Human connection is the subject; sport is the context.",
      "SupportingExecutionModes": [
        "Sport equipment as passive identity signal — paddles in hand, not in play",
        "Indoor venue environment as atmospheric depth layer",
        "Brand element integrated naturally into venue background — reproduced from reference_asset_01"
      ],
      "ExecutionRequirements": [
        "Multiple human subjects in visible social interaction (minimum 2)",
        "Pickleball court setting (indoor venue)",
        "Paddles present and identifiable",
        "GigaSports logo legible in background — reproduced from reference_asset_01",
        "Eye-level camera perspective",
        "Subjects in foreground with sufficient facial readability"
      ],
      "ExcludedExecutionModes": [
        "Solo subject — contradicts community concept",
        "Active play shot (mid-swing, ball in frame) — shifts register from social to athletic",
        "Posed formal group photography — contradicts candid social dynamic",
        "Product-forward layout — contradicts human-first hierarchy",
        "Outdoor setting — contradicts indoor venue continuity",
        "High-intensity athletic energy — contradicts Ease and Modern Freedom narrative lenses"
      ]
    },

    "HierarchyResolution": {
      "PrimaryFocus": ["entity_01 — subject group faces and social interaction dynamic"],
      "SecondaryFocus": ["entity_02 — pickleball paddles (sport identity)", "entity_03 — court and net (venue context)"],
      "SupportingFocus": ["entity_05 — GigaSports brand element (background, bokeh)", "entity_04 — venue environment"],
      "AttentionSequence": [
        "1. Subject group faces and expressed social emotion",
        "2. Paddles in hand (sport context confirmed)",
        "3. Court and net (venue grounded)",
        "4. GigaSports brand element (brand recognized)",
        "5. Venue environment (scene settled)"
      ]
    },

    "RenderingResolution": {

      "PerceptualRendering": {
        "EmotionalTone": "Warm, socially energized, and low-key — the emotional register of a group genuinely enjoying time together in an active setting. Comfortable, inclusive, inviting.",
        "Atmosphere": "Indoor sports venue with warm ambient light — active and communal, not institutional or competitive."
      },

      "PhysicalRendering": {
        "RealityModel": "Realistic lifestyle photography — indistinguishable from a candid editorial photograph taken at an actual GigaSports pickleball club event",
        "CameraIntent": "Eye-level medium shot at near distance — subjects fill the frame, facial expressions clearly readable, camera height communicates equality",
        "LightingIntent": "Soft warm indoor venue lighting — overhead ambient fill with subtle directional key. Subjects slightly brighter than background without artificial studio feel.",
        "MaterialBehavior": "Subtle fabric texture on athletic casual wear, matte surface behavior on pickleball paddles, textured court surface. Material variation increases perceptual credibility.",
        "OpticalIntent": "Shallow depth of field — subjects in sharp focus, background in natural warm bokeh. Bokeh calibrated so GigaSports logo remains identifiable."
      },

      "RenderingQuality": {
        "DetailRendering": "High on subject faces, expressions, and hands. Medium on equipment and immediate environment. Low on background — atmospheric.",
        "TextureRendering": "Tactile fabric texture on clothing. Natural skin texture — no over-smoothing. Court surface grain visible.",
        "LightingRendering": "Soft, natural, warm. No harsh shadows. No dramatic rim lighting or cinematic contrast.",
        "DepthRendering": "Clear foreground-midground-background separation. Subjects crisp; court moderate; venue and brand soft.",
        "CommercialRendering": "Professional lifestyle editorial quality — high production value, not clinical or artificial."
      },

      "AuthenticityBehavior": {
        "HumanAuthenticityRendering": "Natural unposed expressions — laughter mid-moment, conversation mid-word, gesture mid-motion. Natural variation in posture between subjects.",
        "EnvironmentalAuthenticityRendering": "Real venue imperfections — court line wear, natural ceiling, ambient lighting inconsistency typical of indoor sports venues.",
        "MaterialAuthenticityRendering": "Fabric wrinkles and natural drape on athletic wear. Slight sheen variation on paddle surfaces.",
        "ImperfectionRendering": "Authenticity over perfection. A slightly asymmetric composition or partially obscured face increases believability."
      }
    },

    "PreservationResolution": {
      "PreservedEntities": [
        "Subject group (entity_01): 2–3 young HK professionals aged 25–35 in candid social interaction — facial expressions, body language, and social dynamic must survive all downstream execution",
        "GigaSports brand element (entity_05): Reproduced from reference_asset_01 (gigasports_logo.jpg) — wordmark, globe icon replacing O, and BE PROFESSIONAL tagline must all be present and legible. May be soft in bokeh but must be recognizable. Do not generate from training data."
      ],
      "PreservedContext": [
        "Indoor pickleball court venue setting",
        "Instagram 4:5 format (1080×1350) — top 10% and bottom 20% reserved as text-safe zones"
      ],
      "PreservedBrandRequirements": [
        "GigaSports logo: reproduce from reference_asset_01 — exact wordmark, globe-O icon, BE PROFESSIONAL tagline, white on banner/wall surface. Do not infer or substitute.",
        "Community and participatory brand energy — no elite, exclusive, or purely commercial framing",
        "Athlete-centric visual hierarchy — human subjects as primary element"
      ],
      "PreservedNarrativeRequirements": [
        "Candid between-play social moment — not active athletic performance",
        "Group interaction required — no solo subject",
        "Emotional register: warm, socially welcoming, accessible"
      ],
      "PreservedConstraints": [
        "Cantonese copy overlay in safe zones — no critical visual information in top 10% or bottom 20% of frame",
        "Membership registration CTA must be accommodated in bottom safe zone",
        "No imagery contradicting Hong Kong market context"
      ]
    }
  }
}
```

# Synthesis Contract
**Brand:** GigaSports
**Campaign:** Gigasports Pickle Club Community
**Framework:** Synthesis Framework v8.1
**Stage:** 7 — Communication Resolution

---

```json
{
  "SynthesisContract": {

    "ExecutiveSummary": "A candid, warm lifestyle photograph of 2–3 young HK professionals sharing a genuine social moment on a pickleball court — paddles in hand between rallies, faces expressing authentic laughter or easy conversation. Eye-level medium shot. Shallow depth of field places subjects in sharp focus while the indoor sports venue and GigaSports brand element recede into warm, readable bokeh. The image communicates belonging, accessibility, and the idea that this is what a modern HK professional's social life looks like. Copy and membership CTA overlay in safe zones.",

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
          "reason": "Contradicts the social-first, accessible positioning; would shift identity arrival from 'community member' to 'athlete'"
        },
        {
          "statement": "Retail and product promotion",
          "reason": "Contradicts GigaSports' community enabler brand truth for this campaign; transactional messaging undermines belonging narrative"
        },
        {
          "statement": "Solo individual heroism",
          "reason": "Directly contradicts the Community activated dimension and the group social dynamic required by the visual concept"
        }
      ],
      "MemoryAnchor": {
        "statement": "The image a viewer would describe as: 'That pickleball post where the group of young professionals looked like they were genuinely having fun.'",
        "justification": "Candid social warmth in a sport context is visually distinctive within both the pickleball category and the broader HK fitness/lifestyle advertising landscape. The specific combination of professional-looking subjects, casual sport equipment, and genuine (not performed) social interaction is the memorability anchor."
      }
    },

    "ObservableSignalMapping": [
      {
        "communication": "Authentic social belonging",
        "human_signal": "Spontaneous body language between subjects — laughter, easy gesture, eye contact that communicates comfort and genuine enjoyment",
        "observable_requirements": [
          "At least two subjects visibly interacting (not both looking at camera)",
          "Facial expressions that read as unposed — open mouth laughter, mid-sentence expression, or relaxed smile rather than directed smiling at lens",
          "Physical proximity that communicates social comfort, not formal distance"
        ],
        "Visual Evidence Examples": [
          "One subject laughing while the other reacts — moment immediately after a missed shot or funny exchange",
          "Two people mid-conversation with paddles at their sides, court visible behind them",
          "A celebratory gesture (fist bump, high five) captured mid-motion between players"
        ],
        "allocation_priority": "MustSurvive"
      },
      {
        "communication": "Pickleball as accessible social activity",
        "human_signal": "Sport equipment present but held in a casual, non-aggressive way that reads as 'in between playing' not 'about to compete'",
        "observable_requirements": [
          "Paddles visible and identifiable as pickleball paddles",
          "Paddle grip is relaxed — at side, held loosely, not raised in playing position",
          "Court and net visible in background to confirm venue context"
        ],
        "Visual Evidence Examples": [
          "Paddle held at hip height with relaxed grip during social conversation",
          "Paddle resting on shoulder while laughing",
          "Court lines and net visible behind subjects confirming active venue"
        ],
        "allocation_priority": "PreserveWhenPossible"
      },
      {
        "communication": "GigaSports as host and enabler of this community",
        "human_signal": "Brand element present in environment — legible but not dominant",
        "observable_requirements": [
          "GigaSports logo or branded signage visible in venue background",
          "Brand element does not interrupt or compete with primary social moment",
          "Brand presence feels like it belongs to the venue — not like a stamped overlay"
        ],
        "Visual Evidence Examples": [
          "GigaSports banner on venue wall behind subjects, soft in bokeh but readable",
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
        "justification": "This is the primary communication. If the social dynamic is lost, the image fails the campaign objective entirely. No other element compensates for its absence."
      },
      {
        "component": "Pickleball sport context — paddles and court",
        "supports": ["SecondaryCommunication — pickleball as accessible social activity"],
        "priority": "High",
        "survival_policy": "PreserveWhenPossible",
        "derived_from": ["CampaignContract", "SceneContract"],
        "justification": "Without sport context the image becomes generic lifestyle content and loses its campaign specificity. Paddles and court must remain visible but may be simplified in detail when attention is constrained."
      },
      {
        "component": "GigaSports brand presence",
        "supports": ["SecondaryCommunication — GigaSports as host"],
        "priority": "High",
        "survival_policy": "PreserveWhenPossible",
        "derived_from": ["CampaignContract — required branding", "BrandContract — sacred brand assets"],
        "justification": "Brand attribution is required for campaign effectiveness. Must remain legible. May be rendered soft (in bokeh) as long as recognizability is maintained."
      },
      {
        "component": "Indoor sports venue environment",
        "supports": ["PrimaryCommunication — scene grounding"],
        "priority": "Medium",
        "survival_policy": "SimplifyWhenConstrained",
        "derived_from": ["SceneContract", "CompositionRenderingContract"],
        "justification": "Environmental context supports scene credibility and emotional warmth. May be simplified to ambient background with minimal detail when attention must be concentrated on primary communication."
      }
    ],

    "ExecutionResolution": {
      "PrimaryExecutionMode": "Candid social lifestyle photography — a genuine between-play interaction moment among a group of young HK professionals on a pickleball court. Human connection is the subject; sport is the context.",
      "SupportingExecutionModes": [
        "Sport equipment as passive identity signal — paddles in hand, not in play",
        "Indoor venue environment as atmospheric depth layer",
        "Brand element integrated naturally into venue background"
      ],
      "ExecutionRequirements": [
        "Multiple human subjects in visible social interaction (minimum 2)",
        "Pickleball court setting (indoor venue)",
        "Paddles present and identifiable",
        "GigaSports brand element legible in background",
        "Eye-level camera perspective",
        "Subjects in foreground with sufficient facial readability"
      ],
      "ExcludedExecutionModes": [
        "Solo subject — contradicts community concept",
        "Active play shot (mid-swing, ball in frame) — shifts register from social to athletic performance",
        "Posed formal group photography — contradicts candid social dynamic requirement",
        "Product-forward layout (equipment as hero) — contradicts human-first hierarchy",
        "Outdoor setting — contradicts indoor venue environmental continuity",
        "High-intensity athletic energy — contradicts Ease and Modern Freedom narrative lenses"
      ]
    },

    "HierarchyResolution": {
      "PrimaryFocus": ["entity_01 — subject group faces and social interaction dynamic"],
      "SecondaryFocus": ["entity_02 — pickleball paddles (sport identity)", "entity_03 — court and net (venue context)"],
      "SupportingFocus": ["entity_05 — GigaSports brand element", "entity_04 — venue environment"],
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
        "EmotionalTone": "Warm, socially energized, and low-key — the emotional register of a group of people genuinely enjoying time together in an active setting. Not excited, not intense. Comfortable, inclusive, and inviting.",
        "Atmosphere": "Indoor sports venue with warm ambient light — the environment should feel active and communal, not institutional or competitive. A sense of energy without aggression."
      },

      "PhysicalRendering": {
        "RealityModel": "Realistic lifestyle photography — the image should be indistinguishable from a candid editorial photograph taken at an actual GigaSports pickleball club event",
        "CameraIntent": "Eye-level medium shot at near distance — subjects fill the frame with enough body language visible to read social dynamic; facial expressions clearly readable; camera height communicates equality with subjects, not observation from above or below",
        "LightingIntent": "Soft warm indoor venue lighting — overhead ambient fill with subtle directional key that separates subjects from background without creating theatrical contrast. Subjects slightly brighter than background to preserve hierarchy without artificial studio feel.",
        "MaterialBehavior": "Subtle fabric texture on athletic casual wear, matte surface behavior on pickleball paddles, textured court surface visible underfoot. Material variation should increase perceptual credibility and prevent the image reading as digitally rendered.",
        "OpticalIntent": "Shallow depth of field — subject group in sharp focus, background venue and brand element in natural, warm bokeh. Bokeh calibrated so GigaSports brand element remains identifiable despite being out of focus."
      },

      "RenderingQuality": {
        "DetailRendering": "High detail on subject group faces, expressions, and hands. Medium detail on equipment and immediate environment. Low detail on background venue elements — atmospheric rather than architectural.",
        "TextureRendering": "Tactile fabric texture on clothing. Natural skin texture on faces — no over-smoothing or idealized skin rendering. Court surface grain visible.",
        "LightingRendering": "Soft, natural, warm. No harsh shadows. No dramatic rim lighting or cinematic contrast. Venue overhead lighting with warm color temperature.",
        "DepthRendering": "Clear foreground-midground-background separation through depth of field and mild atmospheric perspective. Subjects in crisp foreground; court in moderate focus midground; venue and brand in warm soft background.",
        "CommercialRendering": "Professional lifestyle editorial quality — high production value but not clinical or artificial. The image should look like it was taken by a skilled lifestyle photographer at a real event, not produced in a studio."
      },

      "AuthenticityBehavior": {
        "HumanAuthenticityRendering": "Natural, unposed expressions — laughter mid-moment, conversation mid-word, gesture mid-motion. Natural variation in posture, weight distribution, and engagement between subjects. Avoid symmetry, formality, or held poses.",
        "EnvironmentalAuthenticityRendering": "Real venue imperfections — court line wear, natural ceiling structure, ambient lighting inconsistency typical of indoor sports venues. Environment should feel used and active, not pristine and empty.",
        "MaterialAuthenticityRendering": "Fabric wrinkles and natural drape on athletic wear. Slight sheen variation on paddle surfaces. Court surface texture from use. No hyper-polished material perfection.",
        "ImperfectionRendering": "Authenticity takes priority over perfection. A slightly asymmetric composition, a partially obscured face, a motion blur on a hand — these increase credibility and distinguish the image from generic commercial stock photography."
      }
    },

    "PreservationResolution": {
      "PreservedEntities": [
        "Subject group (entity_01): 2–3 young HK professionals aged 25–35 in candid social interaction — facial expressions, body language, and social dynamic must survive all downstream execution",
        "GigaSports brand element (entity_05): Logo or branded signage must remain legible in background — may be soft in bokeh but must be recognizable"
      ],
      "PreservedContext": [
        "Indoor pickleball court venue setting — all elements must remain coherent with an active indoor sports community facility",
        "Instagram 4:5 format (1080×1350) — top 10% and bottom 20% reserved as text-safe zones for copy and CTA overlay"
      ],
      "PreservedBrandRequirements": [
        "GigaSports brand element present and legible",
        "Community and participatory brand energy — no elite, exclusive, or purely commercial framing",
        "Athlete-centric visual hierarchy (human subjects as primary element)"
      ],
      "PreservedNarrativeRequirements": [
        "Candid between-play social moment — not active athletic performance",
        "Group interaction required — no solo subject",
        "Emotional register: warm, socially welcoming, accessible — not intense, competitive, or aspirational-distant"
      ],
      "PreservedConstraints": [
        "Cantonese copy overlay in safe zones — image composition must not place critical visual information in top 10% or bottom 20% of frame",
        "Membership registration CTA must be accommodated in bottom safe zone",
        "No imagery contradicting Hong Kong market context"
      ]
    }
  }
}
```

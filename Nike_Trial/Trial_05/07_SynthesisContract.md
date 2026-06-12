# Synthesis Contract
**Brand:** Nike
**Campaign:** Nike Chill Run Club
**Framework:** Synthesis Framework v8.1 (7.1)
**Stage:** 7 — Communication Resolution

---

```json
{
  "SynthesisContract": {

    "ExecutiveSummary": "A golden hour lifestyle photograph of two runners — Karina (from aespa) and the user (reference_asset_01) — caught mid-stride in synchronized parallel motion on a Hong Kong waterfront path. Their expressions carry the specific ease of present-state liberation: faces in motion, fully out of the workday, neither performing for the camera nor for each other. Nike Novablast 5 in Volt / Black / White visible mid-stride on both subjects' feet — the ZOOMX midsole profile and Volt Swoosh legible at medium camera distance. Camera positioned at slightly below eye level at a 30–45 degree angle to subjects, shot on a 50mm lens at f/2.8, framing from head to shoe in a medium-full shot — both subjects and the shoe sharp, the HK harbor falling into progressively soft, warm bokeh behind them. Both subjects' skin renders with natural pore texture and a light running sheen — not airbrushed. Instagram 4:5 format with safe zones for Cantonese copy overlay. Entity_01 (the user) reproduced from reference_asset_01 — face and build from reference image, not generated from training data.",

    "CommunicationResolution": {
      "PrimaryCommunication": {
        "statement": "Your body already knows how to leave the day behind — you just have to start moving. The Novablast 5 is what that liberation feels like underfoot.",
        "derived_from": {
          "campaign": "Nike Novablast 5 product awareness — the shoe is the vehicle for the mental reset, not just the setting",
          "brand": "Nike as enabler of human potential; movement as identity signal; editorial photography language",
          "strategy": "Individual Agency and Kinesthetic Freedom activated — parallel liberation, not social performance",
          "narrative": "Kinesthetic Liberation (primary) + Present State Revelation (secondary) — the body has solved the problem the viewer hasn't started yet",
          "art_direction": "'In Stride' — two runners in synchronized parallel motion; shoe mid-stride as product and narrative argument simultaneously"
        }
      },
      "SecondaryCommunication": [
        {
          "statement": "Hong Kong's golden hour belongs to the people who came to run. The city gives itself to people in motion.",
          "supports": "PrimaryCommunication",
          "priority": "High"
        },
        {
          "statement": "Nike Chill Run Club is where people like Karina and the user spend their post-work hour. You could too.",
          "supports": "PrimaryCommunication",
          "priority": "Medium"
        }
      ],
      "SuppressedCommunication": [
        {
          "statement": "Athletic performance and competitive running",
          "reason": "Contradicts the kinesthetic liberation positioning — would shift identity arrival from 'person who found motion' to 'athlete in training,' raising the perceived barrier for the non-running target audience"
        },
        {
          "statement": "Social performance and group warmth",
          "reason": "Already executed in Trial 1. Repeating the social energy register would reduce differentiation and redundantly communicate the same CRC brief. This execution must carry a different emotional argument."
        },
        {
          "statement": "Fitness transformation and body aspiration",
          "reason": "Directly contradicts Nike's brief constraint: do not position as a fitness brand in this campaign. Body-forward framing alienates the non-running audience and shifts the narrative from liberation to obligation."
        },
        {
          "statement": "Product hero — shoe as the sole visual subject",
          "reason": "Contradicts Nike's brand truth (human-first hierarchy) and the emotional narrative. The shoe participates in the liberation; it does not replace it."
        },
        {
          "statement": "Polished, retouched, or AI-perfect skin rendering",
          "reason": "Composition & Rendering v6.1 mandates natural skin texture for any human subject — over-smoothed skin is the most common 'AI-look' tell and would undercut the editorial-photography reality model."
        }
      ],
      "MemoryAnchor": {
        "statement": "The image a viewer would describe as: 'That Nike post with Karina and that guy running at golden hour in Hong Kong — they looked like they had left the entire work week behind with one stride. And the shoes were really sick.'",
        "justification": "The dual anchor — the subjects' expression of liberation AND the visual distinctiveness of the Novablast 5 in Volt / Black / White mid-stride at golden hour — creates a memory trace that serves both the brand narrative and the product awareness objective simultaneously."
      }
    },

    "ObservableSignalMapping": [
      {
        "communication": "Kinesthetic Liberation — the body has left the workday behind",
        "human_signal": "Facial expression on both subjects: no tension in brow or jaw, eyes forward and slightly open, the specific quality of a face that is processing nothing except the sensation of motion — not performing, not communicating, just moving",
        "observable_requirements": [
          "Both entity_01 and entity_02 faces visible and readable at scroll speed",
          "Expression on both faces: present-state ease — not smile, not effort, not social performance",
          "Body posture mid-stride: natural running form with no athletic intensity or competitive urgency",
          "Neither subject looks at the other or at the camera — both face forward in the direction of motion"
        ],
        "Visual Evidence Examples": [
          "Slightly parted lips consistent with elevated breathing from running — not a posed smile, not a grimace",
          "Eyes forward with a slightly unfocused quality — looking at the horizon, not at a social target",
          "Shoulders relaxed despite running motion — no raised or tense shoulders suggesting effort or exertion"
        ],
        "allocation_priority": "MustSurvive"
      },
      {
        "communication": "Nike Novablast 5 as the physical vehicle of liberation — what the feeling is underfoot",
        "human_signal": "The shoe is visible mid-stride — the ZOOMX midsole in full profile, the Volt Swoosh against the black upper, the convex bounce silhouette communicating springiness before the viewer reads the model name",
        "observable_requirements": [
          "At least one Novablast 5 in full lateral ZOOMX midsole profile visible mid-stride",
          "Volt Swoosh clearly legible against black upper",
          "Rounded midsole bottom profile visible — the shoe's visual identity is the midsole, not the upper",
          "Volt outsole pods visible on white midsole base at full stride"
        ],
        "Visual Evidence Examples": [
          "Leading foot fully extended mid-stride with the lateral midsole silhouette fully visible — the rounded convex bottom, the layered midsole sidewall texture",
          "The Volt Swoosh catching golden hour sidelight — warm golden reflection on the yellow-green Swoosh against black mesh"
        ],
        "allocation_priority": "MustSurvive"
      },
      {
        "communication": "Hong Kong as the city where reclaimed time happens",
        "human_signal": "The warm golden atmospheric haze of the HK harbor visible behind the subjects — the city giving itself over to people in motion at this hour",
        "observable_requirements": [
          "HK waterfront or harbor-adjacent environment legible in background",
          "Golden hour light quality unmistakable — warm directional light at low sun angle",
          "Environment reads as HK specifically — not a generic park or path"
        ],
        "Visual Evidence Examples": [
          "HK harbor water and architectural silhouette visible in warm bokeh behind the running subjects",
          "Golden hour backlight creating warm rim separation on subjects against the atmospheric background"
        ],
        "allocation_priority": "PreserveWhenPossible"
      },
      {
        "communication": "Photographic authenticity — this is a photograph, not a render",
        "human_signal": "Skin on both subjects shows natural texture and minor imperfection; the background falls out of focus gradually rather than as a flat blurred layer",
        "observable_requirements": [
          "Visible pore texture and natural tone variation on both subjects' faces",
          "Background blur deepens gradually with distance — near-background path texture remains faintly visible, far-background harbor renders as soft warm bokeh shapes"
        ],
        "Visual Evidence Examples": [
          "A light perspiration sheen on the forehead/cheek consistent with running pace, not a glossy or matte-filtered surface",
          "Harbor lights or skyline edges in the background read as soft rounded bokeh shapes rather than a uniform color wash"
        ],
        "allocation_priority": "PreserveWhenPossible"
      }
    ],

    "CommunicationAllocation": [
      {
        "component": "Kinesthetic liberation — subjects' faces and stride expression",
        "supports": ["PrimaryCommunication"],
        "priority": "Critical",
        "survival_policy": "MustSurvive",
        "derived_from": ["NarrativeContract", "ArtDirectionContract", "StrategyContract"],
        "justification": "This is the emotional argument. If the faces read as athletic effort, social performance, or forced positivity rather than natural present-state ease, the conversion message — 'your body already knows how to do this' — fails entirely."
      },
      {
        "component": "Nike Novablast 5 mid-stride — ZOOMX midsole profile and Volt Swoosh",
        "supports": ["PrimaryCommunication", "CampaignObjective — product awareness"],
        "priority": "Critical",
        "survival_policy": "MustSurvive",
        "derived_from": ["CampaignContract ProductSpec", "ArtDirectionContract — shoe as motion argument", "CompositionRenderingContract — Primary hierarchy"],
        "justification": "This is a product awareness execution. If the Novablast 5 is not legible as a specific shoe — if the ZOOMX midsole profile and Volt Swoosh are not readable — the campaign objective is not met. The shoe must survive all downstream execution."
      },
      {
        "component": "Entity_01 identity — user's face and build from reference_asset_01",
        "supports": ["PrimaryCommunication", "CampaignContract — named subject requirement"],
        "priority": "High",
        "survival_policy": "MustSurvive",
        "derived_from": ["CampaignContract MandatoryRequirements", "SceneContract PreservationContracts"],
        "justification": "The user is a named required subject. Entity_01's face and physical build must be reproduced from reference_asset_01. If the generator fails to use the reference image, this must be flagged and retried."
      },
      {
        "component": "Entity_02 identity — Karina from aespa",
        "supports": ["PrimaryCommunication", "CampaignContract — named subject requirement"],
        "priority": "High",
        "survival_policy": "PreserveWhenPossible",
        "derived_from": ["CampaignContract MandatoryRequirements", "SceneContract named_subject"],
        "justification": "Karina is a named required subject. The generator must use its training knowledge of her likeness. If likeness is not achievable (generator refusal or inaccuracy), the visual descriptor fallback in SceneContract applies — a Korean female with her specific aesthetic characteristics."
      },
      {
        "component": "HK golden hour environment",
        "supports": ["SecondaryCommunication — city as setting for reclaimed time"],
        "priority": "High",
        "survival_policy": "PreserveWhenPossible",
        "derived_from": ["CampaignContract", "NarrativeContract", "CompositionRenderingContract"],
        "justification": "The HK setting is required by the brief. The golden hour time of day is required for the kinesthetic liberation narrative. If the environment cannot be HK-specific, it must at minimum be an outdoor golden hour waterfront setting."
      },
      {
        "component": "Synchronized parallel stride — the 'In Stride' visual concept",
        "supports": ["PrimaryCommunication"],
        "priority": "Medium",
        "survival_policy": "PreserveWhenPossible",
        "derived_from": ["ArtDirectionContract — In Stride concept", "StrategyContract — parallel liberation"],
        "justification": "The synchronized stride is the visual encoding of parallel liberation — two people in the same rhythm without performing for each other. If the stride cannot be perfectly synchronized, it may be simplified to two subjects running in the same direction at the same pace. The relational dynamic (not facing each other, not interacting) must survive."
      },
      {
        "component": "Natural skin rendering and progressive background blur falloff",
        "supports": ["PrimaryCommunication — photographic credibility"],
        "priority": "Medium",
        "survival_policy": "SimplifyWhenConstrained",
        "derived_from": ["CompositionRenderingContract v6.1 — Human Subject Rendering Requirement, Depth of Field Realism"],
        "justification": "These are realism cues, not narrative content — they support credibility but do not carry unique meaning on their own. They should remain present whenever possible, but if token pressure forces simplification, the core identity, action, and product requirements take priority."
      }
    ],

    "ExecutionResolution": {
      "PrimaryExecutionMode": "Golden hour lifestyle photograph of Karina and the user running in parallel stride on a Hong Kong waterfront path — faces carrying the expression of present-state liberation, Nike Novablast 5 in Volt / Black / White visible and legible mid-stride, HK harbor in warm atmospheric bokeh behind them.",
      "SupportingExecutionModes": [
        "HK golden hour as atmospheric context — warm directional backlight, harbor in background, the city at its best hour",
        "Nike Novablast 5 as the kinesthetic vehicle — the shoe mid-stride, its ZOOMX midsole the physical argument for what liberation feels like",
        "Parallel stride as relational encoding — two people in the same rhythm, not performing for each other"
      ],
      "ExecutionRequirements": [
        "Both subjects mid-stride running in the same direction — neither facing the camera directly",
        "Both subjects' faces visible and readable — expression of present-state ease",
        "Nike Novablast 5 on both subjects' feet — at least one shoe in full ZOOMX midsole side profile",
        "Volt Swoosh legible on at least one shoe",
        "HK outdoor environment at golden hour — warm directional light visible",
        "Camera below eye level at slight three-quarter angle — medium-full body shot from head to shoe, shot character consistent with a 50mm lens at f/2.8",
        "Entity_01 face and build reproduced from reference_asset_01"
      ],
      "ExcludedExecutionModes": [
        "Social interaction between subjects — no eye contact, no talking, no gestures toward each other",
        "Athletic intensity or competitive running posture",
        "Solo subject — both Karina and the user must be present",
        "Indoor or non-HK outdoor setting",
        "Night setting (replicate of Trial 1) — must be golden hour",
        "Product hero shot where shoe dominates without subjects",
        "Fitness transformation framing — no before/after, no body emphasis",
        "Flat, uniform background blur regardless of depth — background must show progressive falloff",
        "Airbrushed, poreless, or beauty-filtered skin on either subject"
      ]
    },

    "HierarchyResolution": {
      "PrimaryFocus": [
        "entity_01 + entity_02 faces — the expression of kinesthetic liberation (simultaneous primary)",
        "entity_03 — Nike Novablast 5 ZOOMX midsole mid-stride (simultaneous primary)"
      ],
      "SecondaryFocus": [
        "entity_01 + entity_02 stride — the synchronized running motion",
        "entity_04 — HK golden hour environment (atmospheric support)"
      ],
      "SupportingFocus": [],
      "AttentionSequence": [
        "1. Both subjects' faces — present-state liberation (simultaneous entry)",
        "2. Novablast 5 mid-stride — ZOOMX midsole profile and Volt Swoosh",
        "3. Synchronized stride geometry — parallel motion encoding the liberation concept",
        "4. HK harbor golden hour background — the city as context"
      ]
    },

    "RenderingResolution": {

      "PerceptualRendering": {
        "EmotionalTone": "Quiet liberation. The warmth of present-moment aliveness — not social excitement, not athletic achievement. The specific emotional register of a body that has remembered what it can do. Medium intensity: ease without languor, aliveness without performance.",
        "Atmosphere": "Hong Kong outdoor golden hour — warm, open, slightly humid, the city releasing the day. The light is the best light of the afternoon. It communicates: this is the hour that belongs to people who chose to move."
      },

      "PhysicalRendering": {
        "RealityModel": "Premium lifestyle editorial photography — indistinguishable from a high-quality candid editorial photograph taken at a Nike Chill Run Club event in Hong Kong at golden hour",
        "CameraIntent": "Below eye level, slight three-quarter angle, medium-full shot, shot on a 50mm lens at f/2.8. Camera below the subjects' eye line communicates energy and dynamism — the viewer looks slightly up at people in motion. The 30–45 degree body angle allows both faces and the lateral shoe profile to read simultaneously. The 50mm focal length renders subjects at natural, undistorted proportions; f/2.8 holds both subjects and the shoe in one sharp focus band while still separating them from the background.",
        "LightingIntent": "Golden hour backlight with ambient sky fill. Low sun creates warm rim separation on subjects against the atmospheric harbor background. Open sky above provides ambient fill on the shadow side of faces — both faces remain readable despite the backlight. Golden light catches the white ZOOMX midsole and Volt Swoosh naturally.",
        "MaterialBehavior": "Lightweight running fabric in motion — slight flutter and drape shift consistent with stride speed. Natural skin texture on both subjects — visible pores, tone variation, perspiration-adjacent moisture consistent with running. ZOOMX foam midsole renders as soft-matte foam, not glossy rubber. Engineered mesh upper renders as lightweight and slightly translucent.",
        "OpticalIntent": "Shallow to moderate depth of field at f/2.8 on a 50mm lens. Both subjects and their shoes in crisp foreground focus simultaneously. Path surface immediately behind subjects only mildly softened, retaining some texture; mid-distance softens further; HK harbor in warm atmospheric bokeh — shapes legible as harbor/skyline silhouettes, not reduced to a flat color wash. Blur deepens progressively with distance, never as a single uniform layer."
      },

      "RenderingQuality": {
        "DetailRendering": "High on both subjects' faces and on Novablast 5 shoe — the ZOOMX midsole profile and Volt Swoosh must be granular enough to identify the specific shoe at Instagram viewing size. Medium on stride posture and running form. Low to medium on background environment — atmospheric warm bokeh, with progressive (not flat) falloff.",
        "TextureRendering": "Natural skin texture on both subjects — visible pore detail, natural tone variation, no AI-smoothed or porcelain rendering, light perspiration sheen consistent with running. Fabric texture on athletic wear consistent with running motion. ZOOMX foam: matte, slightly soft-edged surface consistent with foam construction. Engineered mesh: lightweight and slightly translucent in the golden light.",
        "LightingRendering": "Warm golden hour quality throughout — no cold blue tones, no studio flash, no dramatic cinematic contrast. Rim backlight on subjects warm and natural. Fill on faces from ambient sky cool enough to reveal expression without reducing the golden hour character.",
        "DepthRendering": "Clear foreground-background separation with progressive depth-dependent blur falloff: subjects and shoe crisp; near-background path surface mildly soft with retained texture; far-background HK harbor in warm rounded bokeh.",
        "CommercialRendering": "Premium Nike lifestyle editorial quality — high production value without clinical or studio artificiality. Feels photographed on a real lens, not rendered."
      },

      "AuthenticityBehavior": {
        "HumanAuthenticityRendering": "Both subjects mid-stride — not posed, not stationary. Running posture shows natural variation: slight asymmetry in arm swing, natural lean from stride momentum. Faces not posed for camera — the eyes look forward in the direction of motion, not toward the lens. Expression is mid-moment, not held. Skin on both subjects shows natural pore texture, subtle tonal variation, and natural facial asymmetry — not airbrushed, not beauty-filtered, not artificially flawless.",
        "EnvironmentalAuthenticityRendering": "Hong Kong outdoor path shows natural surface texture. Golden hour light has natural warm inconsistency — not uniformly golden, not studio-lit. HK harbor background has natural atmospheric depth — not a painted backdrop, and its softness follows real lens falloff rather than a flat blur overlay.",
        "MaterialAuthenticityRendering": "Running wear moves with subjects — fabric is not statically posed. Shoe materials render realistically: foam as foam, mesh as mesh, rubber pods as rubber. Skin texture shows natural running warmth and subtle perspiration.",
        "ImperfectionRendering": "Credibility over perfection. Slight motion blur on trailing foot or swinging arm is correct — evidence of actual running speed. Natural stride asymmetry between subjects is correct and preferred. A partially visible shoe or slightly asymmetric framing is acceptable if it increases photographic credibility. Visible skin texture and a non-uniform background blur are required, not optional polish."
      }
    },

    "PreservationResolution": {
      "PreservedEntities": [
        "Entity_01 (the user): face and physical build reproduced from reference_asset_01 — short dark black hair, defined cheekbones and squared jaw, prominent brow ridge, dark brown eyes with double eyelid, clear warm-toned skin, lean athletic build. Expression in scene: present-state liberation ease appropriate to running context. Do not generate from training data.",
        "Entity_02 (Karina from aespa): Korean female, approximately 24–26, sculpted facial structure with defined jaw and high cheekbones, large dark eyes, slim tall build, sleek dark hair. Expression: same present-state liberation register as entity_01. Generator must use training knowledge of her likeness; visual descriptors serve as fallback.",
        "Entity_03 (Nike Novablast 5 Volt / Black / White): black engineered mesh upper, white ZOOMX foam midsole with rounded convex bottom profile, Volt Swoosh on lateral side, Volt rubber outsole pods on white midsole base, high heel stack, rocker profile. At least one shoe in full lateral midsole profile mid-stride. Generated from training data using model name + visual descriptors."
      ],
      "PreservedContext": [
        "HK outdoor waterfront environment at golden hour — warm directional light, harbor or skyline visible",
        "Instagram 4:5 format (1080×1350px) — top 10% and bottom 20% reserved as text-safe zones for Cantonese copy and CTA overlay"
      ],
      "PreservedBrandRequirements": [
        "Nike Swoosh or brand mark visible on subjects' apparel in addition to shoe brand mark",
        "Human subjects as primary visual element — shoes and environment are supporting context",
        "Editorial photography language — photographed, not rendered; candid, not staged"
      ],
      "PreservedNarrativeRequirements": [
        "Neither subject faces the camera or each other — both face forward in the direction of motion",
        "Expression of present-state liberation — ease without performance, aliveness without effort",
        "No social interaction between subjects — parallel liberation, not social warmth"
      ],
      "PreservedConstraints": [
        "Cantonese copy and CTA overlay applied in post-production — no critical visual information in top 10% or bottom 20%",
        "No night setting — must be golden hour (differentiation from Trial 1)",
        "No athletic competition, performance intensity, or fitness transformation framing",
        "50mm / f/2.8 lens character — natural perspective, progressive depth-dependent background blur, no flat/uniform bokeh",
        "Natural skin rendering on both subjects — visible texture, no airbrushing"
      ]
    }
  }
}
```

```json
{
  "SynthesisContract": {

    "ExecutiveSummary": "A Hong Kong office lady's 3:30pm break, reframed from guilty snacking into a light, guilt-free 'light-beauty' ritual. She sits at a near-empty, clean desk — photoshoot-set quality, nothing on the surface except the CLEVER lemon CLEAR PROTEIN pouch, its transparent clear-drink shaker, and one small clock at ~3:30. Calm, lightly satisfied, quietly confident. The clear drink and pack are the brightest, sharpest heroes; she is the emotional proof; the clean minimal background carries the on-image ad headline '告別3點3罪惡感！' + subtitle '日本製·清蛋白' as the editorial voice that names the moment. Brand assets (lemon pack, clear shaker, CLEVER logo) reproduced from image1.png and image4.png. The headline is campaign-mandatory — it makes the ad intent explicit and must survive at full legibility.",

    "CommunicationResolution": {
      "PrimaryCommunication": {
        "statement": "CLEVER's Made-in-Japan clear lemon protein is a light, refreshing, guilt-free afternoon-tea ritual that replaces guilty 3:30pm snacking without heaviness or sacrifice.",
        "derived_from": {
          "campaign": "Trial acquisition; reframe 3:30pm snacking; 日本製清蛋白 light-beauty afternoon tea; high-protein low-calorie, clear refreshing.",
          "brand": "Refreshing performance without the burden; protein that behaves like a refreshing drink; clean, intelligent, Japanese-made clear WPI.",
          "strategy": "Recode guilty snacking into smart light-beauty hydration ritual; Accessibility + Performance + Confidence.",
          "narrative": "Guilty snacker → smart light-beauty office lady; heavy cheat feeling → light, refreshing beauty-support feeling.",
          "art_direction": "Office Light-Beauty Ritual; clear drink as hero on clean minimal desk; Low structural density; quiet confidence; on-image ad typography names the emotional shift."
        }
      },
      "SecondaryCommunication": [
        { "statement": "The drink is genuinely clear and light — fruit-juice-like, not powdery, milky, or heavy.", "supports": "PrimaryCommunication", "priority": "High" },
        { "statement": "The choice is calm, image-smart, and guilt-free — quiet self-respect, not sacrifice.", "supports": "PrimaryCommunication", "priority": "High" },
        { "statement": "Made in Japan — refined, trustworthy, light-science quality.", "supports": "PrimaryCommunication", "priority": "Medium" },
        { "statement": "This is a 3:30pm moment — an office afternoon, relatable and specific.", "supports": "PrimaryCommunication", "priority": "Medium" }
      ],
      "SuppressedCommunication": [
        { "statement": "Gym / bodybuilding / muscular performance staging.", "reason": "Forbidden positioning — contradicts light office-elegant lifestyle brand." },
        { "statement": "Busy, cluttered desk or lived-in background detail.", "reason": "Art Direction: Low structural density; 'clean desk sanctuary'; clutter undermines the hero and the 'effortless, clean ritual' message." },
        { "statement": "Dramatic weight-loss / before-after / body-shaming.", "reason": "Forbidden meaning + legal/platform constraints." },
        { "statement": "Thick, opaque, or milky shake appearance.", "reason": "Directly contradicts the core 'clear refreshing drink' differentiator." },
        { "statement": "Multi-flavor lineup, grape variant, spring promotion, timing-clock graphic, outdoor running.", "reason": "Off-concept; resolved to single lemon hero, office afternoon setting." },
        { "statement": "Windows, plants, busy office furniture visible in background.", "reason": "Scene Contract entity_06: background must be clean, minimal, near-empty." },
        { "statement": "Any text, watermarks, or slogans other than the specified on-image ad copy.", "reason": "Scene Contract explicitly_excluded_objects; only '告別3點3罪惡感！' + '日本製·清蛋白' are permitted." }
      ],
      "MemoryAnchor": {
        "statement": "告別3點3罪惡感！ — a clear lemon protein drink on a clean, minimal desk at 3:30.",
        "justification": "The combination of the on-image headline naming the emotional shift AND the clear drink on a pristine desk surface makes this instantly legible as an advertisement with a specific, ownable message. The headline and the product prove each other."
      }
    },

    "ObservableSignalMapping": [
      {
        "communication": "Clear, refreshing drink (not a heavy shake)",
        "human_signal": "Relaxed, easy enjoyment of a light, clearly see-through beverage",
        "observable_requirements": [
          "Transparent vessel with visibly clear, translucent pale-yellow liquid",
          "Light passing through the drink — not opaque",
          "Lemon slice or lemon cue"
        ],
        "Visual Evidence Examples": ["Condensation on the shaker", "Liquid catching the light", "Pale-yellow tint, never milky white"],
        "allocation_priority": "MustSurvive"
      },
      {
        "communication": "Guilt-free, light, quietly confident ritual",
        "human_signal": "Calm satisfaction; soft, natural composure; relaxed posture",
        "observable_requirements": [
          "Natural, unposed expression — content, not performing",
          "Relaxed shoulders, unhurried body language",
          "No diet anxiety, no strain, no performance energy"
        ],
        "Visual Evidence Examples": ["Gentle gaze toward or past the drink", "Easy seated posture"],
        "allocation_priority": "MustSurvive"
      },
      {
        "communication": "On-image ad copy — names the emotional shift ('告別3點3罪惡感！')",
        "human_signal": "—",
        "observable_requirements": [
          "Headline '告別3點3罪惡感！' legible in the upper background zone",
          "Subtitle '日本製·清蛋白' legible below the headline",
          "Typography does not overlap the OL or the product cluster"
        ],
        "Visual Evidence Examples": ["Bold sans-serif headline in upper frame", "Clean sky-blue background provides contrast for text"],
        "allocation_priority": "MustSurvive"
      },
      {
        "communication": "Clean, minimal ritual environment (not a cluttered desk)",
        "human_signal": "A curated, controlled personal space signals intentionality and self-respect",
        "observable_requirements": [
          "Near-empty desk surface — only the pack, shaker, and one small clock",
          "Clean, uncluttered, minimal background — no competing visual information"
        ],
        "Visual Evidence Examples": ["Photoshoot-set quality desk", "Clean sky-blue background plane carrying the headline"],
        "allocation_priority": "MustSurvive"
      },
      {
        "communication": "CLEVER brand + Made-in-Japan identity",
        "human_signal": "—",
        "observable_requirements": [
          "Legible CLEVER lemon CLEAR PROTEIN pouch",
          "CLEVER logo visible on shaker and/or layout",
          "'Made in Japan / 日本製' legible in frame"
        ],
        "Visual Evidence Examples": ["Pack facing camera, clearly lit", "Logo on bottle"],
        "allocation_priority": "PreserveWhenPossible"
      },
      {
        "communication": "3:30pm office afternoon context",
        "human_signal": "Seated at a desk during a break",
        "observable_requirements": [
          "Small desk clock reading approximately 3:30",
          "Office-appropriate wardrobe (not gym wear)"
        ],
        "Visual Evidence Examples": ["Small analog or minimal digital clock on desk edge"],
        "allocation_priority": "SimplifyWhenConstrained"
      }
    ],

    "CommunicationAllocation": [
      { "component": "Clear lemon drink as hero", "priority": "Critical", "survival_policy": "MustSurvive", "derived_from": ["Brand truth", "SceneContract entity_03", "AD FocalPriority t1"], "justification": "The single differentiating visual truth — if lost, the ad becomes any protein ad." },
      { "component": "Guilt-free light confidence of the OL", "priority": "Critical", "survival_policy": "MustSurvive", "derived_from": ["Narrative", "AD VisualIntent"], "justification": "Emotional payoff; core of the concept." },
      { "component": "On-image ad headline '告別3點3罪惡感！' + subtitle '日本製·清蛋白'", "priority": "Critical", "survival_policy": "MustSurvive", "derived_from": ["CampaignContract MandatoryRequirements.required_copy", "AD TypographicIntent", "SceneContract entity_07"], "justification": "Campaign-mandatory: the image must read as an advertisement at a glance. The headline names the emotional shift the product delivers. Cannot be omitted or illegible." },
      { "component": "Clean, near-empty minimal desk and background", "priority": "Critical", "survival_policy": "MustSurvive", "derived_from": ["AD: Low StructuralDensity", "AD: Clean Desk Sanctuary", "SceneContract entity_05/06"], "justification": "Low density is the mechanism that makes the hero legible and gives the background space for the headline." },
      { "component": "CLEVER lemon pack + logo + Made-in-Japan", "priority": "High", "survival_policy": "PreserveWhenPossible", "derived_from": ["CampaignContract MandatoryRequirements", "SceneContract entity_02/04"], "justification": "Required branding; reference-locked brand assets." },
      { "component": "3:30pm office afternoon moment", "priority": "Medium", "survival_policy": "SimplifyWhenConstrained", "derived_from": ["AD VisualConcept", "SceneContract entity_05"], "justification": "One small clock is sufficient; don't over-furnish." }
    ],

    "ExecutionResolution": {
      "PrimaryExecutionMode": "Single-moment lifestyle advertisement — a 3:30pm office break, hero is the clear lemon drink on a near-empty desk, on-image headline names the emotional shift.",
      "SupportingExecutionModes": [
        "Product-as-hero clarity (drink + pack are brightest and sharpest)",
        "Quiet emotional embodiment (OL as proof of guilt-free satisfaction)",
        "Photoshoot-set clean background carrying the ad headline",
        "On-image typography as the editorial voice of the ad"
      ],
      "ExecutionRequirements": [
        "Drink must read as clear and translucent",
        "Desk surface must be near-empty — pack, shaker, and one small clock only",
        "Background must be clean, uncluttered, and minimal",
        "On-image headline '告別3點3罪惡感！' must be legible in the upper background zone",
        "On-image subtitle '日本製·清蛋白' must be legible below the headline",
        "No other text in the image beyond the specified ad copy",
        "Single human subject, office-appropriate, lifestyle (not gym/athletic)",
        "Brand assets reproduced from reference images — not invented"
      ],
      "ExcludedExecutionModes": [
        "Gym / performance / bodybuilding staging",
        "Cluttered or lived-in desk with everyday objects",
        "Busy or detailed background (windows, plants, shelving, people)",
        "Thick opaque shake depiction",
        "Multi-flavor lineup, grape variant, outdoor running, timing-clock motif",
        "Before-after or weight-loss demonstration",
        "Random or unspecified text beyond the designated ad copy"
      ]
    },

    "HierarchyResolution": {
      "PrimaryFocus": ["entity_03 (clear lemon drink)", "entity_02 (CLEVER lemon pack)"],
      "SecondaryFocus": ["entity_01 (the OL — emotional proof)", "entity_07 (ad headline — editorial voice)"],
      "SupportingFocus": ["entity_04 (CLEVER logo + Made-in-Japan)", "entity_05 (minimal desk + clock)", "entity_06 (clean background)"],
      "AttentionSequence": ["entity_03", "entity_02", "entity_01", "entity_07", "entity_04", "entity_05"]
    },

    "RenderingResolution": {

      "PerceptualRendering": {
        "EmotionalTone": "Calm, light, quietly confident, guilt-free — optimistic and achievable. Clean and curated, not cozy or cluttered.",
        "Atmosphere": "Bright, airy, high-key Japanese-refreshment mood. A near-empty, purposefully minimal personal space — the on-image headline and the clean background together make the ad's message instant and undeniable."
      },

      "PhysicalRendering": {
        "RealityModel": "Realistic",
        "CameraIntent": "Eye-level near medium shot at desk distance, peer-level — viewer feels seated across from her. 85mm perspective is slightly compressed and flattering.",
        "CameraSpecs": {
          "focal_length_mm": "85mm",
          "aperture_f_stop": "f/4"
        },
        "LightingIntent": "Soft, bright high-key daylight. Clear drink and pack get the cleanest, most direct light with a gentle specular glint on glass and liquid. OL is lit a touch softer. Background is evenly lit as a smooth, shadow-free sky-blue plane — consistent exposure supports typography legibility. Nothing in the background outshines the hero product cluster.",
        "LuminanceHierarchy": [
          { "element": "entity_03", "luminance_priority": "Brightest" },
          { "element": "entity_02", "luminance_priority": "Brightest" },
          { "element": "entity_01", "luminance_priority": "Mid" },
          { "element": "entity_07", "luminance_priority": "Mid" },
          { "element": "entity_04", "luminance_priority": "Mid" },
          { "element": "entity_05", "luminance_priority": "Dimmest" },
          { "element": "entity_06", "luminance_priority": "Dimmest" }
        ],
        "MaterialBehavior": "Clear translucent liquid with light passing through (never opaque); light condensation on shaker; matte pouch vs. glossy bottle material contrast; natural human skin with visible pores, fine lines, and subtle asymmetry — no airbrushing.",
        "OpticalIntent": "Progressive, depth-dependent bokeh from 85mm at f/4: foreground pack and shaker are crisp, OL is sharp to gently diffuse by depth, the minimal background softens further into a smooth even sky-blue plane. Typography sits in the background plane — slightly softened by depth but fully legible. No flat uniform blur."
      },

      "RenderingQuality": {
        "DetailRendering": "Highest detail on hero cluster (pack typography, logo, liquid clarity); progressively reduced toward background. Typography must be rendered as legible text, not decorative texture.",
        "TextureRendering": "Real skin texture, fabric weave, condensation, matte/gloss contrast on product materials.",
        "LightingRendering": "Clean high-key with controlled gentle speculars on glass; no harsh shadows; background lit flat and even to support headline legibility.",
        "DepthRendering": "Clear foreground/midground separation; background reads as a single smooth plane carrying the ad headline.",
        "CommercialRendering": "Polished, clean, social-commerce advertising quality — lifestyle authenticity in the subject, designed ad layout in the typography."
      },

      "AuthenticityBehavior": {
        "HumanAuthenticityRendering": "Natural skin texture (pores, fine lines, subtle tone unevenness), natural asymmetry, candid unposed expression and relaxed body language. Healthy and attractive but real — never beauty-filtered.",
        "EnvironmentalAuthenticityRendering": "The desk is intentionally minimal and clean — like a curated photoshoot set. The cleanliness IS the authenticity. The background is an intentional designed space, not a real office — it carries the ad headline as a deliberate layout choice.",
        "MaterialAuthenticityRendering": "Believable glass and liquid optics, real condensation behavior, true fabric drape on wardrobe.",
        "ImperfectionRendering": "Credibility over perfection for skin and material behavior. The desk and background must be genuinely clean and pristine — surface imperfections in those elements work against the intended aesthetic and the typography legibility."
      }
    },

    "PreservationResolution": {
      "PreservedEntities": [
        "entity_02 — CLEVER lemon CLEAR PROTEIN pouch (Near Exact, reproduce from reference_asset_01 / image1.png)",
        "entity_03 — Transparent shaker with clear pale-yellow lemon drink + CLEVER logo (Near Exact, reproduce from reference_asset_01 / image1.png; clear/translucent liquid mandatory)",
        "entity_04 — CLEVER logo / wordmark + Made-in-Japan cue (Exact, reproduce from reference_asset_02 / image4.png)",
        "entity_07 — On-image ad headline '告別3點3罪惡感！' + subtitle '日本製·清蛋白' (Critical, must be present and legible)"
      ],
      "PreservedConstraints": [
        "No medical or curative claims",
        "No hardcore gym or supplement positioning",
        "No legible invented text beyond the specified ad copy",
        "No background clutter — the clean minimal desk and background are non-negotiable",
        "No text other than '告別3點3罪惡感！' and '日本製·清蛋白'"
      ]
    }
  }
}
```

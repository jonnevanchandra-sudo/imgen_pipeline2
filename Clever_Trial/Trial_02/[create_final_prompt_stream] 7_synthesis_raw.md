```json
{
  "SynthesisContract": {

    "ExecutiveSummary": "A Hong Kong office lady's 3:30pm break, reframed from guilty snacking into a light, guilt-free 'light-beauty' ritual. At her clean, bright desk she holds a transparent shaker of clear pale-yellow lemon CLEVER protein — visibly a refreshing clear drink, not a thick shake — with the lemon CLEAR PROTEIN pouch and CLEVER / Made-in-Japan branding beside her. Calm, lightly satisfied, quietly confident. The clear drink + pack are the brightest, sharpest hero; she reads as proof of the payoff; the softened office afternoon confirms the moment. Brand assets are reproduced from attached reference images, not invented.",

    "CommunicationResolution": {
      "PrimaryCommunication": {
        "statement": "CLEVER's Made-in-Japan clear lemon protein is a light, refreshing afternoon-tea drink that replaces the guilty 3:30pm snack without guilt or heaviness.",
        "derived_from": {
          "campaign": "Trial acquisition; reframe 3:30pm snacking; 日本製清蛋白 light-beauty afternoon tea; clear refreshing high-protein low-calorie.",
          "brand": "Refreshing performance without the burden; protein that behaves like a refreshing drink; clean, intelligent, Japanese-made clear WPI.",
          "strategy": "Recode guilty snacking into a smart, light-beauty hydration ritual; Accessibility + Performance + Confidence.",
          "narrative": "Guilty snacker → smart, light-beauty office lady; heavy 'cheat' feeling → light, refreshing 'beauty-support' feeling.",
          "art_direction": "Office Light-Beauty Ritual; clear fruity drink as hero replacing guilty snack; quiet confidence, guilt-free lightness."
        }
      },
      "SecondaryCommunication": [
        { "statement": "It is a clear, fruit-juice-like drink — light and refreshing, not powdery, milky, or 'gym-bro'.", "supports": "PrimaryCommunication", "priority": "High" },
        { "statement": "The choice is calm, image-smart and guilt-free — quiet self-respect, not sacrifice or dieting.", "supports": "PrimaryCommunication", "priority": "High" },
        { "statement": "This belongs naturally on an office desk at the 3:30pm afternoon break.", "supports": "PrimaryCommunication", "priority": "Medium" },
        { "statement": "Made in Japan — refined, light-science quality and trust.", "supports": "PrimaryCommunication", "priority": "Medium" }
      ],
      "SuppressedCommunication": [
        { "statement": "Hardcore gym / bodybuilding performance, muscular posing, black supplement-tub imagery.", "reason": "Forbidden positioning — contradicts light, office-elegant, lifestyle-accessible identity." },
        { "statement": "Dramatic weight-loss / before-after / scale-and-tape transformation.", "reason": "Forbidden meaning + legal/platform constraints; no guaranteed-slimming or body-shaming." },
        { "statement": "Thick, opaque, milky shake appearance.", "reason": "Directly contradicts the core 'clear refreshing drink' differentiator." },
        { "statement": "Junk-food / snack clutter shown alongside the product.", "reason": "Brand constraint — must not appear unhealthy or cheapen the product." },
        { "statement": "Multi-flavor three-pack lineup; grape variant; outdoor running motif; timing-clock graphic.", "reason": "Off-concept for a single-hero lemon office afternoon scene; resolved to defaults at Scene Assembly (no client response)." }
      ],
      "MemoryAnchor": {
        "statement": "A clear lemon protein drink on the office desk at 3:30 — refreshing, light, guilt-free.",
        "justification": "Single, instantly legible image: the hero is a transparent clear drink in an office afternoon context, which is what distinguishes CLEVER from heavy shakes and slimming teas and what the viewer should retain."
      }
    },

    "ObservableSignalMapping": [
      {
        "communication": "Clear, refreshing drink (not a heavy shake)",
        "human_signal": "Relaxed, easy enjoyment of a light beverage",
        "observable_requirements": ["Transparent vessel with visibly clear/translucent pale-yellow liquid", "Light passing through the drink", "Lemon refreshment cue"],
        "Visual Evidence Examples": ["Condensation on a clear shaker", "Lemon slice visible", "Liquid catches light rather than reading opaque"],
        "allocation_priority": "MustSurvive"
      },
      {
        "communication": "Guilt-free, light satisfaction",
        "human_signal": "Calm, lightly satisfied, quietly confident expression and posture",
        "observable_requirements": ["Soft natural smile or content composure", "Relaxed shoulders, unhurried body language", "No strain, no performance, no diet anxiety"],
        "Visual Evidence Examples": ["Gentle gaze toward or just past the drink", "Easy seated posture at the desk"],
        "allocation_priority": "MustSurvive"
      },
      {
        "communication": "Brand + Made-in-Japan identity",
        "human_signal": "—",
        "observable_requirements": ["Legible CLEVER lemon CLEAR PROTEIN pouch", "CLEVER logo on shaker and layout", "Made in Japan / 日本製 cue legible"],
        "Visual Evidence Examples": ["Pouch standing on desk facing camera", "Logo on bottle"],
        "allocation_priority": "PreserveWhenPossible"
      },
      {
        "communication": "Office afternoon (3:30pm) context",
        "human_signal": "Seated at a work desk on a break",
        "observable_requirements": ["Clean office desk environment", "Subtle afternoon-time cue", "Office-appropriate, non-gym wardrobe"],
        "Visual Evidence Examples": ["Laptop, tidy desk", "Small desk clock ~3:30"],
        "allocation_priority": "SimplifyWhenConstrained"
      }
    ],

    "CommunicationAllocation": [
      { "component": "Clear refreshing lemon drink (hero)", "supports": ["PrimaryCommunication"], "priority": "Critical", "survival_policy": "MustSurvive", "derived_from": ["AD FocalPriority t1", "Brand truth", "SceneContract entity_03"], "justification": "The single differentiating truth; if lost, the ad becomes a generic protein shake." },
      { "component": "Guilt-free, light, quietly confident emotional state", "supports": ["PrimaryCommunication"], "priority": "Critical", "survival_policy": "MustSurvive", "derived_from": ["Narrative", "AD VisualIntent"], "justification": "The emotional payoff that reframes 3:30pm; core of the concept." },
      { "component": "CLEVER lemon pack + logo + Made-in-Japan", "supports": ["SecondaryCommunication"], "priority": "High", "survival_policy": "PreserveWhenPossible", "derived_from": ["CampaignContract MandatoryRequirements", "SceneContract entity_02/04"], "justification": "Required branding; reference-locked brand assets." },
      { "component": "Office light-beauty ritual context", "supports": ["SecondaryCommunication"], "priority": "Medium", "survival_policy": "SimplifyWhenConstrained", "derived_from": ["AD VisualConcept", "SceneContract entity_05"], "justification": "Establishes the 'same moment, smarter content' frame; may simplify under pressure but should remain office-afternoon." }
    ],

    "ExecutionResolution": {
      "PrimaryExecutionMode": "Single-moment lifestyle realism — an authentic 3:30pm office-desk break centered on the clear lemon protein drink as hero.",
      "SupportingExecutionModes": [
        "Product-as-hero clarity (the clear drink and pack are the brightest, sharpest focal cluster)",
        "Quiet emotional embodiment (calm, guilt-free satisfaction read through the OL)"
      ],
      "ExecutionRequirements": [
        "Drink must read as clear/translucent",
        "Single human subject, office-appropriate and lifestyle (not athletic/gym)",
        "Brand assets reproduced from reference images, not invented",
        "Clean, light, airy register with breathing room"
      ],
      "ExcludedExecutionModes": [
        "Gym / performance / bodybuilding staging",
        "Before-after / weight-loss demonstration",
        "Thick opaque shake depiction",
        "Snack-clutter or junk-food juxtaposition",
        "Multi-flavor lineup, grape variant, outdoor running, timing-clock motif"
      ]
    },

    "HierarchyResolution": {
      "PrimaryFocus": ["entity_03 (clear lemon drink in shaker)", "entity_02 (lemon CLEAR PROTEIN pouch)"],
      "SecondaryFocus": ["entity_01 (the OL — emotional proof)"],
      "SupportingFocus": ["entity_04 (CLEVER logo + Made-in-Japan)", "entity_05 (clean office afternoon context)"],
      "AttentionSequence": ["entity_03", "entity_02", "entity_01", "entity_04", "entity_05"]
    },

    "RenderingResolution": {

      "PerceptualRendering": {
        "EmotionalTone": "Calm, light, quietly confident, guilt-free — optimistic and achievable, never strenuous or aspirational-unattainable.",
        "Atmosphere": "Bright, clean, airy Japanese-refreshment mood; a small island of calm self-care within the workday."
      },

      "PhysicalRendering": {
        "RealityModel": "Realistic",
        "CameraIntent": "Eye-level, near medium shot at desk distance — peer-level 'this could be me' framing of the OL with the clear drink and pack held in the foreground. Background office softened so it stays contextual, not competing.",
        "CameraSpecs": {
          "focal_length_mm": "50mm",
          "aperture_f_stop": "f/4"
        },
        "LightingIntent": "Soft, bright, high-key daylight. The clear drink and pack get the cleanest, brightest light with a gentle specular highlight on glass/liquid to read crisp and refreshing; the OL is lit slightly softer; office background and any window are exposed down so nothing behind the subject blows out or outshines the hero. Warm-neutral skin, never orange; airy, not clinical.",
        "LuminanceHierarchy": [
          { "element": "entity_03", "luminance_priority": "Brightest" },
          { "element": "entity_02", "luminance_priority": "Brightest" },
          { "element": "entity_01", "luminance_priority": "Mid" },
          { "element": "entity_04", "luminance_priority": "Mid" },
          { "element": "entity_05", "luminance_priority": "Dimmest" }
        ],
        "MaterialBehavior": "Clear, translucent beverage with light passing through (never opaque/milky); light condensation on the shaker; matte pouch surface vs. glossy bottle; natural human skin with visible pores, fine lines, and subtle asymmetry — no airbrushing.",
        "OpticalIntent": "Progressive depth-dependent background softening: foreground drink and pack crisp, OL sharp-to-gently-soft by depth, office softens gradually with distance (near desk and ~3:30 cue semi-legible, far walls softer). Smooth gentle bokeh, no uniform cutout blur."
      },

      "RenderingQuality": {
        "DetailRendering": "High detail on the hero cluster (pack typography, logo, liquid clarity); progressively reduced toward the background.",
        "TextureRendering": "Real skin texture, fabric weave, condensation droplets, matte/gloss material contrast.",
        "LightingRendering": "Clean high-key daylight with controlled, gentle speculars; no harsh shadows, no studio flatness.",
        "DepthRendering": "Clear foreground-to-background separation via Atmospheric DoF and luminance, keeping the office legible as context.",
        "CommercialRendering": "Polished and clean enough for social commerce, but credible and lifestyle — not a sterile studio packshot."
      },

      "AuthenticityBehavior": {
        "HumanAuthenticityRendering": "Natural skin texture (pores, fine lines, subtle tone unevenness), asymmetric candid expression, relaxed unposed body language; healthy and attractive but real, not beauty-filtered.",
        "EnvironmentalAuthenticityRendering": "A real, lived-in but tidy office desk — minor natural imperfections (slight clutter edge, real surface reflections), not an empty CGI set.",
        "MaterialAuthenticityRendering": "Believable glass/liquid optics, real condensation, true fabric behavior on wardrobe.",
        "ImperfectionRendering": "Credibility takes priority over perfection — no plastic skin, no flawless symmetry, no over-smoothed 'AI-perfect' look."
      }
    },

    "PreservationResolution": {
      "PreservedEntities": [
        "entity_02 — CLEVER lemon CLEAR PROTEIN pouch (Near Exact, reproduce from reference_asset_01)",
        "entity_03 — transparent shaker with clear pale-yellow lemon drink + CLEVER logo (Near Exact, reproduce from reference_asset_01; clear/translucent mandatory)",
        "entity_04 — CLEVER logo / wordmark (Exact, reproduce from reference_asset_02)"
      ],
      "PreservedContext": [
        "Office afternoon (3:30pm) setting; clean, light, minimal workspace",
        "Single human subject as an HK OL lifestyle persona (not gym/athletic)"
      ],
      "PreservedBrandRequirements": [
        "CLEVER brand name / logo clearly present",
        "Made in Japan / 日本製 cue present and legible",
        "Light/sky-blue + white clean brand visual system",
        "Product reads clear, light and refreshing — never heavy or opaque"
      ],
      "PreservedNarrativeRequirements": [
        "Quiet, guilt-free, light-beauty confidence — no sacrifice, no diet anxiety",
        "Everyday achievable office moment, not a dramatic transformation"
      ],
      "PreservedConstraints": [
        "No medical/curative claims, no guaranteed-slimming, no body-shaming",
        "No hardcore gym/supplement positioning",
        "No legible on-image marketing copy required from the generator (final Cantonese copy is added by the app/design layer)"
      ]
    }
  }
}
```

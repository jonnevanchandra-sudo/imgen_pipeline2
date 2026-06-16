# Brand Contract — CLEVER Protein (Stage 0)

Framework: `0.Brand Intelligence.v2.md`
Input: Brand website (`shop.cleverprotein.com.hk`, `cleverprotein.com.hk/about-clever`), Weight Down product collection page, and general search results for CLEVER Protein HK.

**Run mode: Web-Sourced Extraction (partial).** No raw ad creative or campaign imagery was supplied — this contract is built from the brand's e-commerce site, about page, and product collection pages. Direct statements/descriptions from the site are treated as Observations (no confidence score). Everything about visual *campaign* behavior (as opposed to e-commerce product pages) is Inference, capped at moderate confidence since no social/ad creative was reviewed directly.

```json
{
  "BrandContract": {
    "Metadata": {
      "brand": "CLEVER Protein (CLEVER 蛋白)",
      "market": "Hong Kong (official market site shop.cleverprotein.com.hk)",
      "sources": [
        "https://shop.cleverprotein.com.hk/",
        "https://www.cleverprotein.com.hk/about-clever/",
        "https://shop.cleverprotein.com.hk/collections/clever-weight-down"
      ]
    },

    "Observations": [
      "Site self-describes as '日本人氣蛋白粉品牌' (popular Japanese protein powder brand), manufactured in Japan",
      "Three product lines: Clear Protein Series (清・蛋白, ultra-filtered WPI, near-zero lactose/fat, translucent 'Clear WPI' drink), Muscle Series (純・蛋白, WPI + probiotics/vitamins), Weight Down Series (減重蛋白, protein + dietary fiber + probiotics + MCT oil + vitamins for satiety)",
      "Weight Down line: 4 flavors — matcha latte (vegan, 294g), chocolate, yogurt, mixed berries (315g each), HK$179 standard, bundle promo '減重蛋白$270/2包'",
      "Marketing copy emphasizes '精準萃取技術' (precision extraction technology) and '100%頂級高品質' (100% top-grade quality)",
      "100% WPI, 80% protein content; products include active enzymes and probiotics for absorption/digestive support",
      "Products carry British LGC laboratory (Informed Choice) anti-doping certification",
      "Visual design across the site: soft pink/rose accent tones against white/clean backgrounds, contemporary sans-serif typography, minimalist layout with light/airy whitespace",
      "Product photography mixes clean studio product shots with lifestyle imagery of the powder mixed into drinks",
      "Design motif emphasizes 'purity' and 'clarity' through translucent product visuals (e.g. the Clear Protein drink shown as a see-through liquid)",
      "Site framing repeatedly uses the word 'Clever' / '醒目選擇' (smart/clever choice) as the core decision-framing device for the brand name itself"
    ],

    "RecurringPatterns": [
      { "pattern": "Clarity/Purity-as-proof", "frequency": "high", "supporting_observations": ["translucent Clear Protein drink visuals", "'精準萃取技術' copy", "minimalist white/pink layouts"] },
      { "pattern": "Credential-led trust signaling", "frequency": "moderate", "supporting_observations": ["LGC/Informed Choice anti-doping certification", "'100%頂級高品質' sourcing language", "Japan manufacturing claim"] },
      { "pattern": "Soft, approachable femme-leaning palette over hard 'gym bro' visual codes", "frequency": "high", "supporting_observations": ["pink/rose accent on white", "light airy layout", "flavor names like matcha latte / mixed berries framed closer to a café drink than a sports supplement"] }
    ],

    "Inferences": [
      { "statement": "The brand positions itself at the intersection of supplement-grade credibility and everyday lifestyle/café consumption — closer to 'smart daily habit' than 'hardcore sports nutrition'", "confidence": 0.75 },
      { "statement": "The pink/white minimalist palette and café-style flavor naming suggest the brand's visual identity is built to feel approachable and slightly premium-lifestyle, not clinical/sterile despite the scientific claims", "confidence": 0.7 },
      { "statement": "'Clever' as a brand name functions as a recurring decision-framing device — the brand likely wants its communication to consistently frame product choice as the 'smart'/'savvy' option versus an inferior alternative, which aligns naturally with comparison-style ('this vs that') formats", "confidence": 0.65 }
    ],

    "SignalClassification": {
      "Core": ["Purity/clarity as visual and verbal proof point", "'Clever choice' framing as the brand's central decision narrative", "Soft pink/white minimalist palette"],
      "Adaptive": ["Mix of studio product shots and lifestyle drink imagery", "Café-style flavor naming (matcha latte, mixed berries)"],
      "Context": ["LGC anti-doping certification (relevant mainly to athlete-facing contexts)", "Bundle/promo pricing mechanics"]
    },

    "BrandIdentity": {
      "personality": "Composed, precise, quietly confident — a brand that signals competence through restraint rather than hype",
      "core_values": ["Purity (100% WPI, minimal additives)", "Precision/quality (Japan-made, '精準萃取技術')", "Smart/informed choice-making"],
      "positioning": "A premium-but-accessible everyday supplement brand for people managing their own health and physique, not a hardcore sports-performance brand",
      "emotional_role": "The quietly smart friend who already found the better option",
      "confidence_style": "Earns trust via credentials and clarity, not bold claims or urgency"
    },

    "AudienceIdentity": {
      "target_audience": "Health-conscious Hong Kong consumers managing weight/physique through daily habit change — broader than elite athletes",
      "aspirational_identity": "Someone who makes informed, slightly superior everyday choices without making a big deal of it",
      "lifestyle_aspiration": "Maintaining a lean, healthy body through small smart substitutions rather than extreme regimens",
      "self_image_projection": "'I'm the person who already knew the better option'",
      "confidence": 0.65
    },

    "CommunicationPhilosophy": {
      "information_density": "Moderate — leads with a clear benefit/claim, backs it with credentials (certifications, % purity), but doesn't over-explain",
      "restraint_level": "High for visual tone, moderate for claims (willing to state precise specs like '80% protein', '100% WPI')",
      "persuasion_style": "Credential- and clarity-led rather than emotional/aspirational hard-sell",
      "cta_aggressiveness": "Low-to-moderate — promotional bundles exist but framing stays soft ('clever choice' rather than urgency/scarcity language)",
      "show_vs_tell": "Tell-led on product specs (numbers, certifications), show-led on lifestyle fit (lifestyle drink photography)",
      "confidence": 0.6
    },

    "EmotionalPositioning": {
      "emotional_tone": "Calm, clean, quietly assured",
      "emotional_maturity": "Adult, non-judgmental — avoids guilt/shame-based weight-loss messaging in its own site copy",
      "emotional_pacing": "Even and steady, not high-urgency",
      "aspiration_style": "Low-key self-improvement rather than dramatic transformation",
      "confidence": 0.6
    },

    "RenderingStyle": {
      "lighting_philosophy": "Bright, clean, even — consistent with e-commerce product photography norms",
      "realism_level": "Clean commercial realism; product-truthful rather than heavily stylized",
      "color_philosophy": "Soft pink/rose + white as the brand's signature pairing; translucency used as a visual proof of purity",
      "atmosphere": "Light, airy, uncluttered",
      "texture_language": "Smooth, clean surfaces; minimal visual noise",
      "polish_level": "High — premium e-commerce finish",
      "confidence": 0.6
    },

    "CompositionBehavior": {
      "hierarchy_sophistication": "Moderate-high — product and key claim dominate, secondary info (certifications, flavor variants) supports without crowding",
      "layout_density": "Low-to-moderate, generous whitespace",
      "whitespace_behavior": "Used deliberately to reinforce 'clean/pure' positioning",
      "eye_flow": "Product-first, claim-second",
      "visual_pacing": "Calm, unhurried",
      "confidence": 0.55
    },

    "CreativeMaturity": {
      "hierarchy_sophistication": "Moderate-high for e-commerce; campaign-level creative maturity unconfirmed (no ad creative reviewed)",
      "restraint_confidence": "High — brand is comfortable not shouting",
      "emotional_subtlety": "Moderate",
      "visual_discipline": "High within e-commerce context",
      "premium_signal_strength": "Moderate-high (Japan-made, certifications, minimalist design)",
      "trend_sophistication": "Unconfirmed — no social/ad creative reviewed directly",
      "confidence": 0.5
    },

    "CoreTensions": [
      {
        "tension": "Premium/clinical credibility (certifications, precision-extraction language, Japan-made) ↔ soft, approachable, café-lifestyle visual identity (pink/white, matcha latte flavor)",
        "supporting_evidence": "Site simultaneously foregrounds LGC certification + '100%頂級高品質' copy and a pastel, lifestyle-drink visual language",
        "confidence": 0.7
      },
      {
        "tension": "Athletic-performance brand roots (anti-doping certification, Muscle Series, 'tone and sculpt' audience language) ↔ this campaign's everyday-office, willpower/snacking framing for non-athletes",
        "supporting_evidence": "Brand's stated audience is fitness enthusiasts/athletes managing physique; the brief's audience is desk-bound professionals fighting impulse snacking, not training",
        "confidence": 0.65
      }
    ],

    "CreativeTradeoffs": [
      {
        "tradeoff": "Calm/restrained brand tone ↔ punchy comparison-meme formats ('This vs That') that perform well in the HK fitness Instagram niche",
        "dominant_side": "Brand restraint should shape *how* the comparison is rendered (clean, composed, not chaotic/loud) even when the format itself is a high-contrast comparison",
        "supporting_evidence": "Site's minimalist, low-density visual language vs. the brief's request for a punchy split-screen 'hidden calories' comparison",
        "confidence": 0.65
      },
      {
        "tradeoff": "Purity/clarity visual signature (translucency, pink/white) ↔ depicting unhealthy comparison foods (siu mai, bubble tea) which are visually 'opposite' to the brand's clean aesthetic",
        "dominant_side": "The CLEVER side of any comparison should carry the brand's signature clean/translucent/pink-white language; the contrasting side can depart from it precisely because it represents the 'before'/undesirable choice",
        "confidence": 0.6
      }
    ],

    "SacredBrandAssets": [
      { "asset": "CLEVER wordmark/logo (clean contemporary sans-serif, all-caps 'CLEVER')", "preservation_note": "Primary brand identifier; reproduce exactly wherever packaging or logo is visible" },
      { "asset": "Soft pink/rose + white color pairing", "preservation_note": "Signature brand palette — should anchor the CLEVER side of any comparison visual" },
      { "asset": "Weight Down packaging (matcha latte / chocolate / yogurt / mixed berries pouches)", "preservation_note": "If a specific flavor pack is shown, treat its label design as an immutable visual reference (see ProductSpec / Reference Asset Manifest at Stage 5 if a reference image becomes available)" },
      { "asset": "Translucency/'Clear' visual motif as purity signal", "preservation_note": "Available as a rendering device for the CLEVER side of a comparison, not mandatory" }
    ],

    "StrategicImplications": [
      { "description": "A 'This vs That' / split-screen comparison format is compatible with the brand's 'Clever choice' framing device, provided the CLEVER side is rendered in the brand's clean, restrained visual language while the contrasting side is allowed to look visually 'busier' or less composed", "supporting_evidence": ["'Clever choice' framing as Core signal", "Creative Tradeoff: purity language vs comparison food"], "implication_confidence": 0.7 },
      { "description": "Because the brand's own positioning skews toward athletes/physique-focused users, this campaign's office-worker/willpower framing represents an audience extension — Strategy should decide how much of the athletic/performance identity to carry forward vs. how much to lead with the broader 'smart everyday choice' framing", "supporting_evidence": ["AudienceIdentity vs. brief's target audience", "Core Tension: athletic roots vs. office framing"], "implication_confidence": 0.7 },
      { "description": "Weight Down packaging (matcha latte / chocolate / yogurt / mixed berries) gives Scene Assembly a concrete, named product to render — if no reference image is supplied, default to a generic but on-brand pink/white pouch with the CLEVER wordmark rather than inventing a flavor", "supporting_evidence": ["SacredBrandAssets: Weight Down packaging", "Observations: 4 confirmed flavors"], "implication_confidence": 0.65 }
    ]
  }
}
```

## Notes

- This is a web-sourced extraction, not a campaign-creative extraction — no prior CLEVER ad/social creative was reviewed. CreativeMaturity and trend-sophistication signals are therefore unconfirmed and capped at moderate confidence.
- The brief itself (Cantonese/Kongish copy, 醒目 Marketer framing, "This vs That" Instagram format) is **not** brand intelligence — it belongs to Stage 1 (Campaign Brief) and Stage 2 (Strategy). It is referenced here only to flag the Core Tensions/Tradeoffs it activates.

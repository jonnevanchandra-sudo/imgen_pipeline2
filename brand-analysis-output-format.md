# Brand Analysis Output Format

Guidance on what `POST /ai/v1/brand/generate-profile` (service-b) actually returns, and which
prompt/format is live vs. dead code. Source of truth: [`service-b/app/prompts/brand_analysis.py`](../service-b/app/prompts/brand_analysis.py)
and [`service-b/app/models/schemas.py`](../service-b/app/models/schemas.py).

## What's actually live

| Prompt | Output shape | Wired to a route? | Used by |
|---|---|---|---|
| `BRAND_PROFILE_SYSTEM` (v1) | Pure Markdown doc | Imported in `brand.py` but never passed to `generate_brand_profile()` — **dead** | Would feed old `BrandHub.tsx` (`data.markdown`), itself unrouted |
| `BRAND_PROFILE_SYSTEM_V2` | Strict JSON (`BrandIntelligenceContract`) | ✅ Yes — `brand.py` → `generate_brand_profile()` | **Live.** Consumed by `BrandHubDemo.tsx` as `res.data.profile` (the page actually mounted at `/brand-hub`) |
| `OUTPUT_FRAMEWORK` | Markdown rendering of the same contract | Imported but never invoked as a prompt — inert | Reference/template only |

`json_to_markdown()` in `openai_service.py` is also fully implemented but never called anywhere —
orphaned from the same earlier markdown-based design.

## 1. Strict JSON (`BRAND_PROFILE_SYSTEM_V2` → `BrandIntelligenceContract`)

Enforced server-side, not just prompted: `generate_brand_profile()` sends
`BrandIntelligenceContract.model_json_schema()` to Poe with `"type": "json_schema", "strict": True`,
and every nested model is a `StrictModel` (`extra="forbid"`) — the LLM cannot return extra or
missing fields.

```json
{
  "observations": ["string", "..."],

  "recurring_patterns": [
    {
      "pattern_name": "string",
      "frequency": "Very High | High | Medium | Low",
      "supporting_observations": ["string"]
    }
  ],

  "inferences": [
    { "insight": "string", "confidence": 0.00, "rationale": "string" }
  ],

  "signal_classification": {
    "core_signals": ["string"],
    "adaptive_signals": ["string"],
    "context_signals": ["string"]
  },

  "brand_identity": {
    "personality": ["string"],
    "core_values": ["string"],
    "positioning": "string",
    "emotional_role": "string",
    "confidence_style": "string"
  },

  "audience_identity": [
    {
      "target_audience": "string",
      "lifestyle_aspiration": "string",
      "status_signaling": "string",
      "self_image_projection": "string",
      "aspirational_identity": "string"
    }
  ],

  "communication_philosophy": {
    "information_density": 0,
    "restraint_level": 0,
    "persuasion_style": 0,
    "cta_aggressiveness": 0,
    "show_vs_tell": 0
  },

  "emotional_positioning": {
    "emotional_tone": ["string"],
    "emotional_maturity": ["string"],
    "emotional_pacing": ["string"],
    "aspiration_style": ["string"]
  },

  "rendering_style": {
    "lighting_philosophy": "string",
    "realism_level": "string",
    "color_philosophy": "string",
    "atmosphere": "string",
    "texture_language": "string",
    "polish_level": "string"
  },

  "composition_behavior": {
    "hierarchy_sophistication": "string",
    "layout_density": "string",
    "whitespace_behavior": "string",
    "eye_flow": "string",
    "visual_pacing": "string"
  },

  "creative_maturity": {
    "hierarchy_sophistication": "string",
    "restraint_confidence": "string",
    "emotional_subtlety": "string",
    "visual_discipline": "string",
    "premium_signal_strength": "string",
    "trend_sophistication": "string"
  },

  "core_tensions": [
    { "force_a": "string", "force_b": "string", "supporting_evidence": ["string"], "confidence": 0.00 }
  ],

  "creative_tradeoffs": [
    { "gain": "string", "sacrifice": "string", "dominant_choice": "string", "supporting_evidence": ["string"], "confidence": 0.00 }
  ],

  "sacred_brand_assets": {
    "visual": ["string"],
    "emotional": ["string"],
    "narrative": ["string"]
  },

  "strategic_implications": [
    { "hypothesis": "string", "supporting_evidence": ["string"], "confidence": 0.00 }
  ]
}
```

`communication_philosophy` fields are ints `0-100` (`Scale0To100`). All `confidence` fields are
floats `0.00-1.00`. This is exactly what `BrandHubDemo.tsx` reads as `res.data.profile` (passed
through `normalize()` for safety, then rendered field-by-field).

## 2. Markdown version (`OUTPUT_FRAMEWORK`)

Same contract, same field order, rendered as Markdown instead of JSON. **Not invoked anywhere
right now** — kept here as the intended companion format if markdown rendering is reintroduced.

```markdown
# [Insert Brand Name] Brand Intelligence Contract

## Metadata
- Brand / Market Context / Reference Set / Framework Version

# Observations
1. [observation] ...

# Recurring Patterns
## [Pattern Name] — Frequency, Evidence

# Inferences
### [Key Insight] — Confidence, Rationale

# Brand Identity
- Personality, Core Values, Positioning, Emotional Role

# Audience Identity
- Aspirational Identity

# Communication Philosophy
- Information Density, Restraint Level, Persuasion Style, Show vs Tell

# Emotional Positioning
- Tone, Maturity, Aspiration Style

# Rendering Style
- Visual Philosophy, Atmosphere, Color/Texture

# Composition Behavior
- Visual Hierarchy, Pacing

# Core Tensions
1. [Force A] ↔ [Force B] (Confidence: ...)

# Creative Tradeoffs
1. [Gain] ↔ [Sacrifice] — Dominant

# Sacred Brand Assets
- Visual, Emotional, Narrative

# Strategic Implications
1. [Hypothesis] (Confidence: ...)

# Creative Summary
> North Star statement
```

## Don't confuse with `BRAND_PROFILE_SYSTEM` (v1)

`BRAND_PROFILE_SYSTEM` (lines 48-106 of `brand_analysis.py`) is a *different*, older markdown
document with its own section set (Brand Overview, Target Audience, Visual Identity Guidelines,
Content Strategy, Competitive Landscape, etc.) — it's tied to the dead `BrandHub.tsx` page, not
the `BrandIntelligenceContract` schema. `OUTPUT_FRAMEWORK` is the markdown twin of the JSON
contract above; `BRAND_PROFILE_SYSTEM` is unrelated legacy content.

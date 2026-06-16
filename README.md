# AI Advertising Pipeline

A structured, multi-stage framework for producing AI-generated advertising imagery. Each stage owns exactly one type of decision and feeds its output contract into the next stage.

## How It Works

```
Brand Intelligence → Campaign Brief → Strategy → Narrative → Art Direction
                                                                    ↓
                         Prompt Compiler ← Synthesis ← Composition & Rendering
                               ↓                              ↓
                         VisualPrompt                   Scene Assembly
```

Run the stages in order — each one consumes the output of the previous.

## Stages

| File | Stage | What It Decides |
|------|-------|-----------------|
| `0. Brand Intelligence.v2.md` | 0 | What the brand actually is (extracted from real materials) |
| `1.1 Campaign_Brief.md` | 1 | Campaign facts only — no strategy, no execution |
| `1.5 Visual_Discovery.md` | 1.5 | Client aesthetic references (async, optional) |
| `2. Strategy.md` | 2 | Which brand dimensions to activate for this campaign |
| `3. Narrative.md` | 3 | Emotional arc and viewer transformation |
| `4. Art-Direction-framework-v3.md` | 4 | Visual concept and structural density |
| `5a Image_Analysis.md` | 5a | Extract attributes from client reference images (optional pre-step) |
| `5.2.5 Scene-Assembly.md` | 5 | Scene blueprint — entities, spatial layout, reference asset locking |
| `5.5 Client_Preference_Ingestion.md` | 5.5 | Codify client picks from Visual Discovery (optional) |
| `6.1 Composition_Rendering.md` | 6 | Camera, lighting, depth of field, materials |
| `7.1 Synthesis.md` | 7 | Consolidate all contracts, resolve conflicts |
| `8.2.1 Prompt_Compiler.md` | 8 | Translate to final image generation prompt |

**Use the highest-numbered version of each stage** (e.g. `5.2.5` over `5.2` over `5`). Lower versions are kept as historical reference.

## Prompt Compiler Variants

- `8.1.1` — flat prose string; works with Midjourney / DALL-E / Flux
- `8.2.1` — JSON priority blocks for GPT Image 2.0 **(preferred)**

## Trial Runs

| Folder | Brand | Notes |
|--------|-------|-------|
| `Nike_Trial/` | Nike HK | Multiple trials; Gen Z Chill Run Club campaign |
| `Clever_Trial/` | CLEVER Protein | Clear WPI; HK OL afternoon tea concept |
| `Protein_Trial/` | Generic protein | Brand-independent assumed BrandContract |
| `Giga_Trial/` | GigaSports | Pickleball Club; active networking positioning |
| `Gym_Trial/` | Gym brand | Gym lifestyle |
| `World_Cup/` | HKFA | World Cup qualifier campaign |

## Core Rule

Every stage may **influence** downstream decisions but must **never directly make** them. Art Direction does not specify lighting. Narrative does not specify camera angles. Violations contaminate the layer boundary and make the pipeline unpredictable.

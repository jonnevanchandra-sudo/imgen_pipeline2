# AI Advertising Pipeline

A structured, multi-stage framework for producing AI-generated advertising imagery. Each stage owns exactly one type of decision and feeds its output contract into the next stage.

## How It Works

```
Brand Intelligence
        ↓
Campaign Brief
        ↓
Strategy
        ↓
Narrative
        ↓
Art Direction
        ↓
Image Analysis
        ↓
Scene Assembly
        ↓
Composition & Rendering
        ↓
Synthesis
        ↓
Prompt Compiler
        ↓
VisualPrompt
```

## Stages

| File | Stage | What It Decides | Inputs |
|------|-------|-----------------|--------|
| `0. Brand Intelligence.v2.md` | 0 | What the brand actually is (extracts data from website, images, etc) | Website link, images uploaded |
| `1.2 Campaign_Brief.md` | 1 | Campaign facts only | prompt.md (result from campaign brainstorming) |
| `2. Strategy.md` | 2 | Which brand dimensions to activate for this campaign | Brand Contract and Campaign Contract |
| `3. Narrative.md` | 3 | Emotional arc and viewer transformation | Brand Contract and Strategy Contract |
| `4. Art-Direction-framework-v3.md` | 4 | Visual interpretation and structural density | Strategy Contract and Narrative Contract |
| `5a Image_Analysis.md` | 5a | Extract attributes from client reference images (optional pre-step, already combined in 5.2) | Reference images uploaded by the user |
| `5.2 Scene-Assembly.md` | 5 | Entities, spatial layout (relative scale), reference asset locking | (Global Pipeline State) Art Direction Contract, Campaign Contract |
| `6.1 Composition_Rendering.md` | 6 | Camera, lighting, depth of field, materials | Scene Contract |
| `7.1 Synthesis.md` | 7 | Consolidate all contracts, resolve conflicts | Campaign Contract, Brand Contract, Strategy Contract, Narrative Contract, Art Direction Contract, Scene Contract, Composition Rendering Contract |
| `8.2.1 Prompt_Compiler.md` | 8 | Translate to final image generation prompt | Synthesis Contract |


## Prompt Compiler Variants

- `8.1.1` — flat prose string
- `8.2.1` — JSON priority blocks

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

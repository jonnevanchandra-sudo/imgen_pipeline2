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
| `8.1.1 Prompt_Compiler.md` | 8 | Translate to final image generation prompt | Synthesis Contract |

## Stages Explanation
- 0.Brand Intelligence.v2.md
      Inputs : Link and images from the brand
      Outputs : Contract.md (style of the brand)
            - Background
            - Font text/color
            - Subjects
            - etc
- 1.2 Campaign_Brief.md
      Input : prompt.md (result from campaign brainstorming)
      Output : Campaign Contract
      What's new in 1.2: added 'Product Spec' in "Mandatory Requirements". It looks at the reference image and give it treatment if whether it's a brand asset reference (e.g. logo, model face, product) or it's an inspiration.
- 2.Strategy.md
      Inputs : Brand Contract & Campaign Contract
      Output : Strategy Contract
      Idea :
            - Objective of this campaign
            - Contextual Tension (current state vs desired state)
            - Meaning behind it
- 3.Narrative.md
      Inputs : Brand Contract & Strategy Contract
      Output : Narrative Contract
      Idea : Goal of this is to understand what transformation do we want the viewer to have. From who he/she was --> to who he/she became
4.Art-Direction-framework-v3.md
      Inputs : Strategy Contract and Narrative Contract
      1. Strategy Contract
            - Strategic Direction : goal & the direction for this campaign
            - Identity Migration : the "identity" we want to build onto the customer
      2. Narrative Contract
            - Narrative Lens Selection
            - Current emotional State
            - Physchological Friction
            - Desired Transformation
            - Viewer Takeaway
            All of which is talking "What do we want for the viewer to take from this image?"
            Objective is: Emotional Meaning --> Visual Interpretation
5a.Image_Analysis.md
      Notes : Also in 5.2 Scene Assembly, no need separate file. Still in consideration if we should separate it from scene assembly or not. In Scene Assembly, this is Reference Asset Extraction Block
      Inputs : Reference Images, Brand Contract, Campaign contract
      Output : 05a_Image Analysis Contract
      How it works:
            1. Classify
                  - Identity-Bearing
                  - Brand-Bearing
                  - Environmental
                  - Product/Equipment
                  - Style Reference
            2. Assign Entity ID
            3. Extract Observable Attributes
            4. Separate Immutable vs Flexible (Attributs not style) --> Let the AI infer itself which is which accroding to the brand & campiagn contract
      Goal is to understand what it IS, not what to do
5.2Scene-Assembly.md
      Inputs : Art Direction, Campaign Contract, and Image Analysis Contract
      New : 
      1. Reference Asset Extraction Block (Same as 5a)
      2. Reference/Asset Manifest in output
            -> Scene Contract carries a Reference Asset Manifest
                  -> List of files to attach to the image generation call to replicate the pictures
      Job of Scene Assembly :
            - What each entity is doing e.g. Holding a cup, etc
            - Relative Scale (e.g. human to a machine)
            - Generation Requirement e.g. Clean background
6.1Composition_Rendering.md
      Inputs : Scene Contract
      Job of Composition Rendering:
            - Lighting hierarchy
            - Lighting Idea : Attention guidance (where should the eye land first), how to capture the emotional feelings
            - Rendering behaviour
            - Camera Behaviour
            Sensory embodiment : making the images feel real (light hitting the skin, fabric texture, etc)
7.1 Synthesis.md
      Inputs : All contract
      Job : Summarize everything



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

# Brand Intelligence Field Traceability

Traces every field in the `BrandContract` output schema (`0.Brand Intelligence.v2.md`) against the explicit "Inputs" sections of every downstream layer (Strategy, Narrative, Art Direction, Scene Assembly, Composition & Rendering, Synthesis) to determine which fields actually travel down the pipeline vs. which dead-end at Stage 0.

Method: only counted as "passed down" if a downstream file explicitly names the field (or a clearly matching alias) in its own `Inputs` / `Consumed Inputs` / validation sections. Fields that could *plausibly* inform a downstream decision but aren't explicitly cited are counted as not passed down — implicit inheritance isn't traceable and isn't enforced by the framework text.

---

## Fields that DO travel (explicitly named downstream)

| BrandContract Field | Where it's explicitly consumed |
|---|---|
| **BrandIdentity** | Strategy (`Compatibility Mapping`, `ActivatedDimensions.source_anchors`, `StrategicConstraints.protected_brand_truths`) → Narrative (`Consumed Inputs`, `BrandAlignment` validation) → Art Direction (as "Core Brand Identity" guardrail + compatibility validation) → Synthesis (loosely, as "Brand Contract: identity") |
| **AudienceIdentity** | Strategy (`Compatibility Assessment/Mapping`) → Narrative (`Consumed Inputs`, "Compatible with Audience Identity") → Art Direction (compatibility validation only — not listed as a generative input) |
| **CommunicationPhilosophy** | Strategy only (`Compatibility Mapping`). Never named again downstream. |
| **CoreTensions** | Strategy only (`Compatibility Mapping`). Explicitly distinguished there from Strategy's own "Contextual Tensions." Never named again downstream. |
| **SacredBrandAssets** | Art Direction only, and only as an "Optional Input (Brand Preservation Guardrail)" — used strictly for validation, never as a creative source. Note: the separate `BRAND_ASSETS` prompt block that survives to the Prompt Compiler comes from **uploaded reference images at Scene Assembly (5.2)**, not from this field — a different mechanism that happens to share a name. |

## Fields that do NOT travel anywhere (dead-end at Stage 0)

| BrandContract Field | Notes |
|---|---|
| **EmotionalPositioning** | Never named as an input anywhere — including Narrative, the layer literally titled "Emotional Interpretation." Narrative's `Consumed Inputs` list cites only Brand Identity + Audience Identity from the Brand Contract. Most surprising gap given the direct name match to Narrative's own purpose. |
| **RenderingStyle** | Never named downstream. Composition & Rendering (the layer that owns lighting/material/atmosphere/optical decisions) lists its inputs as *only* Scene Blueprint, Reality Model, Preservation Contracts, Generation Requirements — all sourced from Scene Assembly, not Brand Intelligence. |
| **CompositionBehavior** | Never named downstream — not even by the layer named "Composition & Rendering," whose hierarchy/attention/flow logic derives from Narrative/Preservation/Emotional/Environmental sources, never from this field. |
| **CreativeMaturity** | Never named anywhere downstream. |
| **CreativeTradeoffs** | Never named anywhere downstream. |
| **StrategicImplications** | Framed as "hypotheses for downstream systems" in Stage 0, but no downstream file cites it by name. |
| **RecurringPatterns** | Never referenced downstream — feeds only Stage 0's own reasoning chain (Inferences, Tensions, Tradeoffs). |
| **Inferences** | Same — internal evidence trail, doesn't travel. |
| **SignalClassification** (Core / Adaptive / Context) | Never referenced by name downstream, though its stated purpose is "determines how downstream systems should interpret and preserve signals." |
| **Observations** | Raw evidence layer; stays at Stage 0. |
| **Metadata** | Administrative; not expected to travel. |

---

## The pattern

Only the "identity/positioning" cluster (`BrandIdentity`, `AudienceIdentity`) and, weakly, `CommunicationPhilosophy` / `CoreTensions` survive past Strategy — and none of them are named explicitly beyond Art Direction. Everything visual or tonal that Brand Intelligence produces — **RenderingStyle, EmotionalPositioning, CompositionBehavior, CreativeMaturity** — has no explicit wire to the layers that would logically consume it (Narrative for emotion, Composition & Rendering for visual rendering). Those downstream layers instead re-derive rendering and emotional decisions from their own internal systems (Narrative's Emotional Intensity System, Composition & Rendering's Hierarchy/Rendering Inference), independent of what Brand Intelligence originally observed about the brand.

## Layer-by-layer input citations (source of truth for the table above)

- **Strategy** (`2. Strategy.md`) — `Compatibility Mapping` explicitly evaluates: Brand Identity, Audience Identity, Communication Philosophy, Core Tensions.
- **Narrative** (`3. Narrative.md`) — `Consumed Inputs`: Activated Dimensions, Behavioral Positioning, Identity Migration, Strategic Direction, Brand Identity, Audience Identity.
- **Art Direction** (`4. Art-Direction-framework-v3.md`) — Required Inputs come only from Strategy/Narrative contracts. Optional Inputs (guardrails, not creative sources): Sacred Brand Assets, Brand Preservation Rules, Core Brand Identity.
- **Scene Assembly** (`5.2 Scene-Assembly.md`) — Inputs: Global Pipeline State, Art Direction outputs, Campaign Contract `ProductSpec`, Uploaded Reference Images. No Brand Intelligence field named directly.
- **Composition & Rendering** (`6.1 Composition_Rendering.md`) — Inputs: Scene Blueprint, Reality Model, Preservation Contracts, Generation Requirements — all from Scene Assembly. No Brand Intelligence field named at all.
- **Synthesis** (`7.1 Synthesis.md`) — Cites "Brand Contract: truth, identity, positioning, signals, boundaries" as a generic aggregated bucket, not a 1:1 pass-through of the named BrandContract schema fields.

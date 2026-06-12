# Synthesis Contract
**Brand:** Nike
**Campaign:** Nike Chill Run Club
**Framework:** Synthesis Framework v7.1
**Stage:** 7 — Communication Resolution

---

```json
{
  "SynthesisContract": {

    "InputsConsumed": {
      "BrandContract": "Nike Brand Intelligence Contract — v2",
      "CampaignContract": "Nike Chill Run Club CampaignContract v1.1 — Trial 03",
      "StrategyContract": "Nike Chill Run Club StrategyContract — Trial 03",
      "NarrativeContract": "Nike Chill Run Club NarrativeContract — Trial 03",
      "ArtDirectionContract": "Nike Chill Run Club ArtDirectionContract — Trial 03",
      "SceneContract": "Nike Chill Run Club SceneContract v5.2 — Trial 03",
      "CompositionRenderingContract": "Nike Chill Run Club CompositionRenderingContract — Trial 03"
    },

    "ExecutiveSummary": "A night photograph of Karina (from aespa) and the user (male, reference_asset_01) running together through Hong Kong at night — harbourfront or waterfront path, city lights glowing in the background. Both are mid-stride, wearing Nike Alphafly 3 in University Red. Their faces carry the specific ease of a mental reset that is actively happening — the workday is gone. The social warmth between them is genuine and visible. This image says: this is what choosing yourself after work looks like, and it looks like this.",

    "CommunicationHierarchy": [
      {
        "rank": 1,
        "signal": "Present-state liberation on both faces — the specific ease of a mind that has stopped processing the workday",
        "delivery_mechanism": "Face expression readable at scroll speed; both subjects' faces in sharp foreground focus",
        "source": "Narrative + Composition"
      },
      {
        "rank": 2,
        "signal": "Genuine social warmth between subjects — two people who are here together, not running near each other incidentally",
        "delivery_mechanism": "Compositional proximity, body language, and social energy legible at mid-frame",
        "source": "Strategy (Community Belonging) + Art Direction (Shared Claim)"
      },
      {
        "rank": 3,
        "signal": "Nike Alphafly 3 in the stride — product recognition without product-hero composition",
        "delivery_mechanism": "Shoe in sharp focus mid-stride; midsole profile and Air Zoom pod windows readable in lower frame; eye arrives at shoe by tracing the running body",
        "source": "Campaign + Scene"
      },
      {
        "rank": 4,
        "signal": "HK night cityscape — this liberation is available in your city, tonight",
        "delivery_mechanism": "City lights as warm background bokeh; warm-cool night atmosphere; unmistakably HK",
        "source": "Brief + Art Direction"
      }
    ],

    "ConflictResolutions": [
      {
        "conflict": "Nike Alphafly 3 is an elite racing shoe; the Chill Run Club brief demands accessible, non-competitive framing",
        "resolution": "The shoe's visual aspiration is offset by the subjects' accessible, social running posture and expression. The Alphafly's presence communicates Nike's performance credentials while the subjects' body language (comfortable pace, social ease) communicates accessibility. Tension is intentional — aspiration + accessibility coexist.",
        "authority": "CampaignContract + StrategyContract"
      },
      {
        "conflict": "Night setting reduces face readability; HierarchyPlan requires both faces to be Primary",
        "resolution": "Camera must be close enough (near-to-medium distance) and subjects lit by warm city ambient to ensure faces read before city background. Subjects are brighter than background by foreground depth position and ambient light advantage.",
        "authority": "CompositionRenderingContract"
      }
    ],

    "RedundancySuppression": [
      "Do not describe entity_01's physical appearance in text — reference_asset_01 is the source of truth for his face and build",
      "Do not describe Karina's appearance in text — generator uses its own training knowledge of her likeness; name only",
      "Do not re-specify HK landmark details that the generator can infer from 'HK harbourfront night' — specificity without fabrication"
    ],

    "ObservableHumanSignals": {
      "entity_01": "Face: open, composed, slight softening around the eyes — the specific ease of someone whose internal monologue has quieted because the run has taken over. Not smiling for a camera. Not grimacing with effort. Just: here.",
      "entity_02": "Face: same present-state liberation quality. Natural expression in motion — not posed. The energy between her and entity_01 is visible in their shared spatial ease and synchronized stride.",
      "social_signal": "Two people who have found the same rhythm. Side by side, moving together through a city that belongs to them right now."
    },

    "PreservedConstraints": [
      "entity_01 face and build: reproduce from reference_asset_01 only — no training data generation for his identity",
      "entity_02 identity: Karina from aespa — name only in prompt, no text description",
      "Nike Alphafly 3: tall ZoomX midsole + twin forefoot Air Zoom pod windows must be legible",
      "Night setting: HK night, city lights, warm ambient — not day, not golden hour",
      "Social energy: genuine connection between subjects must be present — not neutral parallel strangers",
      "Accessible running posture: comfortable pace, no athletic intensity, no competitive body language"
    ],

    "MemoryAnchor": "That Nike ad with Karina and that guy running through Hong Kong at night — they looked like they'd left the whole week behind, and the city was just theirs.",

    "ReferenceAssetManifest": [
      {
        "asset_id": "asset_01",
        "filename": "user_reference_portrait.jpg",
        "type": "Identity-Bearing",
        "prompt_reference_id": "reference_asset_01",
        "attach_to_api_call": true,
        "strictness": "Strong Match"
      }
    ]

  }
}
```

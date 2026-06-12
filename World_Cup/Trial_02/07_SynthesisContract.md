# Synthesis Contract
**Brand:** Hong Kong Football Association (HKFA)
**Campaign:** Hong Kong World Cup 2026 — Team Hoodie Launch
**Framework:** Synthesis Framework v7.1
**Stage:** 7 — Communication Resolution

---

```json
{
  "SynthesisContract": {

    "InputsConsumed": {
      "BrandContract": "HKFA Brand Intelligence Contract",
      "CampaignContract": "HKFA World Cup 2026 CampaignContract v1.1 — Trial 01",
      "StrategyContract": "HKFA World Cup 2026 StrategyContract — Trial 01",
      "NarrativeContract": "HKFA World Cup 2026 NarrativeContract — Trial 01",
      "ArtDirectionContract": "HKFA World Cup 2026 ArtDirectionContract — Trial 01",
      "SceneContract": "HKFA World Cup 2026 SceneContract v5.1 — Trial 01",
      "CompositionRenderingContract": "HKFA World Cup 2026 CompositionRenderingContract — Trial 01"
    },

    "ExecutiveSummary": "An evening photograph of one or two HK young adults wearing the Hong Kong National Team FIFA World Cup 2026 Hoodie in Dragon Red, standing in a recognizable Hong Kong urban environment — harbourfront or city street, with the HK skyline visible. Their faces carry quiet, personal pride — not triumph, not performance, not neutral. The dragon crest is legible on the left chest. The red dominates the frame. The city behind them is unmistakably Hong Kong. The image says: this is what it looks like when Hong Kong wears its own identity. Wear it.",

    "CommunicationHierarchy": [
      {
        "rank": 1,
        "signal": "Quiet personal pride on the subject's face — the expression of someone who knows where they are from",
        "delivery_mechanism": "Face in crisp foreground focus, large enough to read expression at Instagram mobile scroll speed",
        "source": "Narrative + Art Direction"
      },
      {
        "rank": 2,
        "signal": "Dragon Red hoodie as visible identity declaration — this specific red, in this city, on this person",
        "delivery_mechanism": "Red is the dominant color mass in the frame; hoodie fills the subject's body; eye arrives at the color before any other detail",
        "source": "Campaign + ProductSpec + Strategy"
      },
      {
        "rank": 3,
        "signal": "HKFA dragon crest — the mark that makes this the HK hoodie and not any red hoodie",
        "delivery_mechanism": "Legible on left chest at subject's scale; reads after the red is registered; confirms the identity claim",
        "source": "ProductSpec"
      },
      {
        "rank": 4,
        "signal": "HK at night — this city, this moment, this is where the pride lives",
        "delivery_mechanism": "HK skyline or harbour in warm background bokeh; unmistakably HK city atmosphere extends behind the subject",
        "source": "Narrative + Environment"
      }
    ],

    "ConflictResolutions": [
      {
        "conflict": "Product must be legible (crest, colorway) but must not read as a product catalog or merchandise photo",
        "resolution": "The hoodie is worn by a real person in a real city. The product communicates through the person — not in isolation. The face is Primary hierarchy; the crest is High but arrived at via the person, not positioned independently. Product photography energy is explicitly rejected.",
        "authority": "Art Direction + Narrative"
      },
      {
        "conflict": "Campaign targets non-football-fans, but the product is explicitly football-branded (HKFA crest, World Cup patch)",
        "resolution": "The image makes no reference to football activity, football skill, or match context. The subjects are in the city, not near a stadium or pitch. The pride is cultural identity pride, not sports fan pride. The crest communicates HK identity first; the football connection is present but not the entry point.",
        "authority": "Strategy + CampaignContract"
      },
      {
        "conflict": "Evening/night setting reduces face legibility; faces are Primary hierarchy",
        "resolution": "Warm city ambient streetlamp light is the key light source on faces — warm amber, enriching skin tone. Camera distance (medium) ensures faces are large enough in frame to read despite lower ambient. Background city lights as bokeh provide depth without competing.",
        "authority": "CompositionRenderingContract"
      }
    ],

    "RedundancySuppression": [
      "Do not describe subjects' exact faces or physical appearance — generator determines realistic HK young adult appearance; no text description of specific features",
      "Do not over-specify the HK background — 'HK harbourfront at night' or 'HK urban street at night' is sufficient; specific landmark detail is unnecessary and risks hallucination",
      "Do not re-specify product features that the model name already implies — only the non-obvious visual identifiers (crest, white trim, World Cup patch) need explicit mention"
    ],

    "ObservableHumanSignals": {
      "entity_01": "Face: quiet, settled confidence — the specific expression of someone who has put on something that belongs to them. Not smiling for the camera. Not performing pride. Not neutral. The warmth is in the eyes: present, grounded, this is mine.",
      "entity_02_if_present": "Face: same quality — personal, unperformed pride. If two subjects are visible, the shared red between them communicates collective belonging without requiring interaction or performance.",
      "body_language": "Standing or in easy motion — relaxed, grounded, comfortable in the city. Not posed for athletic achievement. Not fashion-posing. Just: here, in their city, in their red."
    },

    "PreservedConstraints": [
      "HK World Cup 2026 hoodie: Dragon Red body, HKFA dragon crest on left chest (legible), white trim accents, 香港 HONG KONG text, World Cup 2026 patch on right sleeve, pullover silhouette",
      "Subject expression: quiet personal pride — not triumph, not neutral, not performance",
      "Red colorway dominance: Dragon Red must be the dominant color mass in the frame",
      "HK environment: evening/night setting, city lights active, unmistakably HK — not generic Asian city",
      "No football activity framing: no stadium, no pitch, no match-day context — urban street or harbourfront only",
      "No product isolation: hoodie is worn by a real person in a real place — not displayed, not modeled on a mannequin"
    ],

    "MemoryAnchor": "That HKFA World Cup campaign — the one with the person in the red hoodie in front of HK at night. Didn't need to say anything. The crest on the chest and the city behind them said it all."

  }
}
```

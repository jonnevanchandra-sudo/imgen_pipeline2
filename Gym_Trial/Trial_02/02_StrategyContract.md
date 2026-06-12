# Strategy Contract — FIT24 (Stage 2)

Framework: `2. Strategy.md`
Inputs: BrandContract (Stage 0) + CampaignContract (Stage 1)
Decision Type: Meaning Selection — which brand dimensions this campaign activates. No narrative, no visuals.

```json
{
  "StrategyContract": {
    "ActivatedDimensions": [
      "Atmosphere/Environment — bright, glass-walled space with a green outlook as the primary differentiator",
      "Modernity — clean industrial-modern design (exposed ceiling, glass, polished floor) signals a contemporary, well-kept facility",
      "Accessibility (implied) — '24' branding implied in the background, supporting a flexible-schedule message without being the headline"
    ],

    "ContextualTensions": [
      {
        "tension": "Modern/premium-feeling glass-and-concrete space ↔ everyday accessibility implied by '24' branding",
        "activation": "Show the space in genuine morning use — one person training calmly — so the premium environment feels reachable and ordinary, not exclusive."
      },
      {
        "tension": "Distinctive window-wall view (strong visual hook) ↔ risk of the environment overshadowing the human moment",
        "activation": "Frame the person mid-workout facing the windows so the view reads as part of *their* experience, not a standalone real-estate shot."
      }
    ],

    "BehavioralPositioning": "FIT24 behaves like a calm, bright start to the day — training here is framed as a refreshing routine, not a separate 'workout world' disconnected from daily life.",

    "IdentityMigration": {
      "CurrentIdentity": "Someone whose idea of 'the gym' is a cramped, fluorescent-lit room they have to push themselves to enter",
      "DesiredIdentity": "Someone who starts their day at a bright, open space with a view — training feels energizing rather than draining"
    },

    "StrategicDirection": "Depict a single person training on or near the treadmill row, facing the floor-to-ceiling windows and green outlook, inside the actual FIT24 space — the FIT24 logo and window-wall view recognizable but framed as the backdrop to a calm, energizing personal moment, not a venue showcase.",

    "MeaningConstraints": {
      "forbidden_meaning": [
        "EliteAthleticism — competitive intensity or extreme exertion framing",
        "GenericStockGymFeel — the space must read as THIS location (window wall, green outlook, FIT24 logo), not an interchangeable stock gym",
        "RealEstateShowcase — the environment must support a human moment, not read as an empty architectural/property photo"
      ],
      "forbidden_positioning": [
        "ProductHero equipment shot — treadmills support the scene, they are not the subject",
        "CrowdedGroupShot — single individual only"
      ]
    }
  }
}
```

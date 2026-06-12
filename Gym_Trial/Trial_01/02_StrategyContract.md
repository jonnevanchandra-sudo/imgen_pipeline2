# Strategy Contract — Anytime Fitness Sai Ying Pun (Stage 2)

Framework: `2. Strategy.md`
Inputs: BrandContract (Stage 0) + CampaignContract (Stage 1)
Decision Type: Meaning Selection — which brand dimensions this campaign activates. No narrative, no visuals.

```json
{
  "StrategyContract": {
    "ActivatedDimensions": [
      "Accessibility/Flexibility — 24/7 access as the literal solution to a schedule-irregular life",
      "Proximity/Convenience — genuinely walkable from HKU, removing the 'special trip' barrier",
      "Approachability — modern equipment framed as welcoming, not intimidating, to first-timers"
    ],

    "ContextualTensions": [
      {
        "tension": "Modern/Premium-feeling equipment ↔ 'Anyone can walk in' accessibility",
        "activation": "Show the equipment in relaxed, in-use context — a single student using it naturally — rather than as a showroom hero shot. Capability is present but never the headline."
      },
      {
        "tension": "Franchise brand consistency (AF purple/monogram) ↔ Local relevance (this specific club, near HKU)",
        "activation": "The recognizable local space leads; the AF monogram and purple accent register as a quiet confirmation of brand in the background, not the visual subject."
      }
    ],

    "BehavioralPositioning": "The gym behaves like an always-available extension of student life — the way a 24-hour library or convenience store is simply 'there' whenever needed, with no scheduling friction.",

    "IdentityMigration": {
      "CurrentIdentity": "Someone who keeps meaning to start going to the gym, but whose schedule never seems to line up with it",
      "DesiredIdentity": "Someone who just goes when they can — training is a normal, low-effort part of their day, not a planned event"
    },

    "StrategicDirection": "Depict a single HKU-aged student training, unhurried and focused, inside the actual Anytime Fitness Sai Ying Pun space — the AF branding and recognizable equipment present and identifiable, but secondary to the candid human moment. The viewer should feel 'this specific gym is right there, and it's open whenever I am.'",

    "MeaningConstraints": {
      "forbidden_meaning": [
        "EliteAthleticism — competitive intensity, bodybuilding, or performance-obsessed framing",
        "Intimidation/Exclusivity — anything that signals 'this space is not for beginners'",
        "GenericStockGymFeel — the space must read as THIS gym, not an interchangeable stock gym"
      ],
      "forbidden_positioning": [
        "ProductHero equipment shot — equipment supports the scene, it is not the subject",
        "CrowdedGroupShot — acquisition message is personal and individual, not a class/community event"
      ]
    }
  }
}
```

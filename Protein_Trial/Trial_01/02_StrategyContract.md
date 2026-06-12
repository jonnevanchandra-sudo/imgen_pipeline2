# Strategy Contract — Natural Protein Powder (Stage 2)

Framework: `2. Strategy.md`
Inputs: BrandContract (Stage 0, assumed mode) + CampaignContract (Stage 1)
Decision Type: Meaning Selection — which brand dimensions this campaign activates. No narrative, no visuals.

```json
{
  "StrategyContract": {
    "ActivatedDimensions": [
      "TastePleasure — enjoyment as the primary brand truth",
      "IngredientHonesty — naturalness proven by recognizable real food, not claimed by copy",
      "EverydayBelonging — lives in the kitchen and the daily routine, not the gym"
    ],

    "ContextualTensions": [
      {
        "tension": "Indulgence ↔ Health",
        "activation": "Refuse the tradeoff. The campaign's meaning IS the collapse of this tension: what's good for you is also what you'd choose for pleasure."
      },
      {
        "tension": "Supplement category ↔ Food identity",
        "activation": "Behave entirely as food. Every category code (scoops of beige dust, shaker bottles, gym counters) is replaced by a food code (smoothie, kitchen, real produce)."
      }
    ],

    "BehavioralPositioning": "The product behaves like an ingredient in a beloved daily ritual — something made and savored, not consumed as a dose.",

    "IdentityMigration": {
      "CurrentIdentity": "Someone who tolerates healthy products as a necessary compromise",
      "DesiredIdentity": "Someone who refuses to compromise — whose healthy choices are also their favorite ones"
    },

    "StrategicDirection": "Stage the moment of genuine taste pleasure, with naturalness present as visible evidence rather than stated claim. The viewer should feel appetite first and read 'natural' second — pleasure converts, ingredients justify.",

    "MeaningConstraints": {
      "forbidden_meaning": [
        "AthleticPerformance — muscle, training, exertion as the reason to buy",
        "Discipline/Sacrifice — health as effortful virtue",
        "ClinicalEfficacy — lab-coded purity or quantified claims"
      ],
      "forbidden_positioning": [
        "SupplementHero — the pack as clinical product shot",
        "TransformationPromise — before/after body framing"
      ]
    }
  }
}
```

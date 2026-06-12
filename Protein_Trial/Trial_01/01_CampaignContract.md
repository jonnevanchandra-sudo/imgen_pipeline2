# Campaign Contract — Natural Protein Powder (Stage 1)

Framework: `1. Campaign_Brief.md`
Input: Raw campaign intent — "advertise a protein powder; highlight that it tastes good and is made from natural ingredients."

**Note on 1.1:** `ProductSpec` (named product model) is not used — there is no specific named product/colorway to lock. The product pack is a required asset but generic. When real packaging exists, rerun via `1.1` + reference image so Scene Assembly can lock it.

```json
{
  "CampaignContract": {
    "BusinessObjective": "Drive first-trial consideration by repositioning the product against the category's core objection: that protein powder tastes bad and is full of artificial ingredients.",

    "MessageHierarchy": [
      { "rank": 1, "message": "It genuinely tastes good — enjoyment, not tolerance." },
      { "rank": 2, "message": "It is made from natural, recognizable ingredients — real food, nothing artificial." },
      { "rank": 3, "message": "It fits effortlessly into an ordinary daily routine." }
    ],

    "AudienceContext": {
      "primary": "Health-conscious adults 25–40; eat well, move regularly, not gym-identified",
      "current_belief": "Protein powder is a chalky, artificial compromise you put up with",
      "desired_belief": "This one is real food that I actually look forward to"
    },

    "OfferDefinition": {
      "product": "Protein powder (unnamed brand), natural ingredients, no artificial flavoring",
      "offer_type": "Product introduction / awareness — no price promotion"
    },

    "ChannelContext": {
      "platform": "Instagram feed",
      "format": "Single static image, vertical 4:5 preferred (1:1 acceptable)",
      "ui_overlay_consideration": "Top 10% and bottom 20% may be covered by Instagram UI or captions"
    },

    "CampaignConstraints": [
      "No competitor brands or look-alike packaging",
      "No legible invented brand text on the pack (brand identity not yet finalized)",
      "No medical or quantified nutrition claims rendered in the image"
    ],

    "MandatoryRequirements": {
      "required_assets": [
        "The product pack present and recognizable as a protein powder pouch/tub, but secondary to the consumption moment",
        "Natural ingredients visibly present as real, recognizable foods",
        "The prepared product (shake/smoothie) being genuinely enjoyed"
      ],
      "forbidden_elements": [
        "Gym equipment, weights, or athletic-performance context",
        "Before/after or body-transformation framing",
        "Clinical/laboratory supplement aesthetics"
      ]
    }
  }
}
```

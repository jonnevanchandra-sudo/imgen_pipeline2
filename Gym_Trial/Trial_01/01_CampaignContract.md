# Campaign Contract — Anytime Fitness Sai Ying Pun (Stage 1)

Framework: `1. Campaign_Brief.md`
Input: Raw campaign intent — "create a gym advertisement for new member acquisition, targeting HKU-area university students, using Anytime Fitness Sai Ying Pun (the client's own gym, photos supplied) as the background."

**Note on 1.1:** `ProductSpec` (named product model) is not used — there is no physical product to lock; the "product" is the gym facility itself, which is handled as venue/environment preservation at Stage 5 via the supplied reference photos.

```json
{
  "CampaignContract": {
    "BusinessObjective": "Drive new membership sign-ups among HKU-area university students by demonstrating that Anytime Fitness Sai Ying Pun fits naturally into an unpredictable student schedule.",

    "MessageHierarchy": [
      { "rank": 1, "message": "Open 24/7 — train whenever your schedule allows, including late at night or early morning between classes and study sessions." },
      { "rank": 2, "message": "Genuinely close to campus — minutes from HKU/Sai Ying Pun, not a special trip." },
      { "rank": 3, "message": "Modern equipment in a welcoming, judgment-free space — approachable for first-timers, not just experienced lifters." }
    ],

    "AudienceContext": {
      "primary": "HKU-area university students, first-time or infrequent gym-goers, balancing irregular class and study schedules",
      "current_belief": "Going to the gym requires planning a block of free time and walking into an intimidating space — it never fits into 'real life'.",
      "desired_belief": "This gym is right here, open whenever I happen to be free, and I'd feel comfortable just walking in."
    },

    "OfferDefinition": {
      "product": "Anytime Fitness Sai Ying Pun — 24/7-access gym membership",
      "offer_type": "New member acquisition. A specific student offer (e.g. trial period or discounted student rate) is assumed to exist but its terms are not specified — any offer copy/CTA is added as a post-production text overlay, not rendered inside the generated image."
    },

    "ChannelContext": {
      "platform": "Instagram feed / social media (secondary use: printed poster near campus)",
      "format": "Vertical 4:5 preferred (1:1 acceptable)",
      "ui_overlay_consideration": "Top 10% and bottom 20% may be covered by Instagram UI, captions, or an offer/CTA overlay added later"
    },

    "CampaignConstraints": [
      "Must be set within and recognizable as Anytime Fitness Sai Ying Pun, using the supplied venue reference photos",
      "No legible invented text, pricing, or promo copy rendered inside the image",
      "No competitor gym branding",
      "Must read as approachable to first-time gym-goers — avoid an intimidating 'hardcore bodybuilder' aesthetic"
    ],

    "MandatoryRequirements": {
      "required_assets": [
        "The Anytime Fitness Sai Ying Pun interior, recognizable via the supplied reference photos (AF-branded wall/functional rig, the colorful free-weight rack, the broader industrial-chic gym floor)",
        "One HKU-aged student genuinely training in the space"
      ],
      "forbidden_elements": [
        "Competitor gym logos or signage",
        "Fabricated/legible pricing, offer text, or signage copy",
        "Posed, camera-aware 'fitness model' framing",
        "Crowded group/class scenes (acquisition message is personal, one student)"
      ]
    }
  }
}
```

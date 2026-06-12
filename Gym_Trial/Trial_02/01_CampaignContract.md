# Campaign Contract — FIT24 (Stage 1)

Framework: `1. Campaign_Brief.md`
Input: User direction — "create an advertisement using this gym as the background, do however you like." Campaign concept and audience selected by the agent (delegated decision), recorded as assumptions below.

**Declared creative direction:** New member acquisition, built around the single most distinctive feature of the supplied photo — a row of treadmills facing floor-to-ceiling windows with a green, tree-lined outlook. Positioning angle: training somewhere bright and open, rather than a cramped windowless gym. Target audience selected: urban young professionals who train in the morning before work.

```json
{
  "CampaignContract": {
    "BusinessObjective": "Drive new membership sign-ups among urban young professionals by showcasing FIT24's bright, glass-walled training space with a natural green outlook as a differentiator from typical gyms.",

    "MessageHierarchy": [
      { "rank": 1, "message": "Train somewhere bright and open — floor-to-ceiling windows and a green outlook, not a cramped windowless box." },
      { "rank": 2, "message": "Modern, clean, well-equipped space (treadmill row, exposed-ceiling industrial-modern design)." },
      { "rank": 3, "message": "FIT24 — implied round-the-clock accessibility fits a busy professional's schedule." }
    ],

    "AudienceContext": {
      "primary": "Urban young professionals (roughly mid-20s to mid-30s) who want to fit a workout into their day, ideally in the morning before work",
      "current_belief": "Gyms near me are cramped, fluorescent-lit, and feel like a chore.",
      "desired_belief": "FIT24 is a bright, calm, energizing space — training here feels like a good way to start the day, not a grind."
    },

    "OfferDefinition": {
      "product": "FIT24 gym membership",
      "offer_type": "New member acquisition. No specific offer terms specified — any CTA/offer copy is added as a post-production text overlay, not rendered inside the generated image."
    },

    "ChannelContext": {
      "platform": "Instagram feed / social media",
      "format": "Vertical 4:5 preferred (1:1 acceptable)",
      "ui_overlay_consideration": "Top 10% and bottom 20% may be covered by Instagram UI, captions, or an offer/CTA overlay added later"
    },

    "CampaignConstraints": [
      "Must be set within and recognizable as the supplied FIT24 location, using the reference photo (window wall + green outlook, treadmill row, FIT24 logo, exposed ceiling)",
      "No legible invented text, pricing, or promo copy rendered inside the image",
      "No competitor gym branding",
      "Must read as bright, calm, and approachable — not an intense/hardcore-performance aesthetic"
    ],

    "MandatoryRequirements": {
      "required_assets": [
        "The FIT24 interior, recognizable via the supplied reference photo (window wall with green outdoor view, treadmill row, FIT24 wall logo, exposed dark ceiling)",
        "One person training on or near the treadmill row, facing the windows"
      ],
      "forbidden_elements": [
        "Competitor gym logos or signage",
        "Fabricated/legible pricing, offer text, or signage copy",
        "Posed, camera-aware 'fitness model' framing",
        "Crowded group/class scenes"
      ]
    }
  }
}
```

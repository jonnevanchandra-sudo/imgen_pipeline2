# Campaign Contract
**Brand:** CLEVER Protein
**Campaign:** The 3 PM Office Rescue (3點鐘辦公室救星)
**Framework:** Campaign Brief v1.1 (adds ProductSpec)
**Stage:** 1 — Campaign Definition

**Note on 1.1:** ProductSpec is included because the brief names a specific product line — "CLEVER Weight Down" — whose packaging must be recognizable on screen as the "smart choice" side of a comparison. No specific flavor/colorway is mandated by the brief, so `colorway` is left flexible (any of the four confirmed Weight Down flavors — matcha latte, chocolate, yogurt, mixed berries).

---

```json
{
  "CampaignContract": {

    "BusinessObjective": {
      "objective_type": "Trial Acquisition",
      "success_metric": "Click-throughs from Instagram bio link to shop.cleverprotein.com.hk and resulting Weight Down purchases/trials"
    },

    "CampaignTheme": {
      "theme_token": "3 PM Office Rescue (3點鐘辦公室救星)",
      "theme_description": "Reframes the 3pm office snack moment as a decision point: the common high-calorie social snack run (siu mai, bubble tea) versus a CLEVER Weight Down shake as the 'smart'/'clever' alternative that delivers satiety without sabotaging weight goals"
    },

    "MessageHierarchy": {
      "primary_message": "At 3pm, the smart/clever choice is CLEVER Weight Down — high satiety, low calories, instead of the usual office snack run",
      "secondary_messages": [
        "Common HK office 3pm snacks (siu mai, bubble tea / iced lemon tea) carry hidden calories and a sugar crash that work against weight-loss goals",
        "CLEVER Weight Down delivers up to 3 hours of satiety from MCT oil and dietary fiber at a fraction of the calories of a typical snack run",
        "CLEVER Weight Down combines 100% WPI, MCT oil, dietary fiber, and 21 probiotic strains — supports muscle retention, digestion, and a low-sugar/low-fat profile",
        "Choosing CLEVER over weight-loss injections or extreme measures is positioned as the safer, more natural path"
      ],
      "offer_message": "Shop CLEVER Weight Down via the Instagram bio link to make the 3pm switch"
    },

    "AudienceContext": {
      "primary_audience": "Hong Kong 'Smart-Struggling' professionals, approx. 25–35, office-bound, time-poor, health-conscious but prone to social snacking; comfortable in Kongish (Cantonese mixed with English professional terms)",
      "secondary_audience": "HK fitness-niche Instagram followers who engage with 'This vs That' comparison content and weight-management topics",
      "core_motivation": "Maintain weight-loss/lean-body progress despite a demanding office routine, without giving up the daily 3pm snack ritual entirely",
      "primary_barrier": "At 3pm, low willpower and social snacking culture (colleagues ordering siu mai, fish balls, iced lemon tea) leads to 'hidden calorie' choices that quietly undo earlier diet/exercise effort, producing guilt and a sugar-crash energy dip"
    },

    "OfferDefinition": {
      "offer_type": "Direct-to-consumer product purchase (online shop)",
      "offer_value": "CLEVER Weight Down shake as a ~100 kcal, high-satiety (up to 3 hours) replacement for a typical ~450 kcal office snack run",
      "call_to_action": "Click the Instagram bio link to shop CLEVER Weight Down at shop.cleverprotein.com.hk"
    },

    "OfferRole": {
      "priority": "Primary",
      "visibility_requirement": "Required"
    },

    "ChannelContext": {
      "primary_channel": "Instagram",
      "placement_type": "Feed post — organic social media, 'This vs That' comparison format"
    },

    "ChannelBehavior": {
      "attention_window": "Short",
      "interaction_model": "Passive",
      "placement_context": "Instagram feed within the HK fitness niche, where 'This vs That' split visual comparisons currently perform well; Cantonese/Kongish headline, body copy, and hashtags are added in post-production as caption text, not embedded in the generated image"
    },

    "CampaignConstraints": {

      "MessageConstraints": {
        "required_messages": {
          "tokens": ["3 PM Office Rescue", "Hidden Calories", "Smart Choice / Clever Choice", "Satiety"],
          "custom": [
            "The contrast must read as a comparison between a typical high-calorie HK office snack moment and CLEVER Weight Down as the smarter alternative",
            "Tone should feel like a relatable, savvy 'insider tip' for office workers, not a clinical or shame-based weight-loss message",
            "Kongish/Cantonese cultural relevance for HK young professionals"
          ]
        },
        "forbidden_messages": {
          "tokens": ["Weight loss injections", "Extreme dieting", "Medical claims"],
          "custom": [
            "Do not depict or reference weight-loss injections, drugs, or medical/clinical weight-loss procedures",
            "Do not frame the comparison with guilt, shame, or body-shaming toward people who eat the comparison snacks",
            "Do not render quantified nutrition/medical claims (e.g. exact kcal figures, '3 hours satiety') as legible text baked into the generated image — these belong to caption copy, not the image itself"
          ]
        }
      },

      "BrandConstraints": {
        "required_brand_elements": {
          "tokens": ["CLEVER wordmark/logo", "CLEVER Weight Down packaging"],
          "custom": [
            "CLEVER Weight Down product (pouch and/or prepared shake) must be visually recognizable as the brand's signature pink/white minimalist packaging",
            "Brand presence should feel like the 'smart choice' anchor of the scene — composed and clean — even within a high-contrast comparison concept"
          ]
        },
        "forbidden_positioning": {
          "tokens": ["Clinical", "Hardcore gym", "Extreme transformation"],
          "custom": [
            "Do not position CLEVER as a hardcore sports-performance or bodybuilding brand — this campaign speaks to everyday office workers, not athletes",
            "Do not use a sterile/clinical supplement aesthetic — maintain the brand's soft, approachable visual register"
          ]
        }
      },

      "LegalConstraints": {
        "tokens": [],
        "custom": [
          "No competitor brand names, logos, or recognizable competitor packaging"
        ]
      },

      "PlatformConstraints": {
        "tokens": ["Instagram 4:5 vertical format"],
        "custom": [
          "Output format: 1080 x 1350 pixels, 4:5 aspect ratio",
          "Bottom ~15-20% of frame reserved for caption/CTA overlay in post-production — avoid placing critical visual information there",
          "No legible on-image text required or expected from the generator — Cantonese headline, body, hashtags, and CTA are added as Instagram caption text"
        ]
      }
    },

    "MandatoryRequirements": {
      "required_assets": [
        "CLEVER Weight Down product (packaging pouch and/or prepared shake) clearly visible and recognizable",
        "A visual contrast/comparison concept between a typical high-calorie HK office snack moment (e.g. siu mai, fish balls, iced lemon tea / bubble tea) and the CLEVER Weight Down shake as the alternative choice"
      ],
      "required_copy": [
        "Cantonese/Kongish headline, body copy, hashtags, and CTA added in post-production as Instagram caption — not embedded in the generated image"
      ],
      "required_branding": [
        "CLEVER wordmark visible on the Weight Down packaging"
      ],

      "ProductSpec": [
        {
          "product_name": "CLEVER Weight Down (減重蛋白)",
          "product_category": "Weight-management protein shake — stand-up pouch + prepared drink",
          "colorway": "",
          "key_visual_identifiers": [
            "Stand-up pouch packaging (~315g format) in the brand's soft pink/rose-and-white minimalist palette",
            "'CLEVER' wordmark in clean, contemporary all-caps sans-serif on the front label",
            "'減重蛋白' / 'Weight Down' product naming visible on the label",
            "Prepared shake shown as a smooth, uniform beverage in a glass or shaker bottle, color consistent with whichever flavor is depicted (e.g. pale cream for yogurt, soft brown for chocolate, muted green for matcha latte, light pink/red for mixed berries)"
          ],
          "visibility_requirement": "Required",
          "visibility_notes": "The CLEVER Weight Down pouch and/or prepared shake must be clearly legible as the brand's product and occupy a visually prominent role as the 'smart choice' side of the comparison concept. Specific flavor is flexible — Scene Assembly/Art Direction may select one of the four confirmed flavors (matcha latte, chocolate, yogurt, mixed berries) based on visual/compositional fit."
        }
      ]
    },

    "CampaignPriority": {
      "primary_objective": "Drive Instagram engagement and bio-link click-throughs for CLEVER Weight Down among HK office professionals",
      "primary_message": "CLEVER Weight Down is the smart 3pm choice — high satiety, low calories, instead of the typical office snack run",
      "primary_offer": "Shop CLEVER Weight Down via Instagram bio link",
      "primary_constraint": "Must read as a relatable 'smart choice' comparison for everyday office workers — not clinical, not shame-based, and not referencing weight-loss injections or extreme dieting"
    }

  }
}
```

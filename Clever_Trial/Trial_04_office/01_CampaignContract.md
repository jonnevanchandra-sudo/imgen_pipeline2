```json
{
  "CampaignContract": {
    "Metadata": {
      "brand": "CLEVER Protein",
      "framework": "Campaign Brief v1.1",
      "stage": "1 — Campaign Definition",
      "source": "prompt.md + contract.md (BrandContract)"
    },

    "BusinessObjective": {
      "objective_type": "Trial Acquisition",
      "success_metric": "Click-throughs and first-time purchases of CLEVER clear whey protein via social media post (swipe-up / link clicks / attributed orders)"
    },

    "CampaignTheme": {
      "theme_token": "日本製輕盈美學",
      "theme_description": "Position CLEVER Protein as a Made-in-Japan, light and refreshing clear protein drink that replaces guilty afternoon snacking and helps Hong Kong office ladies achieve a slim, confident 'light beauty' aesthetic."
    },

    "MessageHierarchy": {
      "primary_message": "日本製清蛋白，輕盈清爽又高蛋白，取代罪惡下午茶零食，幫你告別3點3肚腩煩惱。",
      "secondary_messages": [
        "果汁口感、無粉感無奶膩，每日一杯好似飲健康特飲。",
        "日本頂級WPI配合21種益生菌及酵素，輕鬆管理體重同時提升肌膚光澤。",
        "高蛋白低卡路里，有效提升飽足感，幫助專注工作、保持精神。"
      ],
      "offer_message": "即上網落單，率先體驗日本製輕盈美學清蛋白下午茶。"
    },

    "AudienceContext": {
      "primary_audience": "香港上班族OL（20–35歲），長時間坐辦公室，注重身形外表，但又愛食零食。",
      "secondary_audience": "關注卡路里及皮膚狀態的年輕女性打工族，平日有飲手搖飲品／果汁習慣。",
      "core_motivation": "以簡單零負擔方法管理體重、保持小腰圍，同時維持皮膚光澤和辦公室形象，享受零食感覺但不想有罪惡感。",
      "primary_barrier": "覺得傳統蛋白粉太heavy又難飲，擔心粉感重、奶膩，亦懷疑蛋白飲品會高卡路里，不適合作下午茶替代品。"
    },

    "OfferDefinition": {
      "offer_type": "Product trial / purchase incentive (standard e-commerce CTA)",
      "offer_value": "體驗日本製清蛋白作為健康下午茶與零食代替品",
      "call_to_action": "立即點擊連結購買／體驗日本製輕盈美學清蛋白"
    },

    "OfferRole": {
      "priority": "Secondary",
      "visibility_requirement": "Required"
    },

    "ChannelContext": {
      "primary_channel": "Social media — Instagram / Facebook (Hong Kong)",
      "placement_type": "Single image post with Cantonese caption"
    },

    "ChannelBehavior": {
      "attention_window": "Short",
      "interaction_model": "Passive",
      "placement_context": "Mobile-first feed; users scroll during work breaks, especially mid-afternoon around 3–4pm."
    },

    "CampaignConstraints": {
      "MessageConstraints": {
        "required_messages": {
          "tokens": ["日本製", "清蛋白 / clear protein", "輕盈 / 輕盈美學", "高蛋白低卡", "適合作為下午茶／零食替代"],
          "custom": [
            "明確提及3點3下午茶時段或下午小肚腩情境。",
            "突出『輕盈清爽、無粉感無奶膩』口感差異點。",
            "傳達『告別罪惡感』的情緒收益。"
          ]
        },
        "forbidden_messages": {
          "tokens": ["醫療療效承諾", "誇大減肥效果（例如『速瘦』、『極速燃脂』等）"],
          "custom": [
            "避免聲稱可治療疾病或具醫療級別效果。",
            "避免保證性用語如『一定減肥』、『保證變瘦』等。"
          ]
        }
      },
      "BrandConstraints": {
        "required_brand_elements": {
          "tokens": ["CLEVER Protein 品牌名稱", "清晰可見的產品包裝", "'Made in Japan' / 日本製 資訊"],
          "custom": [
            "視覺風格要輕盈、乾淨、具『日系』感覺（淺色系、簡約設計）。",
            "如在畫面中出現OL，需自然、自信、健康，不誇張健身風。"
          ]
        },
        "forbidden_positioning": {
          "tokens": ["硬核健美／健身補劑形象"],
          "custom": [
            "避免太男性化或heavy gym supplement的視覺語言（黑色罐裝、肌肉pose）。",
            "避免與垃圾食物一起出現。"
          ]
        }
      },
      "LegalConstraints": {
        "tokens": ["不得作出未經證實的健康聲稱", "避免使用醫療用語"],
        "custom": ["體重管理及肌膚光澤需以『幫助、支持、改善狀態』等溫和字眼表達。"]
      },
      "PlatformConstraints": {
        "tokens": ["遵守Meta/Instagram對體重管理廣告政策", "避免body shaming內容"],
        "custom": ["不直接貶低特定身形；如展示肚腩情境需保持輕鬆幽默、不羞辱。"]
      }
    },

    "MandatoryRequirements": {
      "required_assets": [
        "清晰展示CLEVER Protein日本製清蛋白產品包裝的主視覺（單一英雄口味）。",
        "至少一個視覺元素點出日本製／日系感。",
        "情境元素暗示辦公室下午茶時間（桌面、3:30時鐘等）。"
      ],
      "required_copy": [
        "主視覺或On-image text需包含：『日本製清蛋白』及『告別罪惡感』或同義字。",
        "Caption以廣東話溝通，語氣親切貼地（OL語氣）。",
        "包含推動行動的CTA。"
      ],
      "required_branding": [
        "CLEVER Protein品牌logo或明顯品牌名稱。",
        "Made in Japan / 日本製標示。",
        "與CLEVER品牌一致的色調（sky-blue + white系統）。"
      ],
      "ProductSpec": [],
      "ReferenceImages": {
        "note": "image1.png and image4.png are provided as brand asset references for the lemon pack, transparent shaker, and CLEVER logo. image2.png and image3.png are visual style inspiration only.",
        "hero_flavor": "Lemon (檸檬)",
        "treatment": "image1 + image4 = brand asset references (pack, shaker, logo); image2 + image3 = inspiration only"
      }
    },

    "CampaignPriority": {
      "primary_objective": "推動香港OL在社交媒體上認知並嘗試CLEVER Protein日本製清蛋白作為健康下午茶／零食替代品。",
      "primary_message": "日本製、果汁口感的清蛋白，輕盈清爽高蛋白，幫你3點3飽足無罪惡感。",
      "primary_constraint": "必須強調清爽口感與『日本製輕盈美學』定位，同時避免誇大健康和減肥功效。"
    }
  }
}
```

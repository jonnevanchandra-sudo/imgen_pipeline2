```json
{
  "CampaignContract": {
    "Metadata": {
      "brand": "CLEVER Protein",
      "framework": "Campaign Brief v1.1",
      "stage": "1 — Campaign Definition",
      "source": "prompt.md + contract.md (BrandContract)",
      "variant": "Trial_04_gym — gym/fitness space, on-image ad typography"
    },

    "BusinessObjective": {
      "objective_type": "Trial Acquisition",
      "success_metric": "Click-throughs and first-time purchases of CLEVER clear whey protein via social media post (swipe-up / link clicks / attributed orders)"
    },

    "CampaignTheme": {
      "theme_token": "日本製輕盈美學",
      "theme_description": "Position CLEVER Protein as a Made-in-Japan, light and refreshing clear protein drink that replaces the heavy post-workout shake and helps Hong Kong active ladies achieve a slim, confident 'light beauty' aesthetic. Gym/post-workout context — the protagonist is an HK OL who just finished yoga/fitness and chooses CLEVER as her light, guilt-free post-workout drink rather than a heavy protein shake."
    },

    "MessageHierarchy": {
      "primary_message": "日本製清蛋白，輕盈清爽又高蛋白，取代厚重運動後蛋白奶昔，幫你告別運動後重裝感。",
      "secondary_messages": [
        "果汁口感、無粉感無奶膩，運動後一杯，清爽補充不沉重。",
        "日本頂級WPI配合21種益生菌及酵素，輕鬆補充蛋白同時提升肌膚光澤。",
        "高蛋白低卡路里，有效補充運動消耗，保持輕盈體態同時修復肌肉。"
      ],
      "offer_message": "即上網落單，率先體驗日本製輕盈美學清蛋白運動後補充。"
    },

    "AudienceContext": {
      "primary_audience": "香港活躍OL（20–35歲），定期做瑜伽、普拉提或功能性健身，注重身形外表，但想以輕盈方式補充蛋白質。",
      "secondary_audience": "關注卡路里及皮膚狀態的年輕女性健身族，平日有健身習慣但抗拒傳統厚重蛋白粉。",
      "core_motivation": "以簡單零負擔方法補充運動後蛋白質、保持小腰圍，同時維持皮膚光澤和輕盈體態，享受清爽補充感覺但不想攝取過多熱量。",
      "primary_barrier": "覺得傳統蛋白粉太heavy又難飲，擔心粉感重、奶膩，亦懷疑運動後蛋白飲品會高卡路里，不適合追求輕盈的OL。"
    },

    "OfferDefinition": {
      "offer_type": "Product trial / purchase incentive (standard e-commerce CTA)",
      "offer_value": "體驗日本製清蛋白作為健身後輕盈蛋白補充品",
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
      "placement_context": "Mobile-first feed; users scroll during post-workout rest or commute, especially mid-afternoon."
    },

    "CampaignConstraints": {
      "MessageConstraints": {
        "required_messages": {
          "tokens": ["日本製", "清蛋白 / clear protein", "輕盈 / 輕盈美學", "高蛋白低卡", "適合作為運動後輕盈補充"],
          "custom": [
            "明確點出運動後不需要厚重蛋白奶昔的情境。",
            "突出『輕盈清爽、無粉感無奶膩』口感差異點。",
            "傳達『告別運動後重裝感』的情緒收益。"
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
            "如在畫面中出現OL，需自然、自信、健康，運動後輕盈感，不誇張健身風。"
          ]
        },
        "forbidden_positioning": {
          "tokens": ["硬核健美／健身補劑形象"],
          "custom": [
            "避免太男性化或heavy gym supplement的視覺語言（黑色罐裝、肌肉pose）。",
            "避免與大型健身器械或重訓環境強烈連結。"
          ]
        }
      },
      "LegalConstraints": {
        "tokens": ["不得作出未經證實的健康聲稱", "避免使用醫療用語"],
        "custom": ["體重管理及肌膚光澤需以『幫助、支持、改善狀態』等溫和字眼表達。"]
      },
      "PlatformConstraints": {
        "tokens": ["遵守Meta/Instagram對體重管理廣告政策", "避免body shaming內容"],
        "custom": ["不直接貶低特定身形；展示健身情境需保持輕鬆健康、不施壓。"]
      }
    },

    "MandatoryRequirements": {
      "required_assets": [
        "清晰展示CLEVER Protein日本製清蛋白產品包裝的主視覺（單一英雄口味）。",
        "至少一個視覺元素點出日本製／日系感。",
        "情境元素暗示健身後輕盈小休時刻（明亮健身室環境、瑜伽墊、運動後輕盈）。"
      ],
      "required_copy": [
        "主視覺On-image text需包含：標題『告別運動後重裝感！』及副標題『日本製·清蛋白』。",
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
      "primary_objective": "推動香港活躍OL在社交媒體上認知並嘗試CLEVER Protein日本製清蛋白作為健身後輕盈蛋白補充品。",
      "primary_message": "日本製、果汁口感的清蛋白，輕盈清爽高蛋白，幫你運動後飽足無重裝感。",
      "primary_constraint": "必須強調清爽口感與『日本製輕盈美學』定位，同時避免誇大健康和減肥功效。"
    }
  }
}
```

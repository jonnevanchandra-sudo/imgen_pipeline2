```json
{
  "CampaignContract": {
    "Metadata": {
      "brand": "CLEVER Protein",
      "framework": "Campaign Brief v1.1",
      "stage": "1 — Campaign Definition",
      "source": "prompt.md + contract.md (BrandContract)",
      "variant": "Trial_06_gym_male — bright window-lit studio, male protagonist, regenerated from scratch (male-targeted reframing, not a female-OL contract with a face swap)"
    },

    "BusinessObjective": {
      "objective_type": "Trial Acquisition",
      "success_metric": "Click-throughs and first-time purchases of CLEVER clear whey protein via social media post (swipe-up / link clicks / attributed orders)"
    },

    "CampaignTheme": {
      "theme_token": "日本製清蛋白 · 輕盈恢復力",
      "theme_description": "Position CLEVER Protein as a Made-in-Japan, light and refreshing clear protein drink that replaces the heavy, chalky post-workout shake for active Hong Kong men who want a lean, capable physique without buying into 'gym bro' supplement culture. Gym/post-workout context — the protagonist is an active HK man who just finished a fitness session and reaches for CLEVER as his light, no-burden recovery drink instead of a thick protein shake."
    },

    "MessageHierarchy": {
      "primary_message": "日本製清蛋白，輕盈清爽又高蛋白，取代厚重運動後蛋白奶昔，幫你告別運動後重裝感。",
      "secondary_messages": [
        "果汁口感、無粉感無奶膩，運動後一杯，清爽補充不沉重。",
        "日本頂級WPI配合21種益生菌及酵素，輕鬆補充蛋白同時維持精實體態。",
        "高蛋白低卡路里，有效補充運動消耗，幫助肌肉恢復同保持輕盈表現力。"
      ],
      "offer_message": "即上網落單，率先體驗日本製輕盈系統清蛋白運動後補充。"
    },

    "AudienceContext": {
      "primary_audience": "香港活躍男士（25–35歲），恆常做gym、功能性訓練或瑜伽，注重體態同表現，但想以輕盈方式補充蛋白質，唔想被傳統蛋白奶昔嘅厚重感拖累。",
      "secondary_audience": "注重健康同體態管理嘅都市男性，已有健身習慣，抗拒傳統「健身房肌肉佬」式重口味蛋白粉形象。",
      "core_motivation": "想以簡單、無負擔嘅方法補充運動後蛋白質，保持精實體態同表現力，享受清爽補充感覺，但唔想攝取過多熱量或被「健身房補劑」嘅形象綁定。",
      "primary_barrier": "覺得傳統蛋白粉太heavy又難飲，擔心粉感重、奶膩，亦懷疑清爽嘅蛋白飲品係唔係真係夠「頂得住」運動後嘅蛋白需求。"
    },

    "OfferDefinition": {
      "offer_type": "Product trial / purchase incentive (standard e-commerce CTA)",
      "offer_value": "體驗日本製清蛋白作為健身後輕盈蛋白補充品",
      "call_to_action": "立即點擊連結購買／體驗日本製輕盈系統清蛋白"
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
      "placement_context": "Mobile-first feed; users scroll during post-workout rest or commute, especially evening gym-session hours."
    },

    "CampaignConstraints": {
      "MessageConstraints": {
        "required_messages": {
          "tokens": ["日本製", "清蛋白 / clear protein", "輕盈 / 輕盈恢復", "高蛋白低卡", "適合作為運動後輕盈補充"],
          "custom": [
            "明確點出運動後不需要厚重蛋白奶昔的情境。",
            "突出『輕盈清爽、無粉感無奶膩』口感差異點。",
            "傳達『告別運動後重裝感』的情緒收益。"
          ]
        },
        "forbidden_messages": {
          "tokens": ["醫療療效承諾", "誇大增肌效果（例如『極速增肌』、『爆肌』等）"],
          "custom": [
            "避免聲稱可治療疾病或具醫療級別效果。",
            "避免保證性用語如『一定增肌』、『保證爆肌』等。"
          ]
        }
      },
      "BrandConstraints": {
        "required_brand_elements": {
          "tokens": ["CLEVER Protein 品牌名稱", "清晰可見的產品包裝", "'Made in Japan' / 日本製 資訊"],
          "custom": [
            "視覺風格要輕盈、乾淨、具『日系』感覺（淺色系、簡約設計）。",
            "畫面中嘅男士需自然、自信、健康，運動後輕盈感，唔誇張健身風。"
          ]
        },
        "forbidden_positioning": {
          "tokens": ["硬核健美／健身補劑形象", "重訓肌肉猛男形象"],
          "custom": [
            "避免太「健身房肌肉佬」或heavy gym supplement的視覺語言（黑色罐裝、肌肉pose、爆肌特寫）。",
            "避免與大型健身器械或重訓環境強烈連結。",
            "男模應呈現精實、健康嘅運動體態，唔係健美式誇張肌肉量。"
          ]
        }
      },
      "LegalConstraints": {
        "tokens": ["不得作出未經證實的健康聲稱", "避免使用醫療用語"],
        "custom": ["體能恢復及體態管理需以『幫助、支持、改善狀態』等溫和字眼表達。"]
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
        "情境元素暗示健身後輕盈小休時刻（明亮健身室／瑜伽studio環境、運動後輕盈）。"
      ],
      "required_copy": [
        "主視覺On-image text需包含：標題『日日飲，激發體能』及副標題『日本製·清蛋白』。",
        "Caption以廣東話溝通，語氣親切貼地。",
        "包含推動行動的CTA。"
      ],
      "required_branding": [
        "CLEVER Protein品牌logo或明顯品牌名稱。",
        "Made in Japan / 日本製標示。",
        "與CLEVER品牌一致的色調（sky-blue + white系統）。"
      ],
      "ProductSpec": [],
      "ReferenceImages": {
        "note": "image1.png and image4.png are brand asset references for the lemon pack, transparent shaker, and CLEVER logo. image7.png and image (1).png show the SAME male model from two different angles/moments and are the identity reference for the human subject in this variant — only his face, hair, and build carry through; the gym activity, background, and any baked-in text/logo/UI overlay visible in image (1).png are explicitly excluded. image2.png and image3.png remain style inspiration only and are unused in this variant.",
        "hero_flavor": "Lemon (檸檬)",
        "treatment": "image1 + image4 = brand asset references (pack, shaker, logo); image7 + image (1) = male model identity reference (same person, two angles); image2 + image3 = inspiration only, unused"
      }
    },

    "CampaignPriority": {
      "primary_objective": "推動香港活躍男士在社交媒體上認知並嘗試CLEVER Protein日本製清蛋白作為健身後輕盈蛋白補充品。",
      "primary_message": "日本製、果汁口感的清蛋白，輕盈清爽高蛋白，幫你運動後飽足無重裝感。",
      "primary_constraint": "必須強調清爽口感與『輕盈恢復』定位，同時避免淪為硬核健身補劑或誇大增肌效果的視覺語言。"
    }
  }
}
```

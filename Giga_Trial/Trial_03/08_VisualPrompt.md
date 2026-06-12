# Visual Prompt
**Brand:** GigaSports
**Campaign:** Gigasports Pickle Club Community
**Framework:** Prompt Compiler v3.0
**Stage:** 8 — Prompt Translation

---

```json
{
  "VisualPrompt": {
    "CRITICAL": {
      "subjects": "2–3 young Asian professionals, late twenties to early thirties. Mid-laugh or mid-conversation — expressions natural, unposed. Physical proximity reads as social comfort, not formal distance. Pickleball paddles held loosely at their sides.",
      "emotion": "Genuine social warmth between people who actually like each other. A moment between friends, not subjects posing."
    },
    "HIGH": {
      "action": "Between-rally social pause. They are talking, not playing. Eye contact between subjects — not at camera. The conversation is the subject.",
      "brand": "GigaSports logo on a banner or wall in the venue background. Use reference_asset_01 exactly — reproduce the bold italic wordmark, globe icon replacing the O in Sports, and BE PROFESSIONAL tagline as provided. White on surface. Legible through bokeh, not dominant.",
      "setting": "Indoor pickleball court. Net and court line markings in midground. Warm community sports venue — active and social, not institutional."
    },
    "MEDIUM": {
      "community_signal": "The group reads as an established social circle — ease and familiarity between them, not strangers at a first meeting."
    },
    "LOW": {
      "style": "Candid lifestyle editorial. Photographed, not rendered. Athletic casual wear — modern, varied, nothing matching or uniform."
    },
    "FORMAT": {
      "aspect_ratio": "4:5 vertical (1080×1350px), Instagram feed",
      "safe_zones": "No faces, paddles, brand elements, or any critical visual information in the top 10% or bottom 20% of the frame. Bottom zone reserved for Cantonese copy and membership CTA overlay."
    },
    "LIGHTING": {
      "quality": "Soft overhead ambient fill. No hard shadows.",
      "temperature": "Warm indoor venue — neutral-to-warm on faces, not orange-tinted on skin.",
      "source": "Overhead venue lighting with mild wrap. Subjects slightly brighter than background.",
      "hierarchy": "Subjects read brighter and crisper than background. Background recedes into warmth.",
      "prohibited": "No studio lighting. No dramatic rim light. No cinematic low-key contrast. No flash look."
    },
    "CAMERA": {
      "shot_type": "Medium shot — subjects from approximately waist up",
      "angle": "Eye-level. Camera height equal to subjects. Not observational, not elevated.",
      "distance": "Near. Subjects fill the foreground, faces readable at scroll speed.",
      "depth_of_field": "Shallow. Subjects sharp. Court moderate at midground. Background venue and brand in warm natural bokeh.",
      "optical_notes": "Bokeh calibrated so GigaSports logo on background banner stays identifiable despite soft focus."
    },
    "AUTHENTICITY": {
      "human_authenticity": "Open-mouth laugh, caught mid-word, relaxed smile — not posed. Asymmetric posture between subjects. Natural variation in weight distribution.",
      "environmental_authenticity": "Real court surface with use marks. Natural ceiling. Ambient lighting inconsistency typical of indoor sports venues.",
      "material_authenticity": "Fabric wrinkle and drape on athletic wear. Subtle sheen variation on paddle surface. No hyper-polished rendering.",
      "imperfection_rule": "Credibility over perfection. A slightly asymmetric frame or partially obscured face increases believability."
    },
    "SCENE": {
      "depth_structure": "Subjects in foreground — minimum two-thirds of frame height. Court and net in midground. Venue walls and GigaSports banner in background.",
      "spatial_relationships": "Subjects face each other or angled toward each other — social orientation, not camera orientation. Paddles at sides or hip height.",
      "anchor_relationships": "Subjects floor-anchored on court. Net horizontally visible in midground. GigaSports banner wall-mounted in background.",
      "scale": "Subject group dominates frame. Background elements subordinate — atmospheric, not architectural."
    },
    "BRAND_ASSETS": [
      {
        "asset_ref": "reference_asset_01",
        "instruction": "reference_asset_01 is the GigaSports logo. Reproduce it exactly as shown — bold italic compressed wordmark reading 'GigaSports' with a stylized globe icon replacing the letter O in Sports, and 'BE PROFESSIONAL' in small caps centered below. All elements white. Place on a banner or wall surface in the scene background. Do not redraw from memory or substitute any element."
      }
    ],
    "NEGATIVE": [
      "No solo subject.",
      "No active play — no mid-swing, no ball in frame, no competitive intensity.",
      "No posed formal group lineup facing camera.",
      "No studio lighting or dramatic rim light.",
      "No outdoor setting.",
      "No high-performance athletic body language.",
      "No product-forward composition with equipment as hero.",
      "No AI-smoothed skin or idealized facial rendering.",
      "No GigaSports logo redrawn from training data — use reference_asset_01 only."
    ]
  },
  "ReferenceAssetManifest": [
    {
      "asset_id": "asset_01",
      "filename": "gigasports_logo.jpg",
      "type": "Brand-Bearing",
      "prompt_reference_id": "reference_asset_01",
      "attach_to_api_call": true,
      "strictness": "Exact"
    }
  ]
}
```

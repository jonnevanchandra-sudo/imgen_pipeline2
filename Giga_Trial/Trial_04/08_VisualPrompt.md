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
      "subjects": "2–3 young East Asian professionals, late twenties to early thirties. One newcomer and one or two established members. The newcomer's face is the emotional anchor — expression caught mid-transition: slight surprise dissolving into warm relief, the specific look of 'I thought I might not fit in, and I do.' Not a generic smile. The emotional micro-moment must be readable at scroll speed.",
      "emotion": "The exact second someone stops being outside and starts being inside. Welcome is being given, not exchanged. The relational direction flows from the established member(s) toward the newcomer — open body language, genuine warmth, nothing performed for the camera."
    },
    "HIGH": {
      "action": "Active welcome gesture from at least one established member directed at the newcomer — high five mid-contact, arm around shoulder, or open-body orientation with direct warm eye contact. Paddles held loosely in non-greeting hands or at sides. The sport is the context; the welcome is the action.",
      "brand": "GigaSports logo on a banner or wall surface in the venue background. Use reference_asset_01 exactly — reproduce the compressed bold italic wordmark 'GigaSports', the globe icon replacing the O in Sports showing continental outlines, and the BE PROFESSIONAL tagline in small all-caps below. All elements white on the venue surface. Legible through bokeh, not dominant.",
      "setting": "Indoor pickleball court. Court line markings on floor. Net visible in midground. Warm, active indoor sports venue — communal and lived-in, not institutional or polished."
    },
    "MEDIUM": {
      "sport_context": "Pickleball paddles held by all subjects — identifiable paddle shape, relaxed grip, not raised in playing position. Sport is present as identity signal, not as performance."
    },
    "LOW": {
      "style": "Candid lifestyle editorial. Photographed, not rendered. Athletic casual wear — modern, varied, nothing matching or coordinated."
    },
    "FORMAT": {
      "aspect_ratio": "4:5 vertical (1080×1350px), Instagram feed",
      "safe_zones": "No faces, paddles, welcome gesture, brand elements, or any critical visual information in the top 10% or bottom 20% of the frame. Bottom zone reserved for Cantonese copy and membership CTA overlay applied in post-production."
    },
    "LIGHTING": {
      "quality": "Soft overhead ambient fill — no hard shadows, no theatrical contrast.",
      "temperature": "Warm indoor venue. Neutral-to-warm on skin. Not orange-tinted. Background warmer than foreground.",
      "source": "Overhead venue lighting with mild wrap. Subjects slightly brighter than background — hierarchy through luminance, not spotlight.",
      "hierarchy": "Foreground subjects read brighter and crisper. Background recedes into warm bokeh.",
      "prohibited": "No studio lighting. No dramatic rim light. No cinematic low-key contrast. No flash look. No cold temperature."
    },
    "CAMERA": {
      "shot_type": "Medium shot — subjects from approximately waist up. Both faces fully readable.",
      "angle": "Eye-level. Camera at subject height — viewer is inside the social space, not observing from above or below.",
      "distance": "Near. Subjects fill the foreground; facial expressions and welcome gesture legible at scroll speed.",
      "depth_of_field": "Shallow. Both newcomer and established member faces in sharp simultaneous focus — the welcome requires both expressions. Court in moderate focus at midground. Background venue and GigaSports logo in warm natural bokeh.",
      "optical_notes": "Bokeh calibrated so GigaSports logo on background surface stays identifiable — soft, not obliterated."
    },
    "AUTHENTICITY": {
      "human_authenticity": "Welcome gesture mid-motion, not held for camera. Newcomer expression mid-transition — not a posed smile, the specific warmth of surprise giving way to belonging. Natural asymmetry in posture between subjects. Eye contact between subjects, not at lens.",
      "environmental_authenticity": "Real court surface — line wear, natural imperfections. Natural ceiling. Ambient lighting inconsistency typical of indoor sports venues. No set-like uniformity.",
      "material_authenticity": "Fabric wrinkle and drape on athletic casual wear. Natural skin texture — pores, subtle tone variation, nothing smoothed. Slight sheen variation on paddle surfaces.",
      "imperfection_rule": "Credibility over perfection. A slightly asymmetric frame or partially occluded paddle increases believability. This must look photographed, not rendered."
    },
    "SCENE": {
      "depth_structure": "Newcomer (entity_01) and established member(s) (entity_02) in foreground — minimum two-thirds of frame height, faces fully in frame. Paddles at their sides. Court surface and net in midground. GigaSports logo and venue walls in background, receding into bokeh.",
      "spatial_relationships": "Entity_02 faces entity_01 and extends welcome gesture toward entity_01. Entity_01 faces entity_02, receiving the gesture. Neither subject faces the camera — the relational dynamic between them is the visual subject. Paddles held at sides or in non-greeting hands.",
      "anchor_relationships": "Both subjects floor-anchored on court surface. Net horizontally visible in midground. GigaSports logo wall-mounted or banner-hung in background.",
      "scale": "Subject group dominates foreground. Both faces must be large enough to read expression clearly. Background elements subordinate — atmospheric depth, not architectural detail."
    },
    "BRAND_ASSETS": [
      {
        "asset_ref": "reference_asset_01",
        "instruction": "reference_asset_01 is the GigaSports logo. Reproduce it exactly as shown — compressed bold italic wordmark reading 'GigaSports' as a single word, with a stylized globe icon replacing the letter O in Sports (circular, showing continental silhouette outlines, same cap-height as surrounding letters), and 'BE PROFESSIONAL' in small wide-tracked all-caps centered directly below the wordmark. All elements white. Place on a banner or wall surface in the scene background. Do not redraw from training data or substitute any element."
      }
    ],
    "NEGATIVE": [
      "No solo subject — the welcome requires at least two people.",
      "No group of established friends — the newcomer dynamic must be visually distinct from peer-to-peer social interaction.",
      "No active play — no mid-swing, no ball in frame, no competitive athletic body language.",
      "No posed group lineup facing camera.",
      "No studio lighting or dramatic rim light.",
      "No outdoor setting.",
      "No high-performance athletic intensity.",
      "No product-forward or equipment-hero composition.",
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

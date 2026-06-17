```json
{
  "VisualPrompt": {
    "CRITICAL": {
      "subjects": "One Hong Kong office woman, mid-to-late twenties, naturally healthy and attractive East Asian, in light polished-casual office wear — business casual blouse with clean skirt or slacks, not gym clothes. Standing at a clean pantry counter in a modern HK office kitchenette, actively shaking or holding a transparent shaker of clear, pale-yellow lemon protein drink with a lemon slice inside. The drink is the hero: visibly clear and translucent, light passing through it, never opaque or milky.",
      "emotion": "Calm, purposeful, quietly proud — she is making a deliberate, guilt-free choice at 3pm. Not frazzled or rushed. This is her intentional ritual, performed with quiet confidence."
    },
    "HIGH": {
      "brand": "A CLEVER 'CLEAR PROTEIN' lemon-flavor pouch stands on the clean counter facing the camera, clearly legible. CLEVER logo visible on the shaker. A 'Made in Japan / 日本製' cue is legible in frame.",
      "setting": "A clean, bright, modern HK office pantry/kitchenette. Counter surface is near-empty — only the pouch and shaker. Background: a soft-focused water dispenser or hot/cold water machine (blurred, recognizable silhouette) and clean light-colored walls (white or off-white). Background reads as office pantry through minimal, soft-focused cues — not through clutter.",
      "typography": "Bold modern sans-serif headline '告別3點3罪惡感！' in the upper background zone, above and behind the OL. Subtitle '日本製 · 清蛋白' directly below in smaller text. High-contrast text — white or dark-blue against the clean pantry background. Fully legible at mobile screen size."
    },
    "FORMAT": "Square 1:1 for an Instagram/Facebook feed post. No faces, brand elements, or critical visual information in the top 12% or bottom 12% of the frame.",
    "LIGHTING": "Soft, bright high-key light — pantry window daylight or overhead soft LED. Clear shaker and pouch receive the cleanest, most direct light; a gentle specular glint on the glass makes the drink look crisp and refreshing. OL lit softer, skin warm-neutral. Background evenly exposed — no shadow gradients behind the OL that would undermine typography contrast. No bright hotspot directly behind the subject's head.",
    "CAMERA": "Eye-level at counter height, near medium shot. 85mm at f/4: foreground pouch and shaker are crisply sharp; OL is sharp to gently soft by depth; pantry background (water dispenser, walls) softens into a clean, gently blurred backdrop — recognizable as pantry but not detailed. Typography in upper background zone slightly softened but fully legible. Progressive depth-dependent bokeh — no flat uniform blur.",
    "AUTHENTICITY": {
      "human_authenticity": "Real skin — visible pores, fine lines, subtle tone variation, natural asymmetry. Purposeful, naturally composed expression. Hands visible holding or shaking the bottle — natural hand texture, not artificial perfection.",
      "environmental_authenticity": "Counter is intentionally near-empty — curated photoshoot-set quality within a real pantry context. Background pantry elements (water dispenser, walls) are present but soft-focused and minimal. Only natural material imperfections acceptable: subtle counter surface texture, soft reflections.",
      "material_authenticity": "Believable liquid optics — light passing through the clear pale-yellow drink, light condensation on the shaker, matte pouch surface vs. glossy shaker body.",
      "imperfection_rule": "Credibility over perfection for skin and material behavior. Counter and backdrop must stay clean and pristine — any clutter or shadow in those areas works against the intended concept."
    },
    "SCENE": "Pouch and shaker in the foreground at counter level, closest to camera, crisply sharp. OL stands behind and above the counter in the midground, actively engaged with the shaker. Background softens to a clean pantry backdrop — water dispenser silhouette low in the background, clean wall filling the upper background zone where the typography sits. No other objects on the counter surface.",
    "BRAND_ASSETS": [
      {
        "asset_ref": "reference_asset_01",
        "instruction": "reference_asset_01 is image1.png — it contains the CLEVER lemon 'CLEAR PROTEIN' pouch and the transparent shaker with clear pale-yellow lemon drink. Reproduce the pouch exactly: white body, large dark-blue 'CLEAR PROTEIN' typography, bright yellow lemon-flavor band at top, CLEVER logo, and functional badges — same shapes, colors, and proportions, do not redraw from memory. Reproduce the shaker and its CLEVER logo exactly; keep the drink clear and translucent, never opaque. Use only the product and bottle from this image — discard the male model and gym background entirely."
      },
      {
        "asset_ref": "reference_asset_02",
        "instruction": "reference_asset_02 is image4.png — it contains the CLEVER wordmark and a clean, minimal sky-blue layout. Reproduce the CLEVER logo exactly: same letterforms, same color, same proportions, do not redraw from memory. Use image4's clean minimal aesthetic as the target visual register for the overall feel and brand presence. Exclude the timing-clock graphic, any pricing, and the specific model from that image."
      }
    ],
    "NEGATIVE": "No thick, opaque, or milky shake. No gym, dumbbells, muscular posing, or athletic staging. No black supplement tubs. No before-after or weighing scale. No snack wrappers, chips, candy, or other food on the counter. No microwave, messy sink, or dish rack in frame. No visible snack shelf or branded snack packaging in the background. No other people in the pantry. No office desk, chair, or workstation context. No laptop, papers, or work materials. No cluttered counter of any kind. No bright spots or hotspots behind the subject's head. No outdoor running scene. No smoothed AI skin. No invented marketing slogans or text paragraphs beyond the specified headline and subtitle."
  },
  "ReferenceAssetManifest": [
    {
      "asset_id": "asset_01",
      "filename": "image1.png",
      "type": "Brand-Bearing",
      "prompt_reference_id": "reference_asset_01",
      "attach_to_api_call": true,
      "strictness": "Exact"
    },
    {
      "asset_id": "asset_04",
      "filename": "image4.png",
      "type": "Brand-Bearing",
      "prompt_reference_id": "reference_asset_02",
      "attach_to_api_call": true,
      "strictness": "Exact"
    }
  ]
}
```

```yaml
# Prompt Compiler v2.3 (8.1.1) — flat prose VisualPrompt with inline brand asset reproduction
# Source: SynthesisContract Trial_06_gym_male + ReferenceAssetManifest (Scene Assembly 5.2.5)
# Target: flat-prose generators (Midjourney / DALL-E / Flux / GPT Image 2.0)

VisualPrompt: "A clean, bright lifestyle advertising photograph of an East Asian man in his mid-twenties, lean and athletic in build with visible muscle tone — toned, not bodybuilder-bulky — taking a post-workout cool-down moment in a bright modern fitness studio. He wears a light athletic t-shirt, white or light blue, not a dark tank top. He stands or rests calmly, lightly satisfied and quietly confident, holding or just having finished drinking from a transparent shaker of clear, pale-yellow lemon protein drink with a lemon slice inside; the drink is the undisputed hero of the image and must read as genuinely clear and translucent with light passing through it — never opaque, never milky. His expression is calm and unguarded, a small earned moment of relief with no strain, no sweat, and no muscle-flexing or posed gym-bro display.

His face, hair, and build come from two reference images of the same person: this is reference_asset_03 — reproduce his short-to-medium dark hair swept back/upward, his defined jawline, and his lean athletic build exactly; that source image shows him mid-plank in an exercise pose with a stability ball and a houseplant in the background — discard the pose, the ball, the plant, and that background entirely, carrying through only his face, hair, and build. This is reinforced by reference_asset_04, a second image of the same man standing by a window from a different angle — use it only to confirm the same facial identity and hairstyle; that source image has a pre-existing white 'CLEVER' wordmark, on-image ad text, and a small notification/chat-bubble graphic baked into the frame, plus a dark tank top and a standing pose — discard all of that entirely; do not reproduce its logo styling, text layout, UI graphic, pose, wardrobe, or background.

On the studio floor just beside him, nearer the camera than his face, stands a CLEVER 'CLEAR PROTEIN' lemon-flavor pouch, facing the camera and clearly legible — white body, large dark-blue 'CLEAR PROTEIN' typography across the middle, bright yellow lemon-flavor accent band at the top, CLEVER logo, and functional benefit badges. The pouch and shaker both come from a reference image: this is reference_asset_01 — reproduce the pouch exactly: same white body, same blue 'CLEAR PROTEIN' typography, same yellow lemon band, same logo and badges, same shapes, colors, and proportions; reproduce the shaker and its CLEVER logo exactly, keep the drink clear and translucent; use only the product and bottle from this reference image and discard the model and background entirely; do not redraw the packaging or logo from memory.

The CLEVER wordmark also appears in the frame alongside a legible 'Made in Japan / 日本製' cue: this is reference_asset_02 — reproduce the CLEVER logo exactly: same letterforms, same color, same proportions, do not redraw from memory; use that reference image's clean minimal sky-blue aesthetic as the target visual register for the background and overall feel; exclude the timing-clock graphic, any pricing, and the specific model from that reference image.

The studio floor is a clean, near-empty surface — light wood or pale rubber flooring — with the CLEVER pouch, the shaker, and one rolled yoga or exercise mat as the only objects visible; nothing else on the floor, no other gym clutter. The background behind him is dominated by large floor-to-ceiling studio windows flooding the space with soft natural sky-blue daylight — no heavy gym equipment, no mirrored walls, no dark surfaces. In the upper portion of this bright window-light background zone, render bold modern sans-serif white typography as a designed ad headline: '日日飲，激發體能' large and prominent, with the smaller subtitle '日本製 · 清蛋白' beneath it — positioned clear of his face and the product cluster, fully legible at mobile screen size.

Light the scene with soft, bright, high-key natural daylight from the studio windows: the clear drink and pouch receive the cleanest, most direct light with a gentle specular glint on the glass and liquid so the drink looks crisp and refreshing; he is lit a touch softer, skin warm-neutral and never orange, with a light healthy post-workout flush; the background window zone is bright and evenly lit so the white typography stays clearly legible against it, never blown out to the point of washing out the text. Shoot at eye level, a near medium shot, with an 85mm lens at f/4: the foreground pack and shaker are crisply sharp, he is sharp to gently soft by depth, and the studio windows behind soften further into a smooth, glowing sky-blue plane with progressive bokeh falloff and no flat uniform blur — the typography in that zone softens slightly but remains fully readable. Render his skin with visible pores, fine lines, subtle tone variation, and natural asymmetry — a candid, relaxed expression, no beauty filter, no airbrushing, no plastic or AI-perfect rendering. Render believable glass and liquid optics with light condensation on the shaker and a matte pouch surface contrasting against the glossy bottle body, and lightweight athletic fabric texture on his t-shirt. The studio floor and background must remain genuinely clean and pristine — no shadows or imperfections in those areas beyond the natural softening of depth of field. Avoid any thick, opaque, or milky shake; any heavy dumbbells, barbells, or weight machines; any mirrored walls or dark gym surfaces; any outdoor sky or rooftop setting — this is an indoor studio; any sweating, straining, or muscle-flexing/bodybuilder posing; any other people; any black supplement tubs; any before-after comparisons or weighing scales; any cluttered floor or gym bags; any invented typography beyond the specified headline and subtitle; any smoothed AI skin; any locker room elements; and do not carry through the plank pose, stability ball, plant, dark tank top, standing pose, or any background, logo styling, ad text, or notification UI graphic from either of the two identity reference images."

ReferenceAssetManifest:
  - asset_id: asset_01
    filename: "image1.png"
    type: Brand-Bearing
    prompt_reference_id: reference_asset_01
    attach_to_api_call: true
    strictness: Exact
  - asset_id: asset_04
    filename: "image4.png"
    type: Brand-Bearing
    prompt_reference_id: reference_asset_02
    attach_to_api_call: true
    strictness: Exact
  - asset_id: asset_07
    filename: "image7.png"
    type: Identity-Bearing
    prompt_reference_id: reference_asset_03
    attach_to_api_call: true
    strictness: "Near Exact — face, hair, and build only"
  - asset_id: asset_08
    filename: "image (1).png"
    type: Identity-Bearing
    prompt_reference_id: reference_asset_04
    attach_to_api_call: true
    strictness: "Near Exact — face and hair only"
```

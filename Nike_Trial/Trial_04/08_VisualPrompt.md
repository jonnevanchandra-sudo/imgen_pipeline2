# Visual Prompt
**Brand:** Nike
**Campaign:** Nike Chill Run Club — Trial 04
**Framework:** Prompt Compiler v2.3 (8.1.1)
**Stage:** 8 — Prompt Translation

---

```yaml
VisualPrompt: "Editorial lifestyle photography. Instagram 4:5 vertical format, 1080×1350px. Two subjects mid-run in a Hong Kong urban environment at evening or night. Subject 01 is the user — see reference_asset_01 for subject appearance; reproduce face and physical appearance from reference_asset_01 exactly, do not generate independently. Subject 02 is Karina from aespa — see reference_asset_02 for subject appearance; reproduce Karina's appearance from reference_asset_02 with her name as generation anchor; do not describe or generate her appearance from training data. Both subjects are running together at a comfortable, conversational pace — side by side or in easy near-proximity, clearly in shared motion. Neither subject is racing or sprinting. This is a social run, not a performance. Both faces carry ease and warmth in motion — not athletic intensity, not a pose for the camera, not effort or strain. The specific quality of being mid-run with good company: present, light, alive. The stride is natural — bodies in genuine running motion, not exaggerated or posed. Body language communicates proximity and shared pace: they are aware of each other, running together. Both subjects wear the Nike Alphafly 3 on their feet. The shoe is visible on at least one foot mid-stride. Nike Alphafly 3 key identifiers: extreme-stack ZoomX foam midsole — very tall, the most visually distinctive height profile of any running shoe; lightweight Atomknit race upper — thin, form-fitting, breathable; Nike Swoosh on the lateral side; thin rubber outsole pods, not a full ground-contact outsole; aggressive racing flat silhouette with elevated stack. The colorway of the shoe is reference_asset_03 — reproduce it exactly: same colors, same proportions, same lateral swoosh profile. Do not substitute a different Nike shoe or a generic running shoe; this is specifically the Nike Alphafly 3 in the colorway shown in reference_asset_03. Camera at approximately chest-to-waist height of running subjects — slight low or eye-level angle. Medium to three-quarter body framing: subjects from approximately mid-thigh to top of head, capturing both faces and the stride with shoe visible. Both subjects at slight lateral or three-quarter angle — running across or slightly toward the camera, both faces partially readable, mid-stride foot naturally exposed on at least one subject. Near-to-medium camera distance: subjects fill the frame, feels like running alongside them. Slight natural motion blur on swinging arms and trailing foot is acceptable and increases authenticity; faces remain sharp. Moderate to shallow depth of field: subject faces and bodies sharp in foreground; Nike Alphafly 3 on mid-stride foot in sharp to moderate focus; HK city background in warm motion-softened bokeh. Warm city ambient evening and night light: warm amber-orange from streetlamps as primary directional source, enriching skin tone and reading warmly on running apparel; cooler diffuse city skyline glow as secondary fill; the specific warm-cool mixed-temperature atmosphere of HK after dark. Subjects slightly brighter than background through natural luminance contrast — not a spotlight effect. No studio flash, no dramatic cinematic rim light, no cold or blue-dominant lighting on skin. HK outdoor urban environment at night: city lights active, harbourfront, Tsim Sha Tsui waterfront, or dense HK urban street; HK skyline, harbour, or vertical urban density visible in background as warm city bokeh; unmistakably Hong Kong — not a generic Asian night city. Athletic apparel on both subjects: varied, individual, not matching or coordinated. Running apparel shows natural wind-catch and movement at pace. Natural skin texture on both subjects — real, photographically credible, not smoothed or AI-idealized. ZoomX foam midsole reads as lightweight foam: slightly matte, not hard rubber. Top 10% of frame clear — reserved for Cantonese headline copy overlay in post-production. Bottom 20% of frame clear — reserved for Nike product name and CTA overlay in post-production. No faces, shoes, or critical visual content in these zones. Negative: no competitive race or marathon context; no sprint intensity or athletic grimace; no posed stop for the camera — both subjects in genuine motion; no celebrity-shoot staging that elevates one subject above the other; no product-isolated shoe display; no generic Asian city — must be recognizably Hong Kong; no golden hour or daylight; no studio lighting or dramatic cinematic rim; no matching or coordinated outfits; no hyper-polished or AI-smoothed skin; no indoor setting; do not generate subject_01 face independently — use reference_asset_01; do not generate Karina's appearance independently — use reference_asset_02; do not generate the Alphafly 3 colorway independently — use reference_asset_03."

ReferenceAssetManifest:
  - asset_id: asset_01
    filename: user_face.jpg
    type: Character-Identity
    prompt_reference_id: reference_asset_01
    entity_id: entity_01
    attach_to_api_call: true
    strictness: Exact
  - asset_id: asset_02
    filename: karina_reference.jpg
    type: Character-Identity
    prompt_reference_id: reference_asset_02
    entity_id: entity_02
    attach_to_api_call: true
    strictness: Exact
  - asset_id: asset_03
    filename: alphafly3_reference.jpg
    type: Brand-Bearing
    prompt_reference_id: reference_asset_03
    entity_id: entity_03
    attach_to_api_call: true
    strictness: Exact
```

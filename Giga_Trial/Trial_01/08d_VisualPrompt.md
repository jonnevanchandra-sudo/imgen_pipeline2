# Update (ignore)
Create a scene block to make it more detailed

# Visual Prompt
**Brand:** GigaSports
**Campaign:** Gigasports Pickle Club Community
**Framework:** Prompt Compiler v3.0 (with SCENE block)
**Stage:** 8 — Prompt Translation

---

```json
{
  "VisualPrompt": {

    "CRITICAL": {
      "subjects": "2 to 3 young Hong Kong professionals in their mid to late twenties. At least two subjects are visibly interacting with each other — not facing the camera. Facial expressions are unposed and mid-moment: open-mouth laughter, a relaxed expression mid-conversation, or a gesture caught mid-motion. Physical proximity between subjects communicates social comfort — they are close, relaxed, and at ease with each other. Natural variation in posture and weight distribution across subjects. No symmetry. No held poses. All faces must be clearly readable in the foreground — eyes, expression, and the social dynamic between subjects are the primary visual information in the frame.",
      "emotion": "The image must communicate authentic belonging — not performed happiness, not aspirational lifestyle, not sport achievement. The specific feeling of a group of real people genuinely enjoying time together in an active setting. The emotional register is warm, easy, and low-key. A viewer looking at this image should think: these are people like me, this looks like a social life I actually want, and I could belong here. The MemoryAnchor is: that pickleball post where the young professionals looked like they were genuinely having fun."
    },

    "HIGH": {
      "action": "The primary action is the social interaction between subjects — candid conversation, shared laughter, or a celebratory gesture such as a fist bump or high five captured mid-motion. This is a between-play moment: sport just happened and now people are connecting. Pickleball paddles are present in hand but held in a fully passive, relaxed position — at the side, resting on a shoulder, or loosely at hip height during conversation. Paddles must not be raised, gripped actively, or positioned in any way that reads as preparation for play.",
      "brand": "GigaSports logo or branded signage is clearly visible on a wall or banner in the background of the venue. The brand element sits in the soft bokeh of the background but must remain legible — a viewer looking at the background should be able to identify GigaSports. The brand presence feels like it belongs to the venue naturally, not like a logo stamped onto the image as an afterthought.",
      "setting": "Indoor pickleball court venue. Pickleball net and court line markings are visible in the midground behind subjects. The environment communicates an active, communal sports facility — a real place where a social community regularly meets. The venue feels warm and inclusive, not institutional, not high-end exclusive, and not empty or pristine.",
      "skin": "All subjects must have natural human skin — visible pore texture, subtle tone variation, and realistic surface imperfection. No AI-smoothed, porcelain, or plastic skin rendering. Skin must look like a photograph of a real person, not a digital render."
    },

    "LOW": {
      "style": "Realistic lifestyle editorial photography. The image should be indistinguishable from a candid photograph taken by a skilled lifestyle photographer at an actual GigaSports pickleball club event. Professional production value but never clinical, artificial, or studio-produced."
    },

    "FORMAT": {
      "aspect_ratio": "Instagram 4:5 vertical format, 1080 by 1350 pixels.",
      "safe_zones": "The top 10% and bottom 20% of the frame are reserved for text overlay. No faces, no paddles, no GigaSports brand elements, and no critical visual information of any kind may appear in these zones. Subjects' faces and key body language must be fully contained within the central 70% of the frame. This is a hard composition constraint — the image will have Cantonese headline copy placed in the top zone and a membership CTA placed in the bottom zone in post-production."
    },

    "LIGHTING": {
      "quality": "Soft and diffused throughout. No hard shadows, no sharp shadow edges, no dramatic contrast between lit and unlit areas.",
      "temperature": "Warm color temperature throughout the entire scene. The warmth communicates social energy and community — the feeling of a welcoming, active indoor space rather than a clinical facility.",
      "source": "Overhead ambient fill light consistent with an indoor sports venue. A subtle, warm directional key light separates subjects from the background. The key is soft — it should feel like a slightly more favorable position under the venue's overhead grid, not a dedicated photographic light source.",
      "hierarchy": "Subjects in the foreground are naturally brighter than the background due to their proximity to overhead lighting. This brightness differential separates the subject group from the venue background without creating artificial highlighting or studio-style separation.",
      "prohibited": "No harsh under-eye shadows. No dramatic rim lighting. No cinematic high-contrast ratios. No cold or neutral color temperature. No studio flash or strobe appearance. No single dominant directional light that creates theatrical atmosphere."
    },

    "CAMERA": {
      "shot_type": "Medium shot — enough of each subject's body is visible to read posture, body language, and social dynamic. Subjects are not cropped at the neck or waist in a way that removes social context.",
      "angle": "Eye-level. The camera is at the same height as the subjects' faces. This communicates equality — the viewer is standing with the subjects, not observing them from above as a spectator and not looking up at them as aspirational figures.",
      "distance": "Near distance. Subjects fill the foreground and dominate the frame. Faces are large enough that expressions are clearly readable without zooming in. The social dynamic between subjects — who is laughing, who is responding, how they are oriented toward each other — must all be readable at normal viewing size.",
      "depth_of_field": "Shallow depth of field. The subject group is in sharp, crisp focus. The midground court and net are in moderate focus — recognizable but not detailed. The background venue and GigaSports brand element are in soft, warm bokeh. The bokeh on the background must be calibrated so that the GigaSports brand element is soft but still legible — identifiable as a brand mark, not an unreadable blur.",
      "optical_notes": "Natural bokeh quality — soft circular diffusion consistent with a fast prime or short telephoto lens in an indoor venue. No anamorphic oval bokeh. No stylized optical effects. No artificial lens flare."
    },

    "AUTHENTICITY": {
      "human_authenticity": "Expressions must be caught mid-moment — laughter mid-exhale, a word mid-sentence, a gesture mid-motion. No expressions that have been held for a camera. No directed smiling toward the lens. Natural variation in engagement between subjects — one may be more animated than the other, and that asymmetry is correct. Subjects' weight distribution should be uneven and natural — a hip slightly cocked, a foot turned out, a slight lean toward the person they are talking to.",
      "environmental_authenticity": "The venue must feel used and active. Court line wear is acceptable and preferred. Natural ceiling structure — exposed beams, standard venue grid lighting, acoustic panels — is correct. Ambient lighting inconsistency typical of indoor sports venues is correct. The court surface should show texture from use. The environment should feel like a place where people regularly play, not a showroom or a set.",
      "material_authenticity": "Fabric wrinkles and natural drape on athletic casual wear. Natural skin texture on all subjects — no over-smoothed or idealized skin rendering. Slight sheen variation on paddle surfaces. Court surface grain visible underfoot. No hyper-polished material perfection anywhere in the frame.",
      "imperfection_rule": "Credibility takes priority over visual perfection. A slightly asymmetric composition is correct. A partially obscured face at the edge of the group is correct. A motion blur on a gesturing hand is correct. These imperfections distinguish the image from generic commercial stock photography and signal that a real moment was captured."
    },

    "SCENE": {
      "depth_structure": "Foreground layer: subject group (entity_01) and pickleball paddles they are holding (entity_02) — these occupy the primary visual weight of the frame and must be the largest, sharpest elements. Midground layer: pickleball court surface and net (entity_03) — visible behind and below subjects, establishing sport context without competing for attention. Background layer: indoor venue environment (entity_04) and GigaSports brand element (entity_05) — atmospheric, soft in bokeh, present but receded. Nothing in the background may compete visually with the foreground subjects.",
      "spatial_relationships": "Subjects within the group face each other — their bodies and eye-lines are directed toward one another, not toward the camera. The GigaSports brand signage is visible directly behind the subject group, centered or near-centered behind them so it reads over their shoulders in the background. The pickleball net is visible in the midground behind the subjects, running horizontally across the lower-mid portion of the frame. Paddles are physically attached to subjects — held in their hands, not floating, not propped, not placed on the ground.",
      "anchor_relationships": "Subject group is floor-anchored — both feet of each visible subject make contact with or are clearly grounded on the court surface. The pickleball net is floor-anchored as a fixed structural element running across the midground. The GigaSports brand element is wall-anchored or surface-mounted — it appears as a fixed sign or banner on the venue wall, not a floating overlay. Paddles are attached-to subjects — they are extensions of the subjects' hands.",
      "scale": "Subjects at realistic human scale dominate the frame — they should occupy roughly 60 to 70% of the vertical frame height. Paddles are proportional to human subjects at standard pickleball paddle size. The GigaSports brand element is at environmental venue scale — large enough to read as a venue sign, not oversized to the point of dominating the background. The court net is at standard net height relative to the subjects standing near it."
    },

    "NEGATIVE": "No athletic performance, competitive intensity, or high-effort sport execution of any kind. No mid-swing shots. No ball in frame. No aggressive or focused play stances. No solo subject — a single person directly contradicts the community concept and the primary communication. No formally posed group photography — no subjects arranged in a lineup or structured formation facing the camera. No retail product display or equipment-as-hero framing where paddles or gear dominate the visual hierarchy over human subjects. No outdoor setting — all elements must be coherent with an enclosed indoor sports venue. No studio lighting, dramatic rim lighting, moody cinematic contrast, or any lighting that reads as artificially produced. No hyper-polished or idealized skin rendering on any subject. No exclusive, elite, high-performance, or athletically intimidating visual language of any kind."

  }
}
```

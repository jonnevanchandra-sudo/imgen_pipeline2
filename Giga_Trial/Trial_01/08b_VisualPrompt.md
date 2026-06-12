# Updates (ignore)
Make it to json format with NLP content
Add priority list (taken from the synthesis contract) 

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
      "subjects": "2 to 3 young Hong Kong professionals in their mid to late twenties, caught in a genuine candid social moment between pickleball rallies. At least two subjects are visibly interacting — not looking at the camera. Expressions are unposed: open-mouth laughter mid-moment, a relaxed smile mid-conversation, or a gesture mid-motion. Physical proximity between subjects communicates social comfort, not formal distance. Natural variation in posture and weight distribution — no symmetry, no held poses. Faces are fully readable: eyes, expressions, and the social dynamic between subjects must all be clearly visible in the foreground.",
      "emotion": "The image must communicate authentic belonging — the feeling that these are real people genuinely enjoying time together, not performing for a camera. The emotional register is warm, easy, and low-key: the specific feeling of a group of friends mid-laugh after a funny exchange on court. Not excitement, not performance, not aspiration. The viewer should think: these are people like me, and this looks like the social life I actually want."
    },

    "HIGH": {
      "action": "The social interaction between subjects is the primary action — conversation, laughter, or a celebratory gesture (fist bump, high five) captured mid-motion. Paddles are held loosely at the side, resting on a shoulder, or at hip height during conversation — never raised in a playing position. The between-play moment must read clearly: sport just happened, and now people are connecting.",
      "brand": "GigaSports logo or branded signage clearly visible on a wall or banner in the background of the venue. The brand element is soft in natural bokeh due to shallow depth of field, but must remain legible — a viewer looking at the background should be able to read GigaSports. The brand feels like it belongs to the venue, not like a graphic stamped onto the image.",
      "setting": "Indoor pickleball court venue. Pickleball net and court line markings visible in the midground behind subjects. The environment feels active and communal — a real, used sports facility with warm overhead ambient lighting. The venue communicates a sense of a place where a regular social community meets, not an empty pristine facility or a high-end private club."
    },

    "MEDIUM": {
      "camera": "Eye-level medium shot at near distance. Subjects fill the foreground of the frame — enough of their bodies visible to read body language and social dynamic, but faces remain the dominant element. Camera height communicates equality with subjects: the viewer is standing with them, not observing from above or below.",
      "lighting": "Soft warm indoor venue lighting. Overhead ambient fill light with a subtle directional key that separates subjects from the background without creating theatrical shadow or dramatic contrast. Subjects are slightly brighter than the background — a natural consequence of foreground positioning under venue lighting, not artificial highlighting. Color temperature is warm. No harsh shadows under eyes or chin.",
      "authenticity": "Real venue imperfections are present and intentional: court line wear, natural ceiling structure, ambient lighting inconsistency typical of indoor sports venues. Fabric wrinkles and natural drape on athletic casual wear. Natural skin texture on faces — no over-smoothing. A slightly asymmetric composition, a partially obscured face, or a motion blur on a hand all increase credibility and distinguish the image from generic commercial stock photography."
    },

    "LOW": {
      "format": "Instagram 4:5 vertical format. Top 10% and bottom 20% of the frame are reserved as empty text-safe zones for Cantonese headline copy and membership CTA overlay respectively. No critical visual information — faces, paddles, brand element — should be placed in these zones.",
      "style": "Realistic lifestyle editorial photography quality. The image should be indistinguishable from a candid photograph taken by a skilled lifestyle photographer at an actual GigaSports pickleball club event. Professional production value but not clinical, artificial, or studio-produced."
    },

    "NEGATIVE": "No athletic performance, competitive intensity, or high-effort sport execution — no mid-swing shots, no ball in frame, no aggressive play stances. No solo subjects — a single person contradicts the community concept entirely. No formally posed group photography — subjects must not be arranged facing the camera in a lineup or structured formation. No retail product display or equipment-as-hero framing. No outdoor setting — the scene must remain coherent with an indoor sports venue. No studio lighting, dramatic rim lighting, or cinematic contrast ratios. No hyper-polished or idealized skin rendering. No imagery that reads as exclusive, elite, or athletically intimidating."

  }
}
```

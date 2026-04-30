# Lipstick / Makeup Product Recommendation Report

Use this reference when the user asks for lipstick recommendations, makeup product color choices, brand-specific lip shades, beauty shopping, or same-face lip-color try-on reports.

## Output Goal

Generate one vertical 9:16 or 3:4 premium beauty infographic based on the user's selfie or portrait. The image should feel like a high-end beauty consultant report plus brand editorial layout, not a cluttered shopping poster.

## Input Variables

- User image: the user's selfie or portrait, used as the primary identity reference.
- Brand: Dior, YSL, Armani, Chanel, Tom Ford, or another user-specified brand.
- Style preference: commute, gentle, aura, clean, photogenic, brightening, date, formal, daily, or user-specified.
- Recommendation count: 3-5 shades.

## Analysis Layer

Before recommending shades, infer from the user's actual photo:

- Skin undertone: cool, warm, neutral, olive, plus brightness level.
- Contrast level: low, medium, high.
- Temperament: cool, gentle, bright, clean, mature, soft, sharp, elegant, sporty, or relaxed.
- Lip base: original lip color depth, lip shape, suitable intensity, whether heavy color would overwhelm the face.
- Makeup state: bare face, daily makeup, polished makeup, strong makeup.

Output a one-line conclusion inside the prompt, for example: `better suited to muted rose-brown + medium saturation + satin/matte texture`.

## Brand Visual Layer

Map the brand into subtle visual cues only:

- Dior: elegant French softness, gray-white, silver lines, soft light.
- YSL: black/gold, high contrast, fashion editorial, sharp dividers.
- Armani: muted matte, gray tone, restrained luxury, low contrast.
- Chanel: strict black/white, clean alignment, rational minimalism.
- Tom Ford: dark cinematic luxury, deep contrast, polished highlights.

Use brand cues as thin lines, small icons, shade title accents, dividers, and typography mood. Do not add fake logos unless the user supplies them. Do not flood the poster with brand colors.

## Layout Contract

Vertical premium beauty infographic.

- Top or upper-left: user input portrait with a small `skin tone analysis` label.
- Upper-right: one-line diagnosis conclusion.
- Middle 60%: the core try-on matrix with 3-5 columns or an elegant grid. Each column shows the same face with only the lip color changed.
- Each shade module includes shade number/name, color family, effect, and scene tag.
- Bottom: concise consultant suggestion, such as daily best pick, photo best pick, and formal/event best pick.

Keep margins clean, text readable, spacing breathable, and the hierarchy obvious.

## Prompt Skeleton

```text
Create one vertical 9:16 premium lipstick recommendation infographic based on the uploaded reference portrait.

Use the uploaded image as the primary identity reference. Keep the same face shape, eyes, nose, lips, skin texture, age impression, expression temperament, and lighting family. Do not create different models. The only major visual change across the try-on matrix is lip color.

Brand: [BRAND]
Style preference: [STYLE PREFERENCE]
Recommendation count: [3-5]

First analyze the user from the portrait: skin undertone, brightness, contrast, temperament, original lip color, lip shape, and current makeup state. Then recommend [3-5] differentiated lip shades from [BRAND]. Each shade should have a distinct use case: daily, brightening, aura, date, formal, or photo-friendly.

Brand visual system: [brand visual cues]. Use brand accents only as thin lines, small section tags, dividers, shade labels, and subtle typography mood. No fake logo, no large brand color blocks.

Layout:
- Upper-left: reference portrait + short skin tone analysis label.
- Upper-right: one-line conclusion: `best direction: [color family] + [saturation] + [texture]`.
- Middle 60%: same-face lip-color try-on matrix, [3-5] columns. Each face must be the same person, same angle, same light, same skin texture; only the lipstick color changes.
- Under each shade: shade name/number, color family, one-line effect, scene tag.
- Bottom: concise consultant summary with daily pick, photo pick, and formal pick.

Visual style: high-end beauty editorial, structured information design, realistic skin texture, accurate lip color, unified lighting, clean premium typography, clear readable Chinese labels, subtle English support labels.

Avoid: different faces in different columns, plastic skin, fake logos, over-retouching, giant color blocks, unreadable text, excessive product packaging, exaggerated lip shape changes, random shade names, cluttered PPT layout.
```

## Safety / Practical Note

Treat product shade recommendations as visual and shopping references. Real color may vary by lighting, monitor, skin condition, and product batch.

# Beard / Grooming Analysis Report

Use this reference when the user asks for beard style, moustache, shaving choice, male grooming, facial hair, jawline styling, or whether a beard suits them.

## Output Goal

Generate one premium grooming analysis report, usually horizontal 4:3 or square 1:1. The image should compare facial-hair options while keeping the same person and avoiding any change to facial bone structure.

## Input Variables

- User image: front portrait, optionally with side profile.
- Desired style: clean, mature, rugged, elegant, Korean clean, business, street, vintage, or user-specified.
- Maintenance level: low, medium, high.
- Optional constraints: workplace, dating, photo, formal, daily, sensitive skin, patchy beard.

## Analysis Layer

Infer from the user's photo:

- Face shape and lower-face proportion.
- Beard density and growth pattern.
- Jawline definition and chin balance.
- Moustache density and connection to beard.
- Skin visibility and likely patchiness.
- Hair style linkage: whether facial hair should echo the hairstyle and glasses.
- Maintenance difficulty and daily compatibility.

## Layout Contract

- Main area: same-person front portrait as the identity anchor.
- Optional side profile: smaller side-view card if the input supports it.
- Analysis module: face shape, beard density, jawline definition, growth pattern, maintenance level.
- Comparison module: 4-6 beard options.
- Suitable / try / avoid labels, or a simple suitability score.
- Bottom guide: trimming length, neckline/cheekline, moustache handling, maintenance cycle, product/tool suggestions.

Recommended option set:

- Clean Shave
- Light Stubble
- Short Boxed Beard
- Goatee
- Van Dyke
- Full Beard / Longer Beard only if density supports it

## Prompt Skeleton

```text
Create one premium BEARD STYLE ANALYSIS grooming infographic featuring the same man from the uploaded reference image.

Use the uploaded image as the primary identity reference. Keep the same face shape, eyes, nose, lips, skin texture, hairline, hairstyle, age impression, and expression temperament. Only change facial hair. Do not change bone structure, do not make the jaw artificially wider, do not change the person's identity.

Analyze: face shape, beard density, jawline definition, chin balance, moustache density, beard growth pattern, skin visibility, and daily maintenance difficulty.

Layout:
- Main hero: realistic front portrait of the same person.
- Optional small side profile card if useful.
- Key Features panel with icons: Face Shape, Beard Density, Jawline Definition, Growth Pattern, Maintenance Level.
- Best Options row with green indicators: [3-4 suitable facial-hair styles selected for this person].
- Worth Trying row: [1-2 styles that may work with maintenance or growth].
- Less Flattering / Avoid row with red indicators: [2-3 styles that do not suit the face or density].
- Bottom Grooming Guide: neckline, cheekline, moustache length, trimming cycle, tools/products.

Visual style: premium male grooming poster, modern dark blue / charcoal / cream background depending on the person's style, clean infographic hierarchy, stylish typography, subtle icons, realistic face consistency, readable short Chinese labels with English support tags.

Avoid: different faces across options, exaggerated fake beard, changing jawbone, humiliating avoid examples, overly macho stereotype, plastic skin, unreadable text, messy collage, medical or surgical claims.
```

## Integration Rules

- If combined with hairstyle, make beard length support the haircut: clean hair + clean stubble, textured hair + short boxed beard, mature side part + light moustache, etc.
- If combined with glasses, make frame thickness and beard weight visually balanced.
- If combined with outfit, match grooming to scene: commute, date, streetwear, business, travel, or photo shooting.

## Practical Note

Facial-hair recommendations are visual references. Real results depend on beard growth density, trimming skill, workplace rules, and daily maintenance.

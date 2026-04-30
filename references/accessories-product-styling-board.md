# Accessories / Product Styling Board

Use this reference when the user wants accessory matching, product recommendations, shopping shortlist visuals, or a brand/product-aware personal styling board.

## When To Use

Use for requests like:

- 包包推荐 / 鞋子推荐 / 配饰推荐
- 首饰 / 手表 / 香水 / 美甲 / 护肤 / fragrance / skincare
- 这个品牌适合我吗 / 帮我做产品搭配图
- shopping shortlist / product styling board / accessory try-on

For lipstick or makeup shades, prefer `lipstick-makeup-recommendation.md`. For full clothing transformation, prefer `outfit-upgrade-report.md`.

## Prompt Skeleton

```text
Create one premium personal accessories/product styling board based on the uploaded reference image.

Task / output type:
One styling board with product recommendations and try-on/use-scene guidance.
Aspect ratio: [4:3 horizontal / 3:4 vertical / 1:1 square].
No large top title by default; use subtle section labels only.

Input variables:
Reference image: uploaded user photo.
Product category: [bags / shoes / jewelry / watch / perfume / nails / skincare / fragrance / mixed accessories].
Brand or price range: [optional].
User goal: [daily wear / commute / date / party / clean luxury / streetwear / feminine / masculine / neutral].

Analysis layer:
Analyze the user's face/style/color profile first:
- facial temperament and style axis
- current outfit baseline
- best metal tone or material direction
- best color depth and contrast level
- lifestyle scenes where the product should work

Layout contract:
- Main area: one identity-preserving portrait or half-body try-on reference, 35-45% of canvas.
- Product recommendation area: 3-6 product cards or object close-ups.
- Swatch/material strip: colors, metals, leather/fabric/finish, texture.
- Scene tags: where each option works, e.g. commute, date, travel, party, cafe, office.
- Use small readable Chinese labels and concise English tags only.

Content contract:
Each product option should include:
- option name or type
- color/material
- style role: refine / sharpen / soften / brighten / add personality
- best scene
- compatibility note with the person's face, outfit, and color profile

Visual system:
Premium fashion editorial board, clean cream/gray background, subtle thin dividers, realistic product photography, soft shadows, refined spacing. If brand-aware, use brand mood only as 5-10% accents: thin lines, micro tags, palette, lighting. Do not invent official logos.

Consistency rules:
When showing worn examples, keep the same face, body proportion, hair, and skin tone. Products may change; identity must not.

Strict avoid:
No fake logo claims, no crowded e-commerce poster, no giant discount stickers, no unreadable long paragraphs, no product overpowering the person, no changing the person's face, no plastic skin, no humiliating avoid examples.
```

## Product-Specific Notes

### Bags

Focus on scale, strap length, silhouette, hardware color, and scene. Show how bag size changes proportion and mood.

### Shoes

Focus on toe shape, sole height, trouser/skirt relation, leg-line effect, and walking practicality.

### Jewelry / Watch

Focus on metal tone, line thickness, face-feature weight, wrist/neck scale, and whether the item sharpens or softens the look.

### Perfume / Fragrance

Treat as mood and identity styling: scent family, bottle visual, scene, season, and outfit mood. Do not make medical or guaranteed attraction claims.

### Nails

Tie nail length, color, finish, and ornament density to hand style, skin undertone, work/lifestyle, and outfit direction.

### Skincare

Keep it cosmetic and routine-oriented. Avoid medical diagnosis, treatment promises, or disease claims.

## Verification

- The product category and user goal are explicit.
- The board analyzes the person before recommending products.
- Product options are differentiated by style role and scene.
- Brand cues stay subtle and non-deceptive.

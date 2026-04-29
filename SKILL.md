---
name: personal-style-advisor
description: Use when generating personal style consulting reports from user photos or style goals, including eyewear matching, Korean streetwear seasonal looks, outfit upgrades, personal color diagnosis, hairstyle upgrades, makeup/detail guidance, and facial aesthetic proposal boards.
version: 1.0.0
author: 唯一 + Hermes Agent
license: MIT
metadata:
  hermes:
    tags: [personal-style, fashion, beauty, eyewear, hairstyle, color-analysis, image-generation, xiaohongshu]
    related_skills: [popular-web-designs]
---

# Personal Style Advisor

## Overview

This skill turns a user's portrait, body photo, or style request into a high-completion personal style consulting output. It is optimized for image-generation prompts and visual reports in the style of premium proposal boards, fashion magazine layouts, Xiaohongshu-friendly guides, and before/after transformation reports.

Use it as a prompt framework library. The main job is to choose the right report type, preserve the user's identity, adapt the language to the user's goal, and produce a clean prompt or report structure that an image-generation model can follow.

## When to Use

Use this skill when the user asks for any of these:

- AI eyewear or glasses style matching reports.
- Outfit upgrade, personal styling, clothing improvement, or before/after wardrobe transformation.
- Four-season Korean streetwear or Seoul lookbook styling.
- Personal color diagnosis, seasonal color analysis, makeup colors, hair colors, and accessory color guidance.
- Hairstyle upgrade, haircut recommendation, bangs, volume, layers, hair color, or hair aesthetic report.
- Facial aesthetic upgrade report focusing on brows, eyes, nose, contour, lips, skin texture, or natural enhancement.
- Xiaohongshu-style image consulting cards, fashion report boards, or high-information visual prompt packs.

Do not use this skill for:

- Medical diagnosis, cosmetic surgery promises, or guaranteed treatment outcomes.
- Body shaming, face shaming, or humiliating comparison content.
- Replacing a licensed optometrist, dermatologist, plastic surgeon, makeup artist, or hairstylist when professional care is required.
- Generating identity-changing edits that make the person unrecognizable.

## Core Principle

Always preserve the user's identity. The output may improve styling, colors, hair, glasses, layout, and presentation, but it must not change who the person is.

Identity preservation requirements:

- Keep facial recognizability, age impression, face shape, core features, skin texture, expression temperament, and body proportions.
- For glasses, hairstyle, color, and facial aesthetic reports, keep original clothing unless the selected report type explicitly changes outfits.
- Before and After must look like the same person.
- Avoid template influencer faces, over-beautification, aggressive slimming, plastic skin, and unrealistic fashion edits.

## Workflow

1. Identify the report type from the user's request.
2. If the user uploaded an image, treat it as Image A and the primary identity reference.
3. If the user did not upload an image, ask for a portrait/body photo unless they only want a generic reusable prompt.
4. If the user asks for automatic matching, full suite, all photos, all reports, or `自动匹配风格`, run the Auto Full Style Suite workflow instead of choosing only one template.
5. Select the closest reference template from `references/`.
6. Adapt the template to the user's gender expression, age impression, body type, lifestyle, scene, and style preference.
7. Keep the final prompt specific, structured, and image-model friendly.
8. If generating an image, request the proper aspect ratio:
   - Eyewear report: horizontal 4:3.
   - Outfit upgrade report: horizontal 4:3.
   - Hairstyle report: horizontal 4:3.
   - Facial aesthetic report: horizontal 4:3.
   - Seasonal Korean streetwear: four separate vertical 3:4 images.
   - Personal color diagnosis: three separate vertical 3:4 images.
   - Auto Full Style Suite: multiple separate outputs, never one overcrowded mega-collage.

## Auto Full Style Suite

Use this workflow when the user uploads one photo and wants everything generated automatically, such as `自动匹配风格`, `所有报告都做`, `把所有照片都弄成`, `一张照片生成全套`, or `全案`.

### What To Produce

Generate or prepare prompts for a complete personal style suite:

1. `AI 眼镜风格适配报告` — one horizontal 4:3 image.
2. `AI 衣品升级改造报告` — one horizontal 4:3 image.
3. `四季韩系潮牌穿搭指南` — four vertical 3:4 images.
4. `个人色彩诊断三连图` — three vertical 3:4 images.
5. `AI 发型美学升级报告` — one horizontal 4:3 image.
6. `AI 五官美学升级报告` — one horizontal 4:3 image.

This means a complete suite can contain 11 separate images. Do not compress all modules into one image. If direct generation would be too large, produce it in batches and ask which batch to run first.

### Automatic Style Matching Pass

Before generating individual report prompts, analyze the uploaded photo once and create a shared style profile:

```text
Identity anchors: face recognizability, age impression, face shape, body proportion, original temperament
Face features: face shape, feature weight, brow-eye presence, nose bridge, jaw/contour, lip/mouth area
Color profile: likely undertone, contrast level, brightness, saturation tolerance, hair/eye/lip color cues
Body/styling profile: height impression, shoulder/waist/leg proportion, current outfit baseline, proportion goals
Style axis: clean / street / soft / sharp / mature / youthful / minimal / vintage / sporty / elegant
Avoid boundaries: what not to change, what not to exaggerate, what would look less flattering
```

Carry this shared profile into every report so the glasses, outfits, colors, hair, makeup, and facial aesthetic direction feel consistent.

### Batch Order

Recommended order for direct image generation:

1. Start with `眼镜风格适配报告` and `发型美学升级报告` because they preserve clothing and are easy to verify identity.
2. Generate `衣品升级改造报告`.
3. Generate `个人色彩诊断三连图`.
4. Generate `四季韩系潮牌穿搭指南`.
5. Generate `五官美学升级报告` last because it is the most sensitive and must stay subtle.

### Auto Suite Output Plan

When the user asks for the full suite but has not explicitly requested immediate image generation, first output this plan:

```text
我会基于同一张照片生成完整个人风格全案：
1. 眼镜报告 1 张，横向 4:3
2. 衣品升级 1 张，横向 4:3
3. 四季穿搭 4 张，竖向 3:4
4. 色彩诊断 3 张，竖向 3:4
5. 发型报告 1 张，横向 4:3
6. 五官美学 1 张，横向 4:3
合计 11 张图，建议分批生成。
```

Then proceed with the first batch if the user asked to generate directly; otherwise provide the grouped prompts.

## Report Types

### Eyewear Style Matching

Use `references/eyewear-report.md` when the user wants glasses, frames, eyewear, AI glasses, or before/after glasses matching.

Output goal:

- A horizontal 4:3 `AI 眼镜风格适配报告 / Before & After Glasses Style Matching Report`.
- Left Before portrait without glasses.
- Right After portrait with the best-matching glasses.
- Best Options, Worth Trying, Less Flattering/Avoid, and bottom Glasses Guide sections.

Must emphasize:

- Frame shape, width, bridge fit, thickness, color, and style mood.
- Practical daily-wear glasses, not runway props or exaggerated sunglasses.
- Clear suitable / can try / avoid hierarchy.

### Seasonal Korean Streetwear

Use `references/seasonal-korean-streetwear.md` when the user asks for four-season outfits, Korean streetwear, Seoul lookbook, seasonal color styling, or潮牌穿搭.

Output goal:

- Four independent vertical 3:4 finished images.
- Spring, Summer, Autumn, Winter Korean streetwear guides.
- Each image includes Before, Hero After, 5-6 lookbook outfits, palette, cautious colors, formulas, item suggestions, avoid notes, and consultant summary.

Must emphasize:

- Korean clean fit, Seoul street style, proportion optimization, high waistline, leg-lengthening, and real wearable styling.
- Each season must have distinct color, silhouette, material, mood, and styling route.
- Summer must include shorts; winter Hero After must include a Korean streetwear-style coat.

### Outfit Upgrade Report

Use `references/outfit-upgrade-report.md` when the user asks for clothing improvement, image upgrade, before/after style transformation,衣品升级, or making the person look more stylish.

Output goal:

- A horizontal 4:3 `AI 衣品升级改造报告 / Before & After Style Upgrade Report`.
- Strong Before vs After contrast.
- High-design personal proposal board with fit analysis, proportion improvement, style tags, item breakdown, and avoid guidance.

Must emphasize:

- Korean light streetwear, clean fit, city boy, urban casual, Japanese minimal streetwear, relaxed Hong Kong style, and daily wearable trendiness.
- After should be more stylish, sharper, more confident, and more photogenic.
- Avoid making After old-fashioned, overly businesslike, or like insurance-sales attire.

### Personal Color Diagnosis

Use `references/personal-color-diagnosis.md` when the user asks for seasonal color, personal color, makeup color, hair color, color palette, lipstick color, or color analysis.

Output goal:

- Three independent vertical 3:4 finished images, not one long collage.
- Page 1: `个人色彩 × 风格总诊断页 / Personal Color & Style Diagnosis`.
- Page 2: `色彩上身效果 × 穿搭应用页 / Color Draping & Styling Application`.
- Page 3: `妆容 × 发色 × 细节优化页 / Makeup, Hair & Beauty Detail Guide`.

Must emphasize:

- Do not preset a season, palette, lipstick, hair color, or fixed beauty template.
- Diagnose from the user's actual photo first, then generate colors, makeup, hair, accessories, and avoid lists.
- Treat color diagnosis as a bounded multi-option reference system, not one rigid answer.

### Hairstyle Upgrade Report

Use `references/hairstyle-upgrade-report.md` when the user asks for haircut, hairstyle, bangs, layers, hair volume, hair color, or发型美学升级.

Output goal:

- A horizontal 4:3 `AI 发型美学升级报告 / Before & After Hairstyle Upgrade Report`.
- Left original hairstyle, right best recommended hairstyle, plus Best Options, Less Flattering, and Hair Style Guide.

Must emphasize:

- Only upgrade hair: length, bangs, crown volume, side balance, layers, hair ends, texture, and natural color.
- Keep face, clothing, makeup, and identity unchanged.
- Natural Korean, clean cut, relaxed, low-maintenance, realistic hairstyle direction.

### Facial Aesthetic Upgrade Report

Use `references/facial-aesthetic-upgrade.md` when the user asks for facial aesthetic analysis, features, brows, eyes, nose, contour, skin, mouth area, or natural enhancement.

Output goal:

- A horizontal 4:3 `AI 五官美学升级报告 / Before & After Facial Aesthetic Upgrade Report`.
- Central Before/After face comparison with professional annotations.
- Bottom priority matrix and cautious guidance.

Must emphasize:

- Natural Korean clean beauty, subtle enhancement, and real texture.
- Analyze brows, eyes, nose, facial contour, lips/mouth area, and skin texture.
- Avoid medical promises and avoid overdone double eyelids, aggressive canthoplasty, high fake nose bridge, sharp V-face, overfilled lips, or plastic-skin smoothing.

## Output Modes

### Prompt Mode

When the user wants a prompt, output:

```text
【用途】
<which report type this prompt is for>

【生成比例】
<4:3 horizontal / 3:4 vertical / multi-image set>

【核心提示词】
<full adapted prompt>

【负面提示词】
<strict avoid list>

【使用说明】
<how many images, what reference image to attach, what to keep unchanged>
```

### Image Generation Mode

When the user asks to directly generate an image:

1. If a reference photo is needed but not present, ask the user to upload it.
2. If a reference photo is present, call the image generation tool with the adapted prompt.
3. For multi-image sets, generate each image separately and label them clearly.
4. Deliver image files directly when available.

### Consulting Text Mode

When the user wants written advice instead of images, output:

```text
整体判断：
适合方向：
推荐方案：
可尝试：
不推荐：
执行清单：
购物/搜索关键词：
下一步如果要生成图：
```

## Safety And Professional Boundaries

- Mention that eyewear reports are visual references and actual glasses should consider offline try-on and optometry.
- Mention that hairstyle advice should be confirmed with a hairstylist when cutting or coloring hair.
- Mention that facial aesthetic reports are not medical advice and do not replace doctor consultation.
- Avoid language that insults natural appearance. Use neutral framing such as `less flattering`, `not the strongest match`, or `lower daily compatibility`.
- Never claim certainty for medical, dermatological, or cosmetic-procedure outcomes.

## Common Pitfalls

1. Changing the user's identity in After images. The report fails if the person is not recognizable.
2. Treating templates as fixed outputs. Always adapt to the user's actual face, body, style, and request.
3. Making every report look like a PPT table. These prompts need magazine-like hierarchy, visual weight, and clear information design.
4. Putting too much text in generated images. Keep generated-image text short, readable, and label-like.
5. Using a single fixed beauty standard. Preserve personal temperament and provide multiple viable routes.
6. Making Avoid examples humiliating. Avoid sections should be realistic and lightly instructive, not mocking.
7. Defaulting every color analysis to warm, soft, or milk-tea palettes. Diagnose first, then recommend.

## Verification Checklist

- [ ] The selected report type matches the user's request.
- [ ] The aspect ratio and number of images match the template.
- [ ] The prompt explicitly preserves identity and avoids face/body replacement.
- [ ] The prompt focuses changes only on the requested category.
- [ ] Suitable / try / avoid layers are clear where applicable.
- [ ] Chinese text in image is requested as short labels, not long paragraphs.
- [ ] Professional disclaimers are included for optometry, hair, cosmetic, or medical-adjacent topics.
- [ ] The final result is useful, shareable, and visually feasible.

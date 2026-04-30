# Personal Style Advisor

A reusable Hermes Agent skill for creating high-completion personal style consulting prompts, portrait workflows, and visual report systems.

This skill is designed for AI-assisted personal styling, eyewear matching, beauty guidance, hairstyle upgrades, color diagnosis, outfit transformation, portrait photography, pose/action sheets, accessories/product styling, and before/after image proposal boards. It is especially suitable for Xiaohongshu-style visual reports, fashion magazine layouts, realistic personal portraits, and professional-looking personal style consulting cards.

The latest template expansion references the structured prompt approach and recent case taxonomy from [`freestylefly/awesome-gpt-image-2`](https://github.com/freestylefly/awesome-gpt-image-2): treat prompts as reusable visual protocols, lock layout and module contracts first, then add style, lighting, typography, and negative constraints.

## Project Vision

The goal is not to collect loose beauty prompts. This skill turns personal style requests into a controlled prompt system:

- Analyze first: face shape, feature weight, skin tone, contrast, hair, body proportion, temperament, and scene.
- Lock structure first: output type, aspect ratio, module count, layout hierarchy, text density, and consistency rules.
- Preserve identity first: every generated portrait, try-on matrix, report, or poster must still look like the uploaded person.

## Quick Entry

- [Skill definition](SKILL.md)
- [Examples](examples/)
- [Reference templates](references/)
- [Install in Hermes](#install-in-hermes)
- [Quick start prompts](#quick-start-prompts)
- [Safety and boundaries](#safety-and-professional-boundaries)

## What It Can Generate

### Core Style Reports

- **AI 眼镜风格适配报告** — eyewear / glasses matching report with suitable, try, and avoid frame options.
- **四季韩系潮牌穿搭指南** — four seasonal Korean streetwear lookbook guides.
- **AI 衣品升级改造报告** — before/after outfit and style upgrade proposal board.
- **个人色彩诊断三连图** — personal color diagnosis, color draping, outfit application, makeup, hair, and detail guide.
- **AI 发型美学升级报告** — hairstyle upgrade report with best cuts and avoid examples.
- **AI 五官美学升级报告** — natural facial aesthetic proposal board with cautious, non-medical guidance.
- **Auto Personal Style Suite** — upload one photo and automatically create a matched full styling plan across eyewear, outfits, colors, hairstyle, and facial aesthetics.

### New GPT-Image2-Inspired Modules

- **真实人像 / 生活方式照片** — realistic portrait, cafe photo, mirror/fisheye shot, street snapshot, dating profile photo, or editorial personal photo.
- **姿势 / 动作参考表** — 3x3 or 4x4 same-person pose grid, photo pose cards, dance/sport action reference, or movement breakdown sheet.
- **配饰 / 商品搭配板** — bags, shoes, jewelry, watches, perfume, nails, skincare, fragrance, shopping shortlist, or product-aware styling board.
- **口红 / 妆容产品推荐报告** — same-face lipstick or makeup try-on matrix, shade recommendations, and brand-aware beauty infographic.
- **胡须 / 男士 Grooming 分析** — beard, moustache, shaving, jawline grooming, and facial-hair option comparison.
- **时尚 Campaign / 海报模式** — magazine cover, sports fashion campaign, double-exposure portrait, typography poster, or shareable editorial visual.

## GPT-Image2 Reference Mapping

Relevant inspiration from `awesome-gpt-image-2` is mapped into this skill as reusable personal-style modules:

- `docs/gallery-part-2.md#case-347` — 4x4 action reference sheet -> pose/action reference grid.
- `docs/gallery-part-2.md#case-348` — beard style analysis poster -> beard/grooming report.
- `docs/gallery-part-2.md#case-349`, `#case-351`, `#case-356`, `#case-359` — sports/fashion/editorial campaign visuals -> poster/campaign mode.
- `docs/gallery-part-2.md#case-353` — branded lipstick recommendation infographic -> lipstick/makeup recommendation report.
- `docs/gallery-part-2.md#case-357` — fisheye mirror cafe portrait -> realistic personal portrait photography.
- `docs/gallery-part-2.md#case-360` — long hair styling analysis infographic -> hairstyle/detail report refinement.
- `docs/templates.md#tpl-photo` — photography template protocol -> lens, light, scene, and realism controls.
- `docs/templates.md` product/e-commerce and brand sections -> accessories/product styling board.

## Repository Structure

```text
personal-style-advisor/
  SKILL.md
  README.md
  LICENSE
  CONTRIBUTING.md
  examples/
    auto-full-style-suite-example.md
    single-image-five-in-one-example.md
    eyewear-report-example.md
    outfit-upgrade-example.md
    personal-color-diagnosis-example.md
    hairstyle-upgrade-example.md
    facial-aesthetic-example.md
  references/
    eyewear-report.md
    seasonal-korean-streetwear.md
    outfit-upgrade-report.md
    personal-color-diagnosis.md
    hairstyle-upgrade-report.md
    facial-aesthetic-upgrade.md
    personal-portrait-photography.md
    pose-action-reference-sheet.md
    accessories-product-styling-board.md
    lipstick-makeup-recommendation.md
    beard-grooming-analysis.md
    editorial-campaign-poster.md
```

## Install In Hermes

Clone this repository or download it, then copy the folder into your local Hermes skills directory:

```bash
mkdir -p ~/.hermes/skills/creative
cp -r personal-style-advisor ~/.hermes/skills/creative/
```

Restart Hermes or start a new session, then ask Hermes to use the skill:

```text
使用 personal-style-advisor，根据我的照片做一张 AI 眼镜风格适配报告。
```

> Note: Hermes skill loading is session-based. If the skill does not appear immediately, start a new Hermes session.

## Quick Start Prompts

### Single-Image Master-And-Modules Overview

```text
使用 personal-style-advisor。我会上传一张照片。请使用强参考本人模式，生成一张横向「AI 个人风格五合一适配报告」。

布局必须是：一张大主图作为整体风格定调，占画面 40-50%；旁边和下方放五个详情模块：眼镜适配、发型升级、衣品升级、色彩诊断、五官氛围。

不要做成五个等宽平铺栏目。每个模块要像 skill 里的报告缩略版：有小标题、适合/可尝试/不建议、色卡或单品拆解等细节。要求像本人，不要换脸。
```

### Auto Full Style Suite

```text
使用 personal-style-advisor。我会上传一张清晰正面或全身照片。请自动识别我的脸型、五官量感、肤色倾向、身材比例、气质方向和当前穿搭基础，然后自动匹配完整个人风格全案。

请一次性规划：AI 眼镜风格适配报告、AI 衣品升级改造报告、四季韩系潮牌穿搭指南、个人色彩诊断三连图、AI 发型美学升级报告、AI 五官美学升级报告。

所有报告都基于同一张照片，保持同一个人，不换脸，不变成模板网红脸。如果直接生成图片，请按批次生成，合计约 11 张，不要塞进一张大拼图。
```

### Realistic Portrait Photography

```text
使用 personal-style-advisor。我会上传一张本人照片。请按真实拍摄照片来生成一张 4:5 人像，不要做成报告卡。

场景可以是咖啡馆、街拍或镜面自拍风格。请保留我的脸型、五官、年龄感、气质和身材比例，只优化拍摄氛围、光线、姿势和穿搭呈现。
```

### Pose / Action Reference Sheet

```text
使用 personal-style-advisor。请基于我的照片，生成一张 4x4 姿势参考表。

每格都是同一个人、同一套穿搭和同一画风，只改变动作。每格有一个简短中文动作标签，适合拍照姿势练习，不要出现多余人物或复杂背景。
```

### Accessories / Product Styling Board

```text
使用 personal-style-advisor。请基于我的照片，生成一张配饰搭配板。

先分析我的风格、肤色和穿搭方向，再推荐 3-6 个包、鞋、首饰、香水或美甲方向。产品要服务于我的个人风格，不要喧宾夺主。
```

### Lipstick / Makeup Recommendation

```text
使用 personal-style-advisor。请基于我的自拍，生成一张口红/妆容产品推荐报告。

要求同一张脸做 3-5 个色号试色矩阵，只改变唇色和妆感，不改变五官。每个选项给出色系、适合场景和风格效果。
```

### Beard / Grooming Analysis

```text
使用 personal-style-advisor。请基于我的正面照片，生成一张胡须风格分析报告。

比较清爽剃净、短胡茬、短 boxed beard、goatee 等方向，只改变胡须和 grooming，不改变脸型骨相。
```

### Campaign / Editorial Poster

```text
使用 personal-style-advisor。请基于我的照片，生成一张高级个人时尚海报，不要做成咨询报告。

请先锁定构图，比如杂志封面、运动时尚大片、三联 Campaign 或水墨双重曝光人物海报。文字要少、准确、可读，重点保持本人辨识度。
```

### Eyewear Report

```text
使用 personal-style-advisor。请基于我上传的正面照片，生成一张横向 4:3 的 AI 眼镜风格适配报告。要求保留我的脸部辨识度，只改变眼镜，输出适合 / 可尝试 / 不推荐的镜框方案。
```

### Outfit Upgrade

```text
使用 personal-style-advisor。请基于我上传的全身照片，生成一张横向 4:3 的 AI 衣品升级改造报告。风格偏韩系轻潮、Clean Fit、City Boy，要求 Before / After 对比明显，但仍然像同一个人。
```

### Personal Color Diagnosis

```text
使用 personal-style-advisor。请基于我上传的人像照片，生成个人色彩诊断三连图：总诊断页、色彩上身与穿搭应用页、妆容发色细节页。不要预设季型，请根据照片自动判断。
```

### Hairstyle Upgrade

```text
使用 personal-style-advisor。请基于我上传的正面照片，生成一张横向 4:3 的 AI 发型美学升级报告。只改变发型，不改变五官、穿搭和妆容。
```

## How To Use With Image Generation

1. Upload a clear portrait or full-body photo.
2. Choose the output type: consulting report, realistic portrait, pose sheet, product board, or editorial poster.
3. First generate the master-and-modules overview when the user wants a compact cover image.
4. After the overview is approved, generate each module as its own detail image: eyewear, hairstyle, outfit, color, and facial atmosphere.
5. Add preferences such as gender expression, style direction, occasion, budget, brand/product preference, or avoid list.
6. Ask Hermes to generate the image directly or first produce the image-generation prompt.
7. For the full suite, generate in batches: overview first, then eyewear + hairstyle, then outfit, color pages, seasonal outfits, and facial aesthetics.

Recommended wording:

```text
先帮我生成提示词，不要直接出图。
```

or:

```text
请直接生成图片，不要只写文字描述。
```

## Design Principles

- Preserve the user's identity and recognizability.
- Keep Before and After as the same person.
- For photo requests, do not add report cards, titles, or consulting labels.
- For report requests, lock canvas structure, module count, and text density before style words.
- For grids and try-on matrices, keep the same face, outfit, light, and style; only change the target variable.
- For products and brands, use subtle accents and avoid fake official claims or fake logos.
- Prefer short readable labels over long paragraphs in generated images.
- Separate suitable, worth trying, and avoid options where applicable.
- Keep advice practical, respectful, and realistic.

## Safety And Professional Boundaries

This skill is for visual styling and personal image proposal workflows only.

- Eyewear suggestions do not replace optometry or offline try-on.
- Hairstyle suggestions do not replace a professional hairstylist consultation.
- Facial aesthetic suggestions are not medical advice and do not replace a doctor consultation.
- Fitness/action pose sheets are visual references, not medical or training prescriptions.
- Product recommendations are style references, not official brand endorsements.
- Avoid humiliating, body-shaming, face-shaming, or identity-changing edits.

## Attribution

This repository's recent prompt-structure expansion references public methodology and case categories from [`freestylefly/awesome-gpt-image-2`](https://github.com/freestylefly/awesome-gpt-image-2), especially its Prompt-as-Code orientation, gallery taxonomy, photography templates, action-reference case, beard/grooming case, lipstick/product infographic case, and campaign/poster cases. This skill adapts those ideas into a Hermes Agent personal-style workflow; original third-party materials remain owned by their respective authors.

## License

MIT

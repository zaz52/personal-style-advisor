# Personal Style Advisor

A reusable Hermes Agent skill for creating high-completion personal style consulting prompts and visual report workflows.

This skill is designed for AI-assisted personal styling, eyewear matching, beauty guidance, hairstyle upgrades, color diagnosis, and before/after image proposal boards. It is especially suitable for Xiaohongshu-style visual reports, fashion magazine layouts, and professional-looking personal style consulting cards.

## What It Can Generate

- **AI 眼镜风格适配报告** — eyewear / glasses matching report with suitable, try, and avoid frame options.
- **四季韩系潮牌穿搭指南** — four seasonal Korean streetwear lookbook guides.
- **AI 衣品升级改造报告** — before/after outfit and style upgrade proposal board.
- **个人色彩诊断三连图** — personal color diagnosis, color draping, outfit application, makeup, hair, and detail guide.
- **AI 发型美学升级报告** — hairstyle upgrade report with best cuts and avoid examples.
- **AI 五官美学升级报告** — natural facial aesthetic proposal board with cautious, non-medical guidance.
- **Auto Personal Style Suite** — upload one photo and automatically create a matched full styling plan across eyewear, outfits, colors, hairstyle, and facial aesthetics.

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

## Repository Structure

```text
personal-style-advisor/
  SKILL.md
  README.md
  LICENSE
  CONTRIBUTING.md
  examples/
    auto-full-style-suite-example.md
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
```

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
2. First generate the master-and-modules overview when the user wants a compact cover image.
3. After the overview is approved, generate each module as its own detail image: eyewear, hairstyle, outfit, color, and facial atmosphere.
4. Add preferences such as gender expression, style direction, occasion, budget, or avoid list.
5. Ask Hermes to generate the image directly or first produce the image-generation prompt.
6. For the full suite, generate in batches: overview first, then eyewear + hairstyle, then outfit, color pages, seasonal outfits, and facial aesthetics.

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
- Make reports visually useful, not just decorative.
- Prefer short readable labels over long paragraphs in generated images.
- Separate suitable, worth trying, and avoid options where applicable.
- Keep advice practical, respectful, and realistic.

## Safety And Professional Boundaries

This skill is for visual styling and personal image proposal workflows only.

- Eyewear suggestions do not replace optometry or offline try-on.
- Hairstyle suggestions do not replace a professional hairstylist consultation.
- Facial aesthetic suggestions are not medical advice and do not replace a doctor consultation.
- Avoid humiliating, body-shaming, face-shaming, or identity-changing edits.

## License

MIT

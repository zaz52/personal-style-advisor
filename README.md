# Personal Image Style Advisor

A reusable Hermes Agent skill for creating high-completion personal image consulting prompts and visual report workflows.

This skill is designed for AI-assisted personal styling, eyewear matching, beauty guidance, hairstyle upgrades, color diagnosis, and before/after image proposal boards. It is especially suitable for Xiaohongshu-style visual reports, fashion magazine layouts, and professional-looking personal image consulting cards.

## What It Can Generate

- **AI 眼镜风格适配报告** — eyewear / glasses matching report with suitable, try, and avoid frame options.
- **四季韩系潮牌穿搭指南** — four seasonal Korean streetwear lookbook guides.
- **AI 衣品升级改造报告** — before/after outfit and style upgrade proposal board.
- **个人色彩诊断三连图** — personal color diagnosis, color draping, outfit application, makeup, hair, and detail guide.
- **AI 发型美学升级报告** — hairstyle upgrade report with best cuts and avoid examples.
- **AI 五官美学升级报告** — natural facial aesthetic proposal board with cautious, non-medical guidance.

## Install In Hermes

Clone this repository or download it, then copy the folder into your local Hermes skills directory:

```bash
mkdir -p ~/.hermes/skills/creative
cp -r personal-image-style-advisor ~/.hermes/skills/creative/
```

Restart Hermes or start a new session, then ask Hermes to use the skill:

```text
使用 personal-image-style-advisor，根据我的照片做一张 AI 眼镜风格适配报告。
```

> Note: Hermes skill loading is session-based. If the skill does not appear immediately, start a new Hermes session.

## Repository Structure

```text
personal-image-style-advisor/
  SKILL.md
  README.md
  LICENSE
  CONTRIBUTING.md
  examples/
    eyewear-report-example.md
    outfit-upgrade-example.md
    personal-color-diagnosis-example.md
    hairstyle-upgrade-example.md
  references/
    eyewear-report.md
    seasonal-korean-streetwear.md
    outfit-upgrade-report.md
    personal-color-diagnosis.md
    hairstyle-upgrade-report.md
    facial-aesthetic-upgrade.md
```

## Quick Start Prompts

### Eyewear Report

```text
使用 personal-image-style-advisor。请基于我上传的正面照片，生成一张横向 4:3 的 AI 眼镜风格适配报告。要求保留我的脸部辨识度，只改变眼镜，输出适合 / 可尝试 / 不推荐的镜框方案。
```

### Outfit Upgrade

```text
使用 personal-image-style-advisor。请基于我上传的全身照片，生成一张横向 4:3 的 AI 衣品升级改造报告。风格偏韩系轻潮、Clean Fit、City Boy，要求 Before / After 对比明显，但仍然像同一个人。
```

### Personal Color Diagnosis

```text
使用 personal-image-style-advisor。请基于我上传的人像照片，生成个人色彩诊断三连图：总诊断页、色彩上身与穿搭应用页、妆容发色细节页。不要预设季型，请根据照片自动判断。
```

### Hairstyle Upgrade

```text
使用 personal-image-style-advisor。请基于我上传的正面照片，生成一张横向 4:3 的 AI 发型美学升级报告。只改变发型，不改变五官、穿搭和妆容。
```

## How To Use With Image Generation

1. Upload a clear portrait or full-body photo.
2. Tell Hermes which report type you want.
3. Add preferences such as gender expression, style direction, occasion, budget, or avoid list.
4. Ask Hermes to generate the image directly or first produce the image-generation prompt.

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

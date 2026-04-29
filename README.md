# Personal Image Style Advisor

A Hermes Agent skill for personal image consulting prompt workflows.

It helps generate high-completion visual report prompts for:

- AI eyewear / glasses style matching
- Korean streetwear seasonal styling
- Before & After outfit upgrades
- Personal color diagnosis
- Makeup, hair color, and beauty detail guidance
- Hairstyle upgrade reports
- Facial aesthetic upgrade reports

The skill is designed for Xiaohongshu-style image consulting cards, fashion magazine layouts, before/after proposal boards, and practical personal styling reports.

## Install

Copy this folder into your Hermes skills directory:

```bash
mkdir -p ~/.hermes/skills/creative
cp -r personal-image-style-advisor ~/.hermes/skills/creative/
```

Then start a new Hermes session and load/use the skill.

## Structure

```text
personal-image-style-advisor/
  SKILL.md
  references/
    eyewear-report.md
    seasonal-korean-streetwear.md
    outfit-upgrade-report.md
    personal-color-diagnosis.md
    hairstyle-upgrade-report.md
    facial-aesthetic-upgrade.md
```

## Notes

- The prompts emphasize preserving the user's identity and avoiding unrealistic over-beautification.
- Facial aesthetic content is for visual proposal and style reference only, not medical advice.
- Glasses, hair, color, and beauty guidance should be validated with real-world professionals where needed.

## License

MIT

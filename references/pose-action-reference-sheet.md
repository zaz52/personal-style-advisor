# Pose / Action Reference Sheet

Use this reference when the user wants photo pose guidance, posture options, movement breakdowns, dance/sport action steps, or a consistent multi-panel pose grid.

## When To Use

Use for requests like:

- 动作分解 / 动作参考表
- 拍照姿势 / 全身 pose 指南
- 舞蹈动作 / 运动姿势 / 健身动作参考
- runway pose / posture guide / character pose sheet

Do not use for a normal outfit report unless the user specifically wants pose or movement guidance.

## Prompt Skeleton

```text
Create one clean pose/action reference sheet featuring the same person from the uploaded reference image.

Task / output type:
A technical visual reference sheet, not a beauty poster and not a diagnosis report.
Aspect ratio: [1:1 square / 4:3 horizontal].
Grid: [4x4 = 16 panels / 3x3 = 9 panels / 2x3 = 6 panels].

Identity consistency:
Use the uploaded reference image as the primary identity source. Keep the same face shape, hairstyle, body proportion, outfit family, and age impression in every panel. Only the pose/action changes. Do not create different models.

Layout contract:
- Clean white or light neutral background.
- Equal-size panels separated by thin lines.
- Each panel has a small number badge and short title.
- Center of each panel: full-body pose or movement keyframe.
- Optional: 1-line note at the bottom of each panel.
- Add subtle arrows, rotation indicators, weight-shift lines, or motion trails where helpful.

Pose/action sequence:
[Define the sequence: photo posing set / walking sequence / dance move / tennis swing / gym form / runway turns / sitting poses / cafe poses].
Panel list:
1. [pose/action]
2. [pose/action]
3. [pose/action]
...

Visual style:
[realistic photo cutout / clean 3D reference / monochrome grayscale illustration / fashion pose guide / sports coaching board].
Unified lighting, consistent scale, clean spacing, readable labels.

Strict avoid:
No extra characters, no background scenery, no changing clothes between panels unless requested, no face replacement, no distorted anatomy, no unreadable long text, no chaotic arrows, no unsafe medical/training claims.
```

## Suggested Panel Sets

### Photo Pose 3x3

1. relaxed standing
2. one hand in pocket
3. slight shoulder turn
4. seated cafe pose
5. walking mid-step
6. looking over shoulder
7. leaning on wall
8. holding bag/phone naturally
9. close-to-camera casual pose

### Outfit Lookbook 2x3

1. front standing
2. side profile
3. walking pose
4. seated pose
5. detail close-up pose
6. final confident hero pose

### Sports / Movement 4x4

Use 16 keyframes from ready stance to finish pose. Add arrows for weight transfer, rotation, foot direction, and arm path.

## Verification

- Grid size is explicitly locked.
- Every panel uses the same person and same outfit family.
- Pose/action is the only intended variable.
- Text is short enough to be readable.

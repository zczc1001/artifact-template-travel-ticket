---
name: artifact-template-travel-ticket
description: "Create an image using the Travel Ticket 旅行票根 template and its retained reference file. Use when the user selects this template, names Travel Ticket 旅行票根, or explicitly invokes $artifact-template-travel-ticket. 把旅行照片制作成带有地点文字、编号、条形码、织物背景和真实纸张投影的复古票根海报。"
---

# Travel Ticket 旅行票根

Create an image from this template. Keep the reference file unchanged.

## Workflow

1. Read `artifact-template.json` and resolve its paths relative to this skill directory.
2. Invoke $imagegen with the retained PNG as a reference image and the user's requested content as the edit or generation brief.
3. Treat the user's prompt and available sources as the content input. Do not invent factual claims merely to fill the composition.
4. Preserve the reference's visual language unless the user explicitly requests a deviation.
5. Visually inspect the generated image for fidelity and defects, then return the final image.

## Fidelity

Preserve the reference image's composition, visual hierarchy, palette, typography, material treatment, lighting, and recurring brand elements.

User instructions control requested content and explicit deviations. The retained reference controls layout and formatting where the user has not requested a change.

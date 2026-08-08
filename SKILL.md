---
name: artifact-template-travel-ticket
description: "Create an image using the Travel Ticket 旅行票根 template and its retained reference file. Use when the user selects this template, names Travel Ticket 旅行票根, or explicitly invokes $artifact-template-travel-ticket. 把旅行照片制作成带有地点文字、编号、条形码、半自适应织物背景和真实纸张投影的复古票根海报。"
---

# Travel Ticket 旅行票根

Create an image from this template. Keep the reference file unchanged.

## Workflow

1. Read `artifact-template.json` and resolve its paths relative to this skill directory.
2. Invoke $imagegen with the retained PNG as a layout and material reference, and the user's photo as the content and color source.
3. Treat the user's prompt and available sources as the content input. Do not invent factual claims merely to fill the composition.
4. Preserve the reference's visual language unless the user explicitly requests a deviation.
5. Visually inspect the generated image for fidelity and defects, then return the final image.

## Semi-adaptive background color

The background hue is variable. Do not copy the blue hue from the retained reference by default. The retained reference controls the woven-fabric texture, lighting, shadow, and spatial composition—not a fixed background color.

For every source photo:

1. Identify one supportive dominant or secondary color from a large, visually important area of the photo, such as sky, water, foliage, masonry, night, or warm artificial light.
2. Convert it into a quiet background color by reducing saturation and, when needed, shifting lightness so the warm ivory ticket remains clearly separated from the backdrop.
3. Favor harmony over literal color matching. The background should echo the photo without competing with the photo window.
4. Choose the color independently for each image in a set. Do not force all outputs to share one hue.
5. Use blue only when the source photo genuinely supports blue or blue-gray. Otherwise use an appropriate muted family such as sage, moss, warm sand, ochre, terracotta, mauve, charcoal, or stone gray.
6. If the photo has no stable color cue, fall back to a neutral warm gray or stone tone rather than the reference blue.

Never introduce a saturated unrelated color, a multicolor gradient, or a background that reduces the contrast of the ticket edge.

## Fidelity

Preserve the reference image's composition, visual hierarchy, typography, material treatment, lighting, and recurring brand elements. Preserve the palette relationship and restraint, but derive the backdrop hue from the user's photo according to the semi-adaptive color rules above.

User instructions control requested content and explicit deviations. The retained reference controls layout and formatting where the user has not requested a change.

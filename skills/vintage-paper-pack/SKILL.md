---
name: vintage-paper-pack
description: Generate a cohesive pack of five distinct minimalist vintage monoline illustrations on textured aged paper. Use when the user requests a "vintage paper pack" for any theme, such as Halloween, Christmas, birthdays, or New Year, including Indonesian phrases "bikinkan vintage paper pack halloween".
---

# Vintage Paper Pack

## Goal
Create **exactly five individual illustrations** per request, visually coordinated like a premium icon collection. Default theme is provided by the user. Do not generate five unrelated styles or combine all five into one image unless explicitly requested.

## Default design system
- Illustration: vintage minimalist monoline, hand-drawn outline icons, thin consistent stroke, clean silhouettes, tasteful small ornamental details.
- No filled silhouettes, photorealism, 3D, heavy shading, gradients, letters, captions, numbers, logos, or watermarks unless requested.
- Background: subtle aged handmade paper, organic fibers, tiny random speckles, faint wear, non-uniform color; texture must be understated, not muddy.
- Palette: warm ivory (#F1EBDC) with dark ink (#25231E); optional alternate dark navy (#14243A) with champagne ink (#E9D9B5), or muted sage (#DDE3D5) with charcoal ink.
- Icons should have balanced visual weight, coherent line thickness and spacing, distinct recognizable subjects, and enough negative space.
- Prefer 1:1 for each image. Center each illustration with generous margins. No text.

## Workflow
1. Parse theme, quantity, aspect ratio, background, ink color, and delivery format. If absent, use five images, square 1:1, ivory paper, black ink. Do not ask unnecessary questions.
2. Select **five different instantly recognizable subjects** specific to the theme. Avoid duplicating motifs or repeating near-identical icons.
3. Establish one shared visual specification for the entire pack: line weight, icon scale, paper texture, background color, palette, and margins.
4. Generate each illustration as an **individual image** with the image-generation tool, sequentially if needed. Maintain consistent art direction across the five generations. Do not claim completion before all five exist.
5. Inspect each result for anatomy/orientation, broken contours, extraneous limbs, disconnected strokes, inconsistent scale, and unwanted text. Regenerate defective results when possible.
6. If tools allow file handling, export five separately named PNGs (`01-subject.png` through `05-subject.png`) and optionally ZIP them. If no file-handling capability is available, deliver five separate image outputs and explain any export limitation. Never claim PNG, ZIP, or transparent background without producing it.

## Subject example: Halloween
1. Seated black-cat outline with one tail and two ears.
2. Symmetrical spider web with a single eight-legged spider.
3. Rounded witch cauldron with delicate curling steam.
4. Classic witch broom with bound bristles.
5. Vintage lantern with a small candle flame.

## Generation prompt template
"A single [SUBJECT] icon in elegant minimalist vintage monoline illustration style. Thin clean hand-drawn [INK COLOR] outlines, consistent stroke weight, charming subtle ornamental detail, balanced recognizable silhouette, centered composition with generous negative space. On a [BACKGROUND COLOR] aged handmade paper background with extremely subtle organic paper fibers, faint grain and tiny scattered speckles. Cohesive premium vintage icon collection aesthetic. Square 1:1. No typography, no letters, no numbers, no border, no extra icons, no filled areas, no 3D, no gradients, no harsh shadows. Anatomically and structurally coherent."

## Reference composition option
If the user explicitly asks for a **single sheet** like their reference photos, arrange five icons horizontally with equal spacing on a 3:2 or 16:9 paper canvas; this is an alternative output, not a replacement for five separate files unless they request only a sheet.

## Quality checks
- Five distinct theme-specific subjects.
- Each icon is isolated and legible at small sizes.
- Same line thickness, same paper tone and texture, same scale and margin system.
- Correct anatomy/structure (e.g., cat: four limbs if visible, one tail; spider: eight legs).
- No stray marks, unwanted objects, letters, or accidental merged forms.

## Invocation examples
- "Bikinkan vintage paper pack Halloween"
- "Vintage paper pack Natal, background navy, garis emas"
- "Buat vintage paper pack ulang tahun, 5 gambar PNG rasio 1:1"
- "Vintage paper pack Halloween, satu lembar 5 ikon berjajar"

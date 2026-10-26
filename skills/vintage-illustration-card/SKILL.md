---
name: vintage-illustration-card
description: Create or revise a single colored vintage illustration card on subtle aged-paper texture, with a centered isolated subject, generous balanced margins, restrained decorative details, and square 1:1 format. Use when the user requests "vintage ilustrasion card", "vintage illustration card", or wants to turn an icon from a vintage paper pack into an individual colored card.
---

# Vintage Illustration Card

## Purpose
Turn one selected subject into **one finished, colored vintage illustration card**. Follow the user's reference and preserve continuity with any preceding vintage paper pack or approved image. The final Christmas tree example defines the baseline: one richly but tastefully colored object, centered on warm aged paper, **no surrounding sparkles, stars, dots, floating accents, glow rays, or ground decoration**.

This is distinct from `vintage-paper-pack`: a pack is five thin-line icons on a wide single sheet; a card is **one colored illustration on one square canvas**.

## Defaults
- Output: **one image**, **1:1 square**.
- Subject: the object the user names; if they say "yang paling kiri", use the leftmost icon in the latest pack. For sequential requests, preserve the same style across all cards.
- Style: hand-drawn vintage storybook illustration, tasteful flat/watercolor-like muted colors, fine dark-brown/charcoal ink outlines, lightly distressed print texture; neither photorealistic nor shiny 3D.
- Background: one continuous warm ivory/cream handmade aged-paper texture, with fine fibers and sparse organic speckles. No frame, panel, vignette, typography, logo, or watermark.
- Palette: natural, muted colors appropriate to the subject; user-selected background, outline, and object colors always override defaults.
- Placement: center the object horizontally and vertically, keeping **roughly 15–20% empty margin on each side** and sufficient space above/below. Aim for subject occupying about **60–70% of canvas height**, adjusted for its shape; do not crop.
- Decorations: details *on the object* are allowed when meaningful (e.g. Christmas ornaments, bows, garlands, snow on branches). **No floating decorative elements around the object** by default. No rays extending from a star topper.

## SEO-friendly title and metadata (required for every newly generated card)
After generating an illustration, provide a **descriptive English SEO-friendly title** suitable for a digital-product listing or image asset. Never output a bare generic subject name such as `Black Cat`, `Christmas Bell`, or `Gift`.

- Title pattern: **[distinctive subject + visible attributes] + [holiday/occasion] + [visual style or product intent]**. Use natural English, title case, approximately 6–12 words (roughly 45–90 characters when practical).
- Describe what is **actually visible**. Include relevant terms such as `Vintage`, `Halloween`, `Christmas`, `Watercolor`, `Illustration`, `Textured Paper`, `Printable` only when accurate. Do not imply transparency, SVG/vector, clipart cutout, licensing rights, or printable resolution without evidence.
- Do not keyword-stuff, repeat the same term, claim search rankings, or invent trend/search-volume data. Avoid unnatural strings like `Black Cat Ghosted Halloween Bla Bla Bla`. Use `Ghostly Black Cat Halloween Vintage Illustration` only if a ghostly quality is visually present.
- Also supply a short **SEO description** (one natural English sentence, ~15–30 words) and a lowercase **filename slug** with hyphens and no extension unless a real file has been exported.
- Titles and descriptions are **text delivered alongside the generated image**, NEVER written inside the artwork unless explicitly requested.
- For revisions to the same image, preserve the existing title unless the visual subject or key attributes materially change; do not force repetitive metadata on every minor edit.
- When creating multiple cards in a sequence, give each card its own distinct subject-specific title, avoiding duplicate titles.

Examples (adapt to the actual artwork):
- Black cat: `Mystical Black Cat Halloween Vintage Storybook Illustration`
- Christmas bells: `Golden Christmas Bells with Red Bow Vintage Watercolor Illustration`
- Christmas stocking: `Festive Red Christmas Stocking with Gifts Vintage Illustration`
- Christmas present: `Holly Wrapped Christmas Gift with Red Ribbon Vintage Illustration`
- Christmas tree: `Decorated Evergreen Christmas Tree Vintage Watercolor Illustration`

## Workflow
1. Determine subject from the request or preceding image; treat an attached/approved image as the primary reference for form, colors, layout, and visual identity.
2. Establish square composition, paper texture, palette, outline weight, and target subject scale. Respect explicit user overrides.
3. Generate **one** colored illustration using an image-generation tool. For edits, edit the supplied image when possible rather than replacing the entire design.
4. Inspect the result: object centered, ample margins on all four sides, one coherent subject, correct anatomy/structure, clean outlines, restrained object details, no unrelated props or floating embellishments.
5. If user says "kecilkan", decrease only subject size while keeping style and paper unchanged. If "besarkan sedikit", increase the subject by roughly 8–12% without touching edges. Preserve other details.
6. If user asks "hilangkan hal berlebih", remove all unrelated surrounding decorations (stars, sparkles, glow strokes, dots, ground marks), **but retain the subject and ornaments attached to it**. Keep a topper star if part of the Christmas tree, while removing rays around that star.
7. Never change subject pose, palette, ornament placement, or art style unnecessarily when the user requests a localized edit.
8. For each new finished card, deliver the image plus the SEO title, one-sentence SEO description, and filename slug in accompanying text, without placing text in the image.

## Prompt template — initial creation
"Create ONE 1:1 square vintage illustration card featuring a single [SUBJECT]. Use a charming hand-drawn vintage storybook style with delicate dark ink outlines, muted tasteful [COLORS] and subtle watercolor/aged-print texture. Center the isolated object at a medium scale, around 60–70% of the canvas height, leaving generous and balanced empty margins on the left, right, top, and bottom. A continuous [BACKGROUND COLOR] vintage handmade paper background with subtle fine fibers and organic speckles fills the entire canvas. Include only meaningful details physically attached to [SUBJECT]. No extra objects, no floating stars, no sparkles, no glow rays, no dots or confetti surrounding the subject, no ground strokes, no frame, no text, no logo, no watermark, no photorealism, no 3D. Correct anatomy and orientation."

## Prompt template — minimal cleanup of approved artwork
"Edit the supplied illustration minimally. Preserve the exact central [SUBJECT], its scale, placement, shape, color palette, attached ornaments, outline style, aged-paper texture, and square 1:1 canvas. Remove ONLY all unrelated floating decorations surrounding the subject, including sparkles, extra stars, dots, ground strokes and radiating lines around any topper star. Leave a clean, spacious vintage paper background. Do not redesign the subject."

## Example: Christmas tree
Keep a central evergreen with muted green branches, light snow on branches, red bows and ornaments, gold garlands and a single gold star at the top. **The topper star stays, but all rays around it are removed.** No floating sparkle stars around the tree. No drawn ground line under its trunk. Leave adequate margins on all four sides.

## Quality checklist
- [ ] Exactly one subject on one square canvas.
- [ ] Colored vintage storybook look with coherent ink outlines.
- [ ] Consistent, subtle textured-paper background.
- [ ] Balanced margins; object not oversized or cropped.
- [ ] No surrounding decorative clutter.
- [ ] Object structure and orientation are correct.
- [ ] User's requested edits affect only specified details.
- [ ] Requested palette and reference style are preserved.
- [ ] New cards have accurate, distinctive SEO title, short description, and filename slug outside the image.

## Invocation examples
- "Bikin vintage ilustrasion card Christmas tree"
- "Dari vintage paper pack Christmas, buat ikon paling kiri jadi card berwarna 1:1"
- "Vintage illustration card lonceng Natal, background sage green"
- "Besarkan sedikit pohonnya, tapi tetap ada ruang di semua sisi"
- "Hilangkan bintang-bintang di sekitar pohon dan garis cahaya dari bintang puncaknya"

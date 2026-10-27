---
name: ui-asset-generator
description: "Audit a UI screenshot to identify all required raster visual assets (hero backgrounds, illustrations, 3D renders, photos, card thumbnails, and portrait avatars) and directly generate and display the clean, UI-free image in the chat for visual comparison and iterative refinement. Use whenever the user shares a UI design screenshot and asks to extract, prepare, or generate the background/card/illustration assets before slicing into HTML/Tailwind."
---
# UI Asset Generator

Directly generate and display clean, high-resolution visual assets (backgrounds, hero illustrations, card thumbnails, and portrait avatars) in the chat from a UI design screenshot so the user can visually compare, iterate until it matches, and download the asset before slicing into HTML and Tailwind CSS.

## Summary

When a user provides a UI screenshot to prepare assets for slicing, inventory the non-vector visual assets and **immediately invoke the image generation tool** to display the clean, UI-free image directly in the chat. Support iterative visual refinement based on user feedback until the user is satisfied and ready to move to the next asset or slice the UI.

## When to Use

- The user uploads a UI design screenshot and invokes `@ui-asset-generator` or asks to generate/recreate the background image, hero illustration, or card thumbnails.
- The user provides feedback on a just-generated asset (e.g., "kurang mirip", "warnanya lebih terang", "posisinya geser ke kanan") to iterate and regenerate the image.

## Steps

### Step 1: Brief Asset Inventory

Scan the uploaded UI screenshot and list a compact inventory (3-5 lines max) of the raster visual assets needed for the page:

1. **Asset #1 (Primary Hero Background / Main Illustration)**: Aspect ratio, art style (e.g., anime hand-drawn, gouache painting, realistic photography, 3D render), color palette, subject placement, and negative space where UI text will sit.
2. **Asset #2+ (Secondary Assets, if any)**: Card thumbnails, bento photos, or standalone portraits.

### Step 2: Immediately Generate and Display the Image in Chat (Mandatory)

1. **Always call the image generation tool directly in your response** to produce and render **Asset #1** right inside the chat window.
2. **Do NOT output text-only prompts or SVG code as a substitute** when the image generator can be called. The user needs to see the actual generated raster image in the chat to compare it against their screenshot.
3. **100% UI-Free Artwork**: Exclude all headlines, buttons, navigation bars, badges, glass cards, and browser frames from the generated image. Preserve the exact negative space, horizon line, lighting direction, and color temperature of the reference so HTML text can be layered cleanly on top later.
4. Only generate **one image per turn** (since the image generation tool supports one image per response).

### Step 3: Visual Comparison & Iteration Loop

After generating and displaying the image in the chat:

1. Ask the user to compare the generated image with the original screenshot:
   - **If it needs adjustments**: The user will tell you what to fix (e.g., style, colors, camera angle, object placement, negative space). Immediately call the image generation tool again with a refined prompt incorporating their exact feedback. Repeat this loop until the user confirms it matches.
   - **If it matches and there are more assets**: When the user says "pas" / "lanjut", immediately generate and display **Asset #2** in the chat and repeat the comparison loop.
   - **If all assets are complete**: Instruct the user to download the final image(s) and upload them together with the original UI screenshot while calling `@precision-ui-slicing-opus-v2`.

## Gotchas

- **System Tool-Locking Note**: In this environment, calling a skill expansion tool (`retriever:expand_skills`) in the middle of a turn can sometimes temporarily hide the built-in image generation tool for that single turn. If the image generation tool is not visible in your tool declarations during the turn the skill is first expanded, tell the user in one short sentence: *"Ketik **'buat sekarang'** (tanpa tag `@`) agar gambar langsung tampil di chat!"* — on the very next turn, the skill instructions are already in context and the image generation tool will execute and display the image directly in the chat.
- Never include UI text, buttons, icons, or browser chrome inside the generated artwork.
- Never generate multiple images in a single turn; go one by one so each asset can be iterated to perfection.

---
name: asset-batch
description: Generate batches of visually consistent image assets as independent files, never a combined collage or sprite sheet.
---

# Asset Batch

## Goal
Generate multiple assets with **one requested asset per independent image file**. A single canvas containing multiple requested assets is not a valid batch.

## When to use
When the user requests multiple character expressions, poses, UI buttons, icons, decorations, props, or other visual assets, especially transparent PNGs.

## Non-negotiable contract
1. **One asset = one separate image output and file.** Never replace separate files with a grid, collage, contact sheet, character sheet, or sprite sheet.
2. One subject per canvas; no extra variants, labels, frames, or neighboring assets unless explicitly requested.
3. Transparent background by default for standalone assets; opaque for full-scene backgrounds unless otherwise specified.
4. Maintain reference character identity, clothing, proportions, palette, artstyle, and consistent margins and scale.
5. Do not claim a file is transparent or independent unless verified when verification is available.
6. Do not promise a batch size unsupported by the image tool. Generate independent images sequentially if multi-output generation is unavailable. Report limitations and actual output count.

## Workflow
### 1. Plan a manifest
List each requested asset with a unique filename and description (for example, nana-happy.png, nana-surprised.png, button-play.png). Choose sensible aspect ratios and consistent padding.

### 2. Generate isolated images
Use independent image outputs only. Batch generation is permitted only when the available tool explicitly supports multiple independent image results; otherwise generate each asset separately when possible.

For each asset instruct the generator: "Create ONLY [specific asset], one standalone subject on its own canvas. No other assets, grid, collage, contact sheet, sprite sheet, text, or labels. Transparent background if supported. Match reference style and identity."

If only one output per turn is supported, do not claim that all assets can be generated in the same turn.

### 3. Validate
Inspect each image for a single intended subject, consistent style, correct anatomy/orientation, clean edges, adequate padding, true transparency where required, and independent file identity. Regenerate failures if possible. A composite image counts as one failed batch output, not multiple completed assets.

### 4. Name and package
Save each asset as its own file using the manifest filenames. When possible, optionally supply a ZIP containing all independent files. Never crop a combined image and present it as independently generated outputs unless the user explicitly approves that fallback.

### 5. Report accurately
Report requested asset count, actual independent files generated, any failures or remaining items, transparency verification status, and accessible file links. Never report success based on the number of subjects inside a single image.

## Anti-patterns
- A poster of ten buttons called ten separate PNGs.
- A character sheet when independent poses were requested.
- A checkerboard-looking background claimed to be transparent without verification.
- Assuming a generator supports ten independent images without checking.
- Promising background multi-turn generation without an execution tool.

## Success criterion
For N requested assets, success means N independently accessible image files, each containing only its requested asset. If fewer are possible, state the actual count and limitation.

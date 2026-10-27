---
name: adobe-stock-contributor
description: Audit and prepare photos, AI illustrations, textures, and graphic assets for Adobe Stock Contributor submissions. Use when asked to prepare an asset for Adobe Stock, check submission readiness, generate Adobe Stock titles/keywords, or export compliant files.
---

# Adobe Stock Contributor

## Purpose and boundaries
Prepare an existing asset for submission to Adobe Stock. This is a **preflight and export** skill, not an automatic approval guarantee. Work independently of the asset-creation skill (e.g. vintage-illustration-card). Never upload, submit, or publish to a contributor account without explicit user authorization and an available authorized integration.

## Source of truth
Before advising on mutable submission requirements, consult current official Adobe Stock Contributor documentation, especially:
- https://helpx.adobe.com/stock/contributor/submit-your-content.html
- https://helpx.adobe.com/stock/contributor/submit-your-content/submit-generative-ai-content/submit-generative-ai-content.html
- https://helpx.adobe.com/stock/contributor/content-policies-guidelines/metadata/tips-effective-titles-keywords.html
- https://helpx.adobe.com/stock/contributor/submit-your-content/submit-illustrations/technical-legal-requirements-illustration-submission.html
If current rules cannot be checked, label thresholds as provisional and request verification; do not invent policies.

## Inputs
Accept image/file, intended asset type (photo, illustration, vector, texture), AI-generation status, subject/theme, and optional palette/market. Infer only what is visible. If the actual file is inaccessible, do not pretend to inspect or export it.

## Workflow
1. **Inspect the actual asset**: dimensions, pixel count, format, color profile if available, file size, visible defects, anatomy, text legibility, image coherence, compression, edge quality, and unwanted elements. Distinguish confirmed technical checks from subjective visual review.
2. **Compliance**: identify possible trademarks, logos, protected characters, recognizable people/property, watermarks, misleading claims, close copies, or mass-similar submissions. Flag uncertainty and any release needs; never certify rights or ownership without evidence. If generative AI was used, instruct contributor to select the platform's generative-AI disclosure option. Do not imply AI imagery is camera photography.
3. **Technical validation**: for raster illustrations/photos, check current Adobe requirements; typical targets include JPEG, sRGB, at least 4 MP, at most 100 MP and 45 MB, subject to official changes. Count MP from width × height / 1,000,000. Square 1024×1024 is only ~1.05 MP and is NOT compliant with a 4 MP minimum. Aim for clean native high-resolution output where possible; upscaling alone cannot restore missing detail. Never claim an image is 3000×3000 without inspecting/exporting it. For vectors, follow Adobe's separate vector-specific requirements; do not mislabel raster as vector.
4. **Metadata**: write accurate natural-language **English title** preferably under 70 characters, descriptive and distinctive rather than a bare noun. Write an optional concise English description for cataloging (do not imply the upload UI always accepts descriptions). Provide **up to 49 English keywords**, comma-separated, with the most important first (especially the first 10). Use only visually supported attributes, occasion, color, style, and intended uses; no keyword stuffing, unsupported claims, brands, or artist names. A title may include 'Vintage Watercolor Illustration' only when accurate. Avoid words like 'transparent', 'isolated on white', 'vector', 'seamless', or 'print ready' unless actually true.
5. **Prepare export**, if a file-editing tool and original bytes are available: convert/export to appropriate format, preserve appearance and proportions, embed sRGB where supported, choose high-quality JPEG without unnecessary artifacts, inspect output dimensions and size. If upscaling is needed, disclose the operation and recheck quality; do not simply change DPI metadata or relabel file extension. Keep the original intact.
6. **Deliver** actual exported file link only if the file was created and confirmed to exist. Otherwise provide precise steps and a NEEDS ACTION status. Include title, description, keywords, suggested lowercase hyphenated filename, AI disclosure, technical report, issues, and next actions.

## Status labels
- **READY FOR SUBMISSION**: verified accessible export meets checked technical rules, no obvious blocking defects; Adobe review is still required.
- **NEEDS REVISION**: visible or technical issues require correction.
- **UNVERIFIED**: missing original file, policy confirmation, or other evidence prevents readiness determination.
- **NOT SUITABLE**: serious issues cannot be remedied without fundamentally replacing the work.
Do not use READY when file validation or policy checks were not performed.

## Output template
**Adobe Stock Preflight**
- Status: [status + brief reason]
- Asset type: [...]
- Generative AI: [Yes / No / Unknown]; disclosure action: [...]
- Technical: [actual dimensions, MP, format, size, color profile; unknowns explicitly marked]
- Quality & rights flags: [findings, severity, required fixes]
- SEO title: [...]
- Description (optional catalog copy): [...]
- Keywords (ordered, comma-separated; <=49): [...]
- Filename: [descriptive-slug.jpg, only if export format is actually JPEG]
- Export: [verified path/link or not generated]
- Next step: [specific action]

## Example metadata (for a visually matching image)
Title: Golden Christmas Bells with Red Bow Vintage Illustration
Description: Hand-drawn vintage illustration of two golden Christmas bells with a red ribbon and holly on warm textured paper.
Keywords: christmas bells, golden bells, christmas, vintage illustration, red bow, holiday decoration, bells, holly, evergreen, festive, watercolor, hand drawn, christmas ornament, traditional, winter, holiday, textured paper, cream background, greeting card, seasonal
Filename: golden-christmas-bells-red-bow-vintage-illustration.jpg

## Guardrails
- No fabricated file exports, checks, releases, sales forecasts, approval claims, or search-volume data.
- No automatic bulk near-duplicate uploads; prioritize distinct high-quality assets.
- No watermark on the submitted artwork.
- Avoid placing title/keywords in the image itself unless user explicitly requests text as artwork.
- If user requests a new illustration rather than preflight of an existing asset, use the relevant image-creation skill/tool first, then run this preflight.

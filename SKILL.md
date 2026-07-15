---
name: eyewear-ecommerce-image
description: Create guided ecommerce image packages for sunglasses and eyeglasses from product photos, white-background views, SKU information, reference templates, and optional digital human views. Use when the user wants Codex to generate or plan image2 ecommerce detail pages, main images, scene images, close-up model wearing images, detail images, parameter images, size images, or full ecommerce visual packages for eyewear, especially when they mention sunglasses, glasses, optical frames, product three-view images, ecommerce listing images, detail pages, authenticity, or image templates.
---

# Eyewear Ecommerce Image

Use this skill to guide and produce ecommerce image packages for sunglasses and eyeglasses. Act like a production assistant: tell the user what to provide next, explain the impact of missing materials, confirm the generation plan, then prioritize image2 through Codex image generation/editing capabilities to create or plan the assets.

The core request this skill should satisfy is: turn user-provided sunglasses or eyeglasses product images into ecommerce detail pages, main images, scene images, and close-up model wearing images while preserving the real product.

## First Response

Start by identifying the task type:

- Full new product detail package.
- Supplement missing image groups.
- Regenerate selected images.
- Wearing images only.
- Parameter or size images only.

If the user request is vague, default to a full new product detail package.

Then audit inputs and guide the user:

- Minimum: product front, side, and 45-degree/back white-background views.
- Recommended: minimum input plus SKU data, including brand, model, color, materials, lens functions, dimensions, weight, audience, package list, known selling points, and forbidden claims.
- High quality: recommended input plus reference templates, digital human three-view images, brand tone, audience, competitor references, platform preference, and detailed forbidden words.

Give the user one clear next step. Do not overwhelm them with a long questionnaire.

Example:

> Please upload the product front, side, and 45-degree white-background images first. After that I can check whether the material is enough for main images, detail images, and scene images.

## Generation Plan

Before generating, restate the plan:

- Image groups to produce.
- Which groups use real product cutouts/composition.
- Which groups use image generation with product references.
- Which text will be placed on images.
- Which results may need user confirmation because they involve style, model choice, or product-shape risk.

Default package:

1. Main image group.
2. White-background and multi-angle product images.
3. Detail images for frame, lens, nose pad, hinge, temple, logo, and texture.
4. Parameter images.
5. Size images.
6. Selling point images.
7. Scene images.
8. Wearing images.
9. Face-shape fit images.
10. Detail page structure and asset order.

## Execution Rules

Use image2 as the default generation/editing model when the environment exposes model selection. If image2 is not available, use the strongest available Codex image generation/editing capability and state the fallback in the task package or final notes.

Final visual assets must be generated with an image model, not delivered as prompt-only or text-only plans. When the user asks to produce main images, detail-page images, scene images, or wearing images, call the available image generation/editing model directly. If high-resolution ecommerce zoom quality is needed and the environment provides an API-backed 4K or high-resolution image generation/editing interface, use that API path for final renders. If no image model or API generation path is available, state the blocker clearly instead of claiming the image has been generated.

Prioritize Codex image generation/editing tools when available. If a requested image group cannot be reliably produced, output a task package and explain what extra material would improve the result.

Use a mixed product strategy:

- Main, white-background, parameter, size, and detail images: prefer real product cutout/composition from uploaded product views. Preserve original product pixels whenever possible.
- Scene and wearing images: image2 generation may be used for the environment, face, lighting, and composition, but the eyewear must remain faithful to the source product.

Never invent parameter, material, certification, medical, lens-function, or package claims. If SKU data is missing, leave those areas blank, create a layout-only parameter image, or ask the user for the missing values.

For wearing images, prefer user-uploaded digital human three-view images. If absent, generate fictional digital humans matched to the product audience. Default to close-up face, half-face, or head-and-shoulders crops so the eyewear is large enough to show frame shape, lens color, hinge, temple/arm details, and wearing fit. The preferred scene-wearing perspective is a tight face-closeup commercial crop: face fills most of the frame, eyewear is the visual center, camera is near the model at slight front or front-45-degree angle, one temple side and hinge area remain visible, and background is shallow/secondary. Avoid distant full-body wearing images unless the user explicitly asks for outfit or scene emphasis. Avoid celebrities, influencers, brand ambassadors, and identifiable real people unless the user provides rights-cleared material.

Product authenticity is the highest priority. Use the uploaded product image as the source of truth and preserve:

- Frame outer silhouette, thickness, bridge width, lens shape, lens color, lens transparency, lens gradient, coating appearance, and overall proportions.
- Temple/arm shape, temple angle, hinge structure, screws, nose pads, logo position, printed marks, engravings, material finish, and SKU-specific colors.
- The product's perspective unless the user explicitly asks for a different generated angle and understands the shape-risk.

Do not redesign, simplify, beautify, recolor, reshape, stretch, warp, liquify, or hallucinate the eyewear. Do not add logos, certification marks, UV400/Polarized/CE/FDA/TAC claims, packaging, props, badges, or text unless the user provided verified source material for them.

For authenticity-sensitive outputs, prefer background removal, masking, cutout compositing, proportional resizing, controlled shadow, and mild exposure/sharpness correction over full product regeneration. Apply generative fill mainly to background, scene, lighting, and human context. Avoid generative editing over the eyewear body unless the user explicitly asks for repair and accepts risk.

Before accepting generated outputs, compare against the original product image. Reject or regenerate if the frame outline, lens shape/color/gradient/transparency, temple angle, bridge, hinge, nose pads, logo, material, proportions, or perspective changed unintentionally.

## References

Read only the reference files needed for the current task:

- For intake, planning, and step-by-step production flow, read `references/workflow.md`.
- For product fidelity, copy, digital human, copyright, and quality rules, read `references/quality-rules.md`.
- For output folders, filenames, reports, and fallback packaging, read `references/output-package.md`.
- When using or extending the bundled template library, read `references/template-library.md`.

## Template Assets

The public repository does not bundle ecommerce reference images or template screenshots, because those assets may require separate rights clearance.

To use template-driven generation, add your own rights-cleared ecommerce references under `assets/templates/` and describe their layout logic in `references/template-library.md`.

Use template assets only as references for layout logic and ecommerce storytelling. Do not copy exact text, models, brands, logos, watermarks, or unverified claims.

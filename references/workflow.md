# Workflow

Use this flow for sunglasses and eyeglasses ecommerce image production.

## 1. Classify The Request

Classify the task as one of:

- Full new product detail package.
- Supplement missing image groups.
- Regenerate selected images.
- Wearing images only.
- Parameter or size images only.

Default to a full new product detail package if the user asks generally for ecommerce images, product images, detail images, or listing materials.

## 2. Audit Inputs

Check whether the user has provided:

- Product front, side, and 45-degree/back white-background views.
- SKU data: brand, model, color, frame material, lens material, lens function, dimensions, weight, target user, package list, known selling points, forbidden words.
- Reference ecommerce template images.
- Digital human front, side, and 45-degree/back views.
- Brand tone, audience, platform preference, and competitor references.

If required inputs are missing, ask for one next action.

## 3. Explain Missing-Input Impact

Use concrete impact statements:

- Missing product views: cannot start reliable product generation.
- Missing SKU data: cannot generate accurate parameter, size, material, lens function, weight, or package text.
- Missing reference templates: use default eyewear ecommerce style.
- Missing digital human: generate fictional digital human or skip wearing images.
- Missing forbidden words: use default high-risk claim filter.

## 4. Confirm The Plan

Before generating, summarize:

- Image groups to produce.
- Product-fidelity method for each group.
- Text source for each text-heavy group.
- Digital human source.
- Quality checks and likely manual confirmation points.

## 5. Generate In Batches

Generate lower-risk, high-fidelity assets first:

1. Main image group.
2. White-background and multi-angle images.
3. Detail images.
4. Parameter and size images.

Then generate higher-risk creative assets:

1. Scene images.
2. Wearing images.
3. Face-shape fit images.
4. Detail page structure or long image.

## 6. Quality Check And Rework

Automatically rework hard failures when feasible. Mark soft issues for user confirmation.

If a result cannot be made reliable, produce a fallback task package with:

- Failed image group.
- Failure reason.
- Suggested missing material.
- Best next action.

## 7. Archive The Project

Save or propose a complete project package with inputs, working assets, outputs, reports, prompts, copy sources, and reuse notes. See `output-package.md`.

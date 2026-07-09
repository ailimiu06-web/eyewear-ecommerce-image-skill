# Output Package

Each run should produce or plan a self-contained project package.

```text
project-name/
  inputs/
    product_views/
    sku/
    references/
    digital_human/
  working/
    extracted_product/
    prompts/
    copy/
  outputs/
    main_images/
    detail_images/
    scene_images/
    wearing_images/
    parameter_images/
    long_detail_structure/
  reports/
    quality_check.md
    generation_log.md
    copy_source_table.md
    reuse_notes.md
```

## Output Groups

- `main_images/`: one core main image and two to three alternate directions.
- `detail_images/`: frame, lens, nose pad, hinge, temple, logo, texture, and material detail cards.
- `scene_images/`: lifestyle and environment scenes matched to audience and product use.
- `wearing_images/`: digital-human wearing images.
- `parameter_images/`: parameter, size, material, function, and package-list visuals.
- `long_detail_structure/`: detail page order, layout notes, and optionally a long-page image.

## Reports

`quality_check.md` should list each output, status, detected issues, and rework notes.

`generation_log.md` should record prompts, reference images, tools used, and generation attempts.

`copy_source_table.md` should map every parameter or function claim to a provided source.

`reuse_notes.md` should explain what can be reused as a template for future products or color variants.

## Fallback Package

When image generation cannot be completed reliably, return a package with:

- Planned image group.
- Prompt or task instructions.
- Required missing inputs.
- Failure reason.
- Suggested next action.

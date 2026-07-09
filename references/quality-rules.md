# Quality Rules

## Product Fidelity

Product fidelity is the highest priority. Preserve:

- Frame silhouette.
- Lens color and opacity.
- Temple shape.
- Nose pad structure.
- Hinges.
- Logo placement.
- Texture and pattern.
- Overall material impression.

Reject or rework results where:

- The product becomes another eyewear style.
- Lens color changes.
- Frame or temple structure changes.
- Nose pad, hinge, logo, texture, or pattern disappears incorrectly.
- New logos, marks, or decorations appear.
- Product scale is obviously wrong in a scene.

## Text And Claims

Parameter text must come from user-provided SKU data or product documents. Do not invent:

- Dimensions.
- Weight.
- Materials.
- Lens functions.
- Certifications.
- Medical effects.
- Package contents.

AI may write marketing copy only when it is grounded in visible product traits or provided SKU data.

Default forbidden or confirmation-required claims:

- "100% UV protection".
- "Medical grade".
- "Treatment".
- "Cures".
- "Official certification".
- "Celebrity same style".
- "Guaranteed eye protection".

If text rendering is unreliable, output a clean image plus a separate copy/layout note instead of delivering unreadable text.

## Digital Human Rules

Use digital human sources in this order:

1. User-provided digital human three-view images.
2. Fictional AI digital humans matched to product audience and scene.
3. Skip wearing images if the user prefers no model generation.

Avoid celebrities, influencers, brand ambassadors, and identifiable real people unless the user provides rights-cleared material and explicitly asks to use it.

Default wearing-image composition:

- Use close-up face, half-face, or head-and-shoulders crops as the default.
- Make the eyewear large enough to inspect frame shape, lens color, hinge, temple/arm details, and facial fit.
- Prefer slight front or front-45-degree face angles when they reveal both the frame front and temple/arm connection.
- Avoid distant full-body portraits, heavy hair occlusion, strong motion blur, or props that hide the frame, lenses, hinge, or temples unless the user explicitly prioritizes outfit/scene mood.

Record digital human source as:

- User provided.
- AI fictional.
- Not used.

## Hard Failures

Automatically rework when possible:

- Product deformation.
- Lens color mismatch.
- Frame or temple mismatch.
- Missing required detail.
- Text garbling.
- SKU mismatch.
- Unsupported function claim.
- Abnormal digital human anatomy.
- Incorrect wearing position.
- Wearing image too distant to inspect frame, lens, hinge, temple/arm details, or facial fit.
- Product/scene scale mismatch.

## Soft Review Items

Ask the user to judge:

- Visual style.
- Scene fit.
- Digital human temperament.
- Detail page order.
- Commercial strength of alternate main images.

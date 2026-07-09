# Eyewear Ecommerce Image Skill

Codex skill for creating guided ecommerce image packages for sunglasses and eyeglasses.

It helps an agent plan and produce:

- Ecommerce detail pages
- Main product images
- Scene images
- Close-up model wearing images
- Detail, parameter, and size images

The skill prioritizes product authenticity. Uploaded product photos are treated as the source of truth, and generated outputs should preserve frame shape, lens shape, color, transparency, gradient, hinges, temples, logo placement, material finish, proportions, and perspective.

## Usage

Install this folder as a Codex skill, then ask Codex to use `eyewear-ecommerce-image` with your eyewear product photos.

Recommended inputs:

- Product front, side, and 45-degree/back white-background views
- SKU data such as model, color, material, dimensions, lens function, and package list
- Rights-cleared digital human references or permission to generate fictional digital humans
- Rights-cleared ecommerce layout references, if you want template-driven pages

## Template Assets

This public repository does not include ecommerce template screenshots or product reference images. Add your own rights-cleared assets under `assets/templates/` when needed.

## License

MIT

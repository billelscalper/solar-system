# AGENTS.md

## Project Structure

- `solar-system.html` — Standalone Three.js solar system (uses CDN imports, no build needed)
- `PROJECT 1/` — Static "FitFuel" e-commerce site (HTML + vanilla JS + CSS)
- `PROJECT 1/generate.js` — Node script to regenerate SVG product/category images

## Key Commands

```bash
# Regenerate SVG assets (requires Node.js)
node "PROJECT 1/generate.js"
# Output: assets/img/products/*.svg, assets/img/categories/*.svg, assets/img/hero.svg

# Serve locally for testing
npx serve .
```

## Conventions

- `generate.js` uses CommonJS (`require`), not ES modules
- Product data lives in `PROJECT 1/assets/js/data/products.js`, `categories.js`, `brands.js`
- SVGs are generated with 3 variants per product (normal, rotated left, rotated right)
- No build pipeline, linter, or test framework — this is a pure static site
- No git repository initialized

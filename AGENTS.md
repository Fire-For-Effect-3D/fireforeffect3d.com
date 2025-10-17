# FireForEffect3D.com – Agent Guide

Welcome! This repository contains a marketing site built with [Astro](https://astro.build). The goal of this guide is to help other AI agents contribute consistently.

## Project layout
- `src/pages/` — top-level Astro pages. Each page should export frontmatter data (arrays, config objects) above the component markup.
- `src/layouts/` — shared page chrome. `Layout.astro` defines the HTML shell, global fonts, and CSS variables.
- `src/components/` — reusable Astro components. Favor colocating component-specific styles with the component.
- `src/styles/` — global stylesheets. Only put shared tokens or resets here; page-specific styling belongs in the page/component file.
- `public/` — static assets served as-is. Do **not** import from `src`.

Never modify anything in `node_modules/` or generated outputs like `dist/`.

## Development workflow
1. Run `npm install` once to install dependencies.
2. Use `npm run dev` for local development (defaults to `http://localhost:4321`).
3. Use `npm run build` before committing major changes to ensure production builds succeed.

## Coding guidelines
- Stay within Astro/TypeScript conventions. Use Astro components (`.astro`) unless a script-only module is required.
- Keep markup semantic and accessible (proper headings, `aria-` attributes, alt text, keyboard-focus styles).
- Prefer CSS custom properties already defined in `Layout.astro`. Add new variables there if new design tokens are required.
- Keep inline `<style>` blocks scoped when possible. Use `:global` selectors only for shared resets.
- When adding JavaScript, prefer lightweight Astro/Vanilla JS solutions. Avoid large client-side frameworks unless justified.
- Place configuration/seeding data (arrays like `services`, `gallery`, etc.) at the top of the Astro file inside the frontmatter block.

## Assets & media
- Add new static images or downloads to `public/`. Use descriptive file names and update alt text accordingly.
- Optimize image dimensions and formats (prefer `.webp` or `.avif` when possible).

## Testing & validation
- Run `npm run build` to validate Astro builds when changes may affect build output.
- If Tailwind or PostCSS configs are adjusted, ensure `npm run dev` still launches without warnings.

## Writing & content updates
- Maintain the veteran-owned, mission-ready voice already present in the content.
- Double-check contact information and download links when editing CTAs.

Thanks for contributing!

# AGENTS.md

## Project overview

Single-file static portfolio site (`index.html`). No build system, no package manager, no tests, no linting, no CI.

## Structure

- `index.html` — entire site: nav, hero, about, research, projects, leadership, footer. All styles are inline (`<style>` block + Tailwind).
- `photo.png` / `photo.jpg` — profile photos referenced in the hero section.

## Key facts

- Tailwind CSS is loaded via CDN (`cdn.tailwindcss.com`). There is no `tailwind.config.js` on disk — the config is defined inline in the `<script>` tag at `index.html:8-41`.
- Fonts (Inter, Space Grotesk) are loaded from Google Fonts.
- Custom CSS keyframes and animations are defined in the inline `<style>` block.
- Scroll-reveal is handled by a small `IntersectionObserver` script at the bottom of the file (`index.html:446-449`).

## Conventions

- All edits go directly into `index.html`. There are no partials, templates, or components.
- Color palette and design tokens are defined in the Tailwind config object inline — update them there, not in a separate config file.
- Card status pills use classes `pill-published`, `pill-progress`, `pill-ready` (defined in the `<style>` block).

## No dev commands

There are no build, lint, or test commands. Preview by opening `index.html` in a browser.

<!--
Guidance for AI coding assistants working on this repository.
Keep this file short and focused: what an automated assistant needs to know to be productive.
-->

# Copilot instructions — jostin (Astro portfolio)

Repository overview:
- This is a small single-page Astro site (framework: Astro v5).
- Key source files live under `src/`:
  - `src/pages/index.astro` — main page content and inline styles.
  - `src/layouts/Layout.astro` — base HTML layout (`<slot/>`).
  - `src/components/Welcome.astro` — starter component that imports images from `src/assets/`.
- Config and scripts:
  - `package.json` defines npm scripts: `dev` (astro dev), `build` (astro build), `preview` (astro preview).
  - `astro.config.mjs` uses default config.

What to change and how:
- Small content/style changes: edit `src/pages/index.astro` or component files. The project uses plain HTML/CSS inside Astro files; prefer non-disruptive edits (preserve inline styles unless migrating to a stylesheet).
- Adding images/assets: place files in `src/assets/` and import them using relative paths (see `Welcome.astro` usage: `import astroLogo from '../assets/astro.svg'`).
- Routes: pages under `src/pages/` map directly to site routes (standard Astro behavior).

Developer workflow (commands):
- Install deps: `npm install` (run from repo root).
- Local dev server: `npm run dev` — serves at http://localhost:4321 by default.
- Build: `npm run build` — produces `dist/` for deployment.
- Preview a build locally: `npm run preview`.

Project-specific conventions & patterns:
- Single-page portfolio structure: index contains profile, skills and contact sections; follow the existing simple semantic HTML structure and CSS variables (no CSS frameworks used).
- Assets are used via ES imports inside .astro files (use `.src` when necessary for `<img src={...} />`).
- Keep commits focused: small content, styling or asset changes are expected. Avoid large refactors unless requested.

Integration points & external deps:
- Only dependency is `astro` (see `package.json`). No backend or API integrations exist in the repo.

Testing, linting, and CI:
- No tests or linters configured. Keep changes minimal and validate by running the dev server locally.

Examples to reference:
- Update profile text: edit `src/pages/index.astro` (look for the Spanish content under the `Sobre mí` section).
- Add a new component: create `src/components/MyComponent.astro` and import it into `src/pages/index.astro`.

When in doubt:
- Run the dev server and open the site — visual verification is the primary validation method for changes.
- If you need to add new tooling (lint/test), propose it in a small PR and include setup commands.

Contact for clarifications:
- The repository README (`README.md`) contains the original starter notes — prefer asking the maintainer before making structural changes.

-- End of instructions --

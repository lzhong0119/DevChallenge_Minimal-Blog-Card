## Goal
Help contributors and AI agents make safe, minimal, and high-value changes to this static "Minimal Blog Card" starter.

Keep edits small and reversible: this repo is a single-page HTML/CSS starter for a devChallenges.io exercise (no build system).

## Quick repo snapshot
- Single-page static site: `index.html` controls markup and contains a small inline style block.
- Assets live in `resources/` and designs (reference images) are in `design/`.
- `README-template.md` and `README.md` contain challenge instructions and deployment guidance.

## What an AI agent should know first
- There is no JS app, package manager, or build step. Do not add heavy tooling without explicit human approval.
- Common developer workflow: open `index.html` in a browser or run a tiny static server (e.g. `python -m http.server`) for testing.
- Primary edits will be HTML/CSS and image optimization under `resources/`.

## Recommended edits the agent may propose and how to implement them
- Move inline styles into a new `styles.css` and link it from `index.html` (edit `<head>`). Example: add `<link rel="stylesheet" href="styles.css">` and copy the existing `<style>` content into `styles.css`.
- If optimizing images, write optimized files back to `resources/` and keep original filenames where possible or update references in HTML.
- If adding files, update `README.md` or `README-template.md` to mention them.

## Patterns & conventions in this repo (examples)
- Minimal markup: `index.html` contains a top-level `.author-info` element you can reference when making CSS changes.
- Favicon path: `resources/favicon.ico` — update or preserve this path when changing assets.
- README-driven: `README.md` is the canonical challenge description—do not delete; update only to reflect real changes.

## Disallowed/ask-first actions
- Do not introduce package.json, node_modules, or other language-specific build tools without explicit permission.
- Do not modify `README-template.md` in a way that removes instructions for challenge submission.
- If a change touches deployment (GitHub Pages/Vercel/Netlify) or CI, ask a human for approval first.

## Editing guidance for patches/PRs
- Keep PRs focused and small (one concern per PR). Example PR titles: "Move inline styles to styles.css" or "Optimize hero image in resources/".
- Provide a short description of the change and any manual testing steps (e.g., "Open index.html in browser; verify layout matches design at 375px/768px/1440px").

## Useful file references
- `index.html` — main markup and small inline styles (start here for layout changes).
- `resources/` — images and favicon used by the page.
- `design/` — reference images for styling and spacing decisions.
- `README-template.md` / `README.md` — challenge instructions and deployment notes.

## When in doubt
- Ask a human reviewer before making structural changes (introducing tooling, CI, or complex refactors).
- If you propose a behavior change, include exact steps to reproduce and a rollback plan.

---
If you'd like I can tailor this to follow a stricter commit message convention, or include concrete code snippets for moving inline CSS into `styles.css`.

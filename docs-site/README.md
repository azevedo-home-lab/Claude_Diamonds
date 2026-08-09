# docs-site

The Claude fundamentals learning site, published via GitHub Pages.
Sibling to the two-diamond method in the repo's root `README.md`, not
part of it — see `docs/specs/2026-08-09-1-claude-fundamentals-learning-site.md`
for what this is and how to tell it's done.

## Status

`loops.html` — turns, the agentic loop, and loop patterns. Fully built,
sourced from three Anthropic pages, cited on the page itself.

`subagents.html` — a subagent's fresh context window, what it inherits
at spawn, and what returns to its parent. Fully built, sourced from
Anthropic's `sub-agents` documentation, cited on the page itself.

`context.html`, `hooks.html` — placeholders, reserving the URL and
shared shell for future lessons.

## Serving this

`Settings → Pages → Source: GitHub Actions`. `.github/workflows/pages.yml`
deploys `docs-site/` on every push to `main` that touches this directory.

## Shared shell

`styles.css` holds the token system (light/dark via
`prefers-color-scheme`) and the header/nav every page repeats. There is
no templating engine — adding a page means copying the header markup
from an existing page and linking `styles.css`, the same approach
`claude-code-workflows`' own `docs-site/` uses.

## Diagrams

Every diagram is hand-authored inline SVG using `currentColor`, so it
renders correctly in both color schemes with no external dependency.

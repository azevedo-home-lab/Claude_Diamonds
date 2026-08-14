# docs-site

The Claude fundamentals learning site plus the method's visual page,
published via GitHub Pages. An official resident of this repo (spec 9,
D9-1) — see `docs/specs/2026-08-09-1-claude-fundamentals-learning-site.md`
for the original scope.

## Status

All four lessons are fully built, each sourced from Anthropic's own
documentation and cited on the page itself: `loops.html` (turns, the
agentic loop, loop patterns), `context.html` (context window and
compaction), `hooks.html` (hooks in the loop), and `subagents.html`
(subagent context). `method.html` is the visual version of the repo
README's method. The hub (`index.html`) lists the method section first,
then the fundamentals lessons.

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

Lesson diagrams are hand-authored inline SVG using `currentColor`, so
they render correctly in both color schemes with no external dependency.
The two-diamond diagram is the exception: its canonical source is
`assets/diamonds.svg` (self-contained, light/dark via
`prefers-color-scheme`), included by both `method.html` and the repo
README — one file, edited once (spec 9, D9-7).

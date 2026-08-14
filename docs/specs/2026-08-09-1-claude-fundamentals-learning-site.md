# Claude fundamentals learning site

## TLDR

Claude Diamonds gains a published, browsable site. It teaches three
ideas Anthropic documents but this repo never explains. Those are what a
turn is, what the agentic loop does, and how loop patterns like `/goal`
and `/loop` differ. The site has a landing page linking to every lesson, one
lesson built in full, and three stub pages reserving future lessons. The
two-diamond method page gains one link to it and is otherwise unchanged.

## Metadata

- **Issue:** #1
- **Date:** 2026-08-09
- **Status:** Done — shipped in PR #3 (2026-08-09); status closed
  retroactively per spec 9 (D9-4)

## Context

Claude Diamonds cites Anthropic's agent-loop and loop-engineering
documentation in its own README but does not teach the ideas those pages
cover. A reader who cannot already tell a turn, the agentic loop, and a
loop pattern apart has nowhere in this repo to learn the difference.
That gap surfaced directly: a question about `/goal` caused confusion
between community conventions and Anthropic-documented behavior. Only
reading the source pages in full resolved it. This repo is the right
home, since it already explains how to work with Claude, not only what
to build with it.

## Goal

A visitor to the published site can read one complete, accurate lesson
on turns, the agentic loop, and loop patterns. The lesson is sourced
entirely from Anthropic's own documentation. The same visitor can see,
from a single landing page, what other lessons exist or are planned.

## User stories

### P1 — Learn the loop concepts

As a reader new to Claude Code's execution model, I want one page
explaining a turn, the agentic loop, and loop patterns in plain
language. I want it so I stop conflating them.

- **Given** the published site, **when** I open the loops lesson, **then**
  I can state in my own words what a turn is, distinct from the agentic
  loop and from a loop pattern like `/goal` or `/loop`.
- **Given** the loops lesson, **when** I look for where a claim about
  Claude's behavior came from, **then** I find a named source — one of
  Anthropic's `how-claude-code-works`, `agent-sdk/agent-loop`, or
  `getting-started-with-loops` pages — cited by name and linked.
- **Given** the loops lesson, **when** I read about `/goal`, **then** the
  page states it as an Anthropic-documented loop pattern with a
  worked example, not as a community-only convention.

### P2 — Find my way around the site

As a visitor landing on the site for the first time, I want to see what
lessons exist and what is still to come. I want it so I know whether to
keep reading now or come back later.

- **Given** the site's landing page, **when** I look at it, **then** I see
  a link to the loops lesson and a link to each planned-but-not-yet-written
  lesson, each visually distinguishable as built or not-yet-built.
- **Given** any page on the site, **when** I look for the two-diamond
  method, **then** I find exactly one link to it, and following that link
  takes me to the unchanged README content on GitHub.
- **Given** any lesson or stub page, **when** the browser's OS-level
  appearance is set to dark, **then** the page renders in a dark palette
  with all text readable against its background; the same is true set to
  light.

## Success criteria

- The loops lesson names and links all three Anthropic source pages
  (`how-claude-code-works`, `agent-sdk/agent-loop`,
  `getting-started-with-loops`) by their titles and URLs.
- The loops lesson states these correctly, matching the three pages as
  they read on 2026-08-09:
  - the definition of a turn
  - the three-phase conceptual loop
  - the five-step mechanical loop, with at least one worked multi-turn
    example
  - the `max_turns` / `max_budget_usd` caps
  - the four named loop patterns (turn-based, goal-based, time-based,
    proactive)
- The loops lesson states explicitly that `/goal` is one of Anthropic's
  four documented loop patterns, not a community-only convention.
- The landing page contains a working link to the loops lesson and to
  each stub page.
- Exactly one link from the published site's pages resolves to the
  existing `README.md` on GitHub. `README.md`'s two-diamond method
  content is byte-for-byte unchanged except for that one added link.
- Every page on the site loads without a broken image, broken internal
  link, or console error, checked by opening each page in a browser.
- Every page renders correctly — readable text, no clipped content — with
  the OS appearance set to both light and dark.
- The site is reachable at a live GitHub Pages URL after the change
  merges to `main`.

## Scope: in

- A landing page linking to every lesson, built or planned.
- One fully written lesson on turns, the agentic loop, and loop
  patterns.
- Three additional pages, linked from the landing page, that do not yet
  carry lesson content. Each names what it will eventually cover.
- Exactly one link added to the existing `README.md`.
- The site being live and browsable at a GitHub Pages URL.

## Scope: out

- Any change to the two-diamond method content already in `README.md`.
- Full lesson content for any topic beyond turns, the agentic loop, and
  loop patterns — other lessons stay as placeholders in this issue.
- Any interactive or dynamic behavior on the site (search, comments,
  live data) — every page is static.
- Sourcing lesson content from anything other than Anthropic's own
  published documentation.

## Assumptions

- GitHub Pages is available and can be enabled for this repository. If
  it is not already enabled, enabling it is a one-time step the
  implementer cannot complete from an API and must ask for.
- The three named Anthropic pages remain reachable at their current
  URLs through implementation. If a cited page moves or changes before
  this ships, the affected claim is re-verified against the new
  content. It is never left pointing at stale text.

## Open questions

None — the human resolved the two live threads (visual treatment,
site/repo scope) before this spec was drafted.

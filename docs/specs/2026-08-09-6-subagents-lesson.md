# Subagents lesson

## TLDR

`subagents.html` moves from a one-paragraph stub to a full lesson,
matching the depth `loops.html` already set for this site. It covers
three things: the fresh context window a subagent starts with, what it
inherits at spawn, and what returns to its parent. Every claim traces to
Anthropic's own subagents documentation. The hub's card
for this lesson flips from "Not built yet" to "Built" and links straight
to the finished page.

## Metadata

- **Issue:** #6
- **Date:** 2026-08-09
- **Status:** Done — shipped in PR #11 (2026-08-09); status closed
  retroactively per spec 9 (D9-4)

## Context

`docs-site/subagents.html` exists today only as a stub reserving the URL
and the shared page shell. It links out to Anthropic's own documentation
but teaches nothing itself. The hub page already advertises this lesson
as planned, so any visitor sees the gap. `loops.html` already set the bar
for this site: a complete lesson where every factual claim traces to a
named, linked Anthropic source page.

## Goal

A visitor to the published site can read one complete, accurate lesson on
subagents. It covers the fresh context window, what spawning inherits,
and what returns to the parent when the subagent finishes. The lesson is
sourced entirely from Anthropic's own documentation, matching the
citation depth `loops.html` already set.

## User stories

### P1 — Learn how a subagent's context works

As a reader who already knows turns and the agentic loop, I want one page
on how a subagent's context differs from its parent's. I want it so I
can reason about when delegating actually keeps my main conversation
lean, instead of guessing.

- **Given** the subagents lesson, **when** I read about how a subagent
  starts, **then** the page states it begins with a fresh context window,
  separate from its parent's conversation history.
- **Given** the subagents lesson, **when** I read about what a subagent
  has available the moment it spawns, **then** the page states it
  receives its own system prompt and project-level context such as
  `CLAUDE.md`.
- **Given** the subagents lesson, **when** I read about what happens after
  a subagent finishes, **then** the page states only its final response
  returns to the parent, not its full transcript, and explains why that
  keeps the parent's context lean.
- **Given** the subagents lesson, **when** I look for where a claim about
  subagent behavior came from, **then** I find a named Anthropic source
  page, cited by name and linked, matching how `loops.html` cites its
  sources.

### P2 — Find the finished lesson from the hub

As a visitor on the learning hub, I want to see the subagents lesson is
built and go straight to it. I want it the same way I already can for
the loops lesson.

- **Given** the hub page, **when** I look at the subagents card,
  **then** it reads "Built" instead of "Not built yet" and links to
  `subagents.html`.
- **Given** any page on the site, **when** the browser's OS-level
  appearance is set to dark, **then** the subagents page renders in a
  dark palette with all text readable against its background; the same
  is true set to light.

## Success criteria

- The subagents lesson states these three claims, verified against
  Anthropic's `sub-agents` page at merge time:
  - a subagent starts with a fresh, isolated context window that does not
    see the parent conversation's history
  - what a non-fork subagent's initial context contains: its own system
    prompt, the delegation task message, and the `CLAUDE.md` hierarchy the
    parent conversation loads
  - that when a subagent finishes, only its final response reaches the
    parent, not its full transcript. This is what keeps the parent's
    context window from filling with the subagent's intermediate work
- Every factual claim names and links its specific Anthropic source page,
  in visible page text next to the claim. This matches how a reader can
  already see `loops.html` cite its own sources.
- The hub's subagents card (`docs-site/index.html`) shows status "Built"
  and its link resolves to `subagents.html`.
- The subagents page keeps the shared `docs-site/` shell: same
  `site-header` with nav, `aria-current="page"` set on the Subagents nav
  link, and `styles.css` linked unchanged.
- The subagents page loads without a broken image, broken internal link,
  or console error, checked by opening it in a browser.
- The subagents page renders correctly — readable text, no clipped
  content — with the OS appearance set to both light and dark.

## Scope: in

- Rewriting `docs-site/subagents.html` from stub to full lesson.
- Updating the subagents card's status and link on `docs-site/index.html`.

## Scope: out

- Any change to `loops.html`, `context.html`, or `hooks.html`.
- Any change to the two-diamond method content in `README.md`.
- Full lesson content for context/compaction or hooks — those stay
  stub pages, tracked by their own issues.

## Assumptions

- The Anthropic `sub-agents` documentation page remains reachable at its
  current URL through implementation. Its wording may change for one of
  the three Success criteria claims before this ships. If so, that claim
  is re-read and the page updated to match, before merge.

## Open questions

None.

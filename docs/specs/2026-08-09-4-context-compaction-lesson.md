# Context and compaction lesson

## TLDR

`context.html` moves from a placeholder stub to a full lesson, matching
`loops.html`'s depth and sourcing standard. It explains what fills
Claude's context window, what automatic compaction does when that
window fills up, and two ways to steer what compaction keeps. Every
factual claim traces to a named Anthropic source page. The hub page's
card for this lesson moves from "Not built yet" to "Built" and links to
the finished page.

## Metadata

- **Issue:** #4
- **Date:** 2026-08-09
- **Status:** Done — shipped in PR #10 (2026-08-09); status closed
  retroactively per spec 9 (D9-4)

## Context

`docs-site/context.html` exists today only as a stub reserving the URL
and shared page shell. It links out to Anthropic's own agent-loop
documentation but teaches nothing itself. The hub page already
advertises this lesson as planned ("Not built yet"), so the gap is
visible to any visitor. `loops.html`, the one lesson already built, set
a standard: numbered sections, a legend of the page's key terms, SVG
figures only where they clarify a real relationship, sourced tables,
and a footer naming every source. This lesson follows that same
standard for a different topic.

## Goal

A visitor to the published site can read one complete, accurate lesson
on the context window and compaction. The lesson is sourced entirely
from Anthropic's own documentation, and the hub page correctly shows it
as built.

## User stories

### P1 — Learn what fills the context window and what compaction does

As a reader who has used Claude Code but never looked at what's inside
its context window, I want a page explaining what accumulates there,
what triggers automatic compaction, and what compaction keeps versus
discards. I want it so I understand why instructions from early in a
long session sometimes seem to get lost.

- **Given** the context lesson, **when** I read it, **then** I can name
  the four things that fill the context window: system prompt,
  CLAUDE.md, tool definitions, and conversation history.
- **Given** the context lesson, **when** I read the compaction section,
  **then** I can state what triggers compaction (the window approaching
  its limit) and what compaction does (clears older tool outputs first,
  then summarizes remaining older history, keeping recent exchanges and
  key decisions intact).
- **Given** the context lesson, **when** I look for where a claim about
  Claude's behavior came from, **then** I find a named source — one of
  Anthropic's `agent-sdk/agent-loop`, `how-claude-code-works`, or
  `features-overview` pages — cited by name and linked.

### P2 — Learn how to steer what compaction keeps

As a reader who has lost an early instruction to compaction, I want to
know at least one concrete way to prevent that. I want it so my next
long session doesn't repeat the problem.

- **Given** the context lesson, **when** I read the steering section,
  **then** I find at least one named, concrete technique: adding
  summarization instructions to CLAUDE.md, or running `/compact` with a
  focus argument.
- **Given** the context lesson, **when** the browser's OS-level
  appearance is set to dark, **then** the page renders in a dark
  palette with all text readable against its background; the same is
  true set to light.

### P3 — Find the lesson from the hub

As a visitor on the learning hub, I want the context lesson's card to
show it is built, so I don't skip a finished page thinking it's still a
stub.

- **Given** the hub page, **when** I look at the context lesson's card,
  **then** it reads "Built" (not "Not built yet") and its "lessons
  built" / "lessons planned" counts are updated to match.

## Success criteria

- `context.html` names and links these three Anthropic source pages by
  title and URL: "How the agent loop works"
  (`code.claude.com/docs/en/agent-sdk/agent-loop`), "How Claude Code
  works" (`code.claude.com/docs/en/how-claude-code-works`), and "Extend
  Claude Code" (`code.claude.com/docs/en/features-overview`).
- `context.html` states these correctly, matching the three pages as
  they read on 2026-08-09:
  - the four sources that fill the context window (system prompt,
    CLAUDE.md, tool definitions, conversation history), plus skill
    descriptions as a fifth
  - automatic compaction's trigger and its two-step mechanism (clear
    older tool outputs, then summarize)
  - at least one concrete steering technique (CLAUDE.md summarization
    instructions, or `/compact` with a focus)
  - the per-feature context-cost table (CLAUDE.md, Skills, MCP servers,
    Code intelligence, Subagents, Hooks)
- `context.html` keeps the shared `docs-site/` shell: same header, nav,
  and `styles.css`, with `aria-current="page"` set on the Context nav
  link (and removed from the Learning hub link, where the stub
  currently omits it entirely).
- `index.html`'s card for this lesson changes from "Not built yet" to
  "Built" and links straight to `context.html`. The hub's "lessons
  built" / "lessons planned" counts update from 1/3 to 2/2.
- The page loads without a broken image, broken internal link, or
  console error, checked by opening it in a browser.
- The page renders correctly — readable text, no clipped content — with
  the OS appearance set to both light and dark.

## Scope: in

- Rewriting `docs-site/context.html` from stub to full lesson.
- Updating its hub card and lesson-count meta on `docs-site/index.html`.

## Scope: out

- Any change to `loops.html`, `hooks.html`, or `subagents.html`.
- Any change to the two-diamond method content in `README.md`.
- Any interactive or dynamic behavior on the page — it stays static,
  matching every other page on the site.
- Sourcing lesson content from anything other than Anthropic's own
  published documentation.

## Assumptions

- The three named Anthropic pages remain reachable at their current
  URLs through implementation. If a cited page moves or changes before
  this ships, the affected claim is re-verified against the new
  content. It is never left pointing at stale text.
- `styles.css`'s existing tag classes (`tag-turn`, `tag-loop`,
  `tag-pattern`) are reused for this page's own three-term legend
  (context window / compaction / steering) rather than adding new CSS
  classes, since the existing three-color set is unused elsewhere on
  this page and carries no semantic meaning tied to loops.html
  specifically.

## Open questions

None — the design (section breakdown, legend reuse, and which sections
get an SVG figure) was resolved with the human before this spec was
drafted.

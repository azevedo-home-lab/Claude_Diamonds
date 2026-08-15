# Spec 11 — README reframed around two concerns; index carve-out; templates explained

Status: DECIDED 2026-08-15 (the Owner, portfolio front-diamond session) —
executed same session.

Process note, on the record: CLAUDE.md requires method changes to be
executed in a later loop, never in the same conversation they were
proposed. The Owner ran this as proposal → decision rounds (v1, v2) →
execution in the same session; reservation recorded here per the
challenge protocol; executed without relitigating.

## Origin

The repo's focus widened. It is no longer only the method for running
product work with Claude Desktop and producing product artifacts (in
connection to WFM) — it is also Product Topics: lessons that let any
product person learn the product-job theory and how it applies to WFM.
Two concerns: (1) the required learnings, (2) the actual product work
and its artifacts. The README must be simple, organized with links,
topmost link to the learning hub, plus the sources; index.html must
reflect the same split.

Corrected taxonomy (Owner, v2): the **learning hub** is the learnings
only — Product Methodologies (Eriksson · Torres · Cutler) and Claude
Aspects (loops · context · hooks · subagents). **The method** — Two
diamonds, one gate · How to run it · The repo contract — is its own
concern, not a learning-hub track.

## Decisions

- **D11-1 — Two-job framing.** README opens with the two concerns:
  learn the product job / run the product job. DECIDED: yes.
- **D11-2 — Lesson links in README.** Each built lesson listed under its
  track; the two-edit cost per new lesson accepted; index.html is
  canonical for what's built. DECIDED: accept cost.
- **D11-3 — Index dek reuse.** index.html's dek (and meta description)
  replaced verbatim by the README's two-concern text; README canonical —
  changing it implies re-syncing the dek. Prior dek retired.
  DECIDED: yes.
- **D11-4 — Sources.** One consolidated Sources section at README end,
  one line per foundation; originals canonical. DECIDED: yes — with
  Claude mechanics expanded to sub-bullets, one per Anthropic doc the
  aspect lessons cite (Owner, v3 round).
- **D11-5 — Index sections.** Three sections: The method (the three
  carved-out method cards) first, then Product Methodologies (3 lesson
  cards), then Claude Aspects (4 lesson cards). DECIDED: method first,
  learning hub later.
- **D11-6 — Top nav.** Fifth item "The method" → index.html#the-method,
  identical on all 9 pages, mirroring the section order (Learning hub |
  The method | Product Methodologies | Claude Aspects | GitHub ↗).
  DECIDED: yes.
- **D11-7 — Index doc-meta counts.** DECIDED: removed entirely.
- **D11-8 — Templates explanation.** README's method section gains an
  "Install it" paragraph — docs/templates/ holds the two canonical
  paste blocks that bind a Desktop project (front diamond) and a
  product repo's CLAUDE.md (development) to the method; snapshots are
  re-pasted on change, the repo file wins on drift. The repo-map line
  states the same. DECIDED: yes.

## Drift rules this spec adds

- README is canonical for the two-concern framing text; index.html's
  dek quotes it verbatim and is re-synced when it changes (same ritual
  as template re-paste).
- index.html remains canonical for lesson status ("what's built"); the
  README's lesson lists follow it, at the accepted two-edit cost.

## Executed changes

README.md rewritten (two-job intro; learning hub topmost with both
tracks' lessons; the method in three views + Install it; repo map with
the templates role stated; consolidated Sources with Claude-mechanics
sub-bullets). docs-site/index.html restructured per D11-3/5/6/7; the
"Looking for the product method instead…" closing caption retired. The
five-item nav applied to all nine pages.

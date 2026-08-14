# Spec 9 — Bloat and drift corrections (sequential repo review)

Status: DECIDED 2026-08-14 (Pedro, portfolio front-diamond session) —
executed same day, same session, PR #24.

Process note, on the record: CLAUDE.md requires method changes to be
"executed in a later loop, never in the same conversation they were
proposed." Pedro explicitly overrode that rule for this spec ("write
decision log, then execute"). Reservation recorded here per the
challenge protocol; executed without relitigating.

## Origin

A sequential review of the repo at `main` (c974660, post spec-8
correction loop) found seven bloat/drift items. Each was put to Pedro
individually; his decisions follow. This spec is the decision record —
the method repo's equivalent of a product decision log.

## Decisions

### D9-1 — docs-site stays; drift reduced by single-sourcing (DECIDED)

Finding: docs-site is ~40% of the repo while CLAUDE.md and the README
declare the repo "method only."

Decision: keep the site in this repo — it is already versioned here and
a separate repo solves nothing. CLAUDE.md's boundary statement is
corrected to name docs-site (and docs/canvas-snapshot.md) as residents.
Direction: images and text should be generated/referenced from a single
source rather than hand-crafted per surface, to reduce drift. Noted:
the site's page text is sometimes simpler and more explanatory than the
repo's .md docs — that explanatory register is a feature, not drift.

### D9-2 — WFM4.0 migration to /product: deferred (DECIDED, deferred)

Finding: WFM4.0's per-product material (decision log, research, 8.8 MB
of sources) still lives in the portfolio GDrive folder — the layout the
repo contract retired on 2026-08-14.

Decision: migrate later, in a dedicated session. Until then the debt is
known and recorded here; the contract text is not weakened to
accommodate it.

### D9-3 — docs-site stale labels fixed; Method section added (DECIDED)

Finding: docs-site/README.md called context.html and hooks.html
"placeholders" though both are built; index.html said "2 lessons built /
2 planned" above four cards all marked Built.

Decision: fix both. Additionally, the learning hub gains a new section
at the top with cards for the method page and the three foundation
docs (Eriksson, Torres, Cutler).

### D9-4 — shipped specs are closed; close-on-merge rule (DECIDED)

Finding: specs 1, 4, 6 still read "Status: Draft" and spec 8
"PROPOSED" though all shipped and merged.

Decision: close all four with the merging PR named. New rule in
CLAUDE.md: the PR that ships a spec updates that spec's status in the
same PR.

### D9-5 — method summaries: human .md is canonical (DECIDED)

Finding: the three foundations were summarized in five places (README
blurbs, docs/methods/README.md, human .md, .claude.md, site method
page).

Decision: the summary lives only in the human `.md`; other surfaces
point to it. README Foundations blurbs and docs/methods/README.md are
trimmed to pointers. The `.claude.md` files are operating instruction,
not summaries — unaffected. The site method page keeps its explanatory
register per D9-1 but links the human docs as source.

### D9-6 — template binding: URL pointer blessed, hybrid rule (DECIDED)

Finding: the front-diamond template mandates a pasted snapshot
("instructions cannot follow URLs"), yet the live portfolio project
binds by URL pointer; the WFM4.0 pasted copy is two versions stale.

Decision: bless the URL pointer as a hybrid rule. Cowork sessions may
bind by URL (they can fetch the canonical file live); plain Desktop
chats still require the pasted snapshot. The template header is
updated accordingly. The stale WFM4.0 copy is superseded by the URL
binding and will be cleaned up with D9-2's migration.

### D9-7 — diagram single-sourced; canonical is the site visual (DECIDED)

Finding: the two-diamond shape was hand-drawn three times (README
mermaid, repo-contract mermaid labels, site method-page visual).

Decision: the canonical is the site's visual, extracted to
`docs-site/assets/diamonds.svg` (self-contained, light/dark via
`prefers-color-scheme`). README and the method page include that one
file; the README mermaid is removed. Mermaid remains acceptable only
for sequence/technical diagrams — the repo contract's territory-flow
diagram is one such and stays as the single mermaid of its kind (it is
a different diagram, not a copy of the shape).

## Execution checklist (this PR)

- [x] This spec.
- [x] Spec statuses 1, 4, 6, 8 closed (D9-4).
- [x] CLAUDE.md: residency line (D9-1) + close-on-merge rule (D9-4).
- [x] docs-site/README.md and index.html label/count fixes + Method
      section (D9-3).
- [x] docs-site/assets/diamonds.svg created; method.html and README
      include it; README mermaid removed (D9-7).
- [x] README Foundations and docs/methods/README.md trimmed to
      pointers (D9-5).
- [x] Front-diamond template: hybrid binding rule (D9-6).
- [ ] WFM4.0 migration — deferred, separate session (D9-2).

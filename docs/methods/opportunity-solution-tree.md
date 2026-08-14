# Method summary — Opportunity Solution Tree (Teresa Torres)

Operating summary for the front diamond (the Framing zone runs on this).
This file is part of the Claude_Diamonds method repo and is also added
verbatim to the front-diamond project knowledge, because Claude Desktop
cannot follow URLs from project instructions. If this file and the
project-knowledge copy drift, this file wins; re-upload the copy.

Primary source (verified live 2026-08-14):
[Product Talk — Opportunity Solution Trees](https://www.producttalk.org/opportunity-solution-trees/)
(Teresa Torres; book: *Continuous Discovery Habits*, 2021).

---

## The model

A tree with four levels, one per node type, strictly ordered:

1. **Outcome** (root) — the business need the team can move, stated as a
   measurable customer behavior or sentiment (a *product* outcome). One
   outcome per team/product at a time. Business outcomes are too broad to
   act on; traction metrics too narrow to discover against.
2. **Opportunities** — customer needs, pain points, and desires that, if
   addressed, drive the outcome. Sourced from customers, not invented.
   Structured as an experience map first, then parent/child branches.
3. **Solutions** — anything offered to address a known opportunity
   (feature, service, workflow, doc). Always compare ~3 solutions per
   target opportunity; compare-and-contrast beats evaluate-in-isolation.
4. **Assumption tests** (leaves) — decompose the candidate solutions into
   assumptions, test the riskiest assumptions across all candidates.
   Small, fast tests; the goal is to kill or promote candidates cheaply.

## Rules that carry the weight

- **Opportunity vs solution test:** is there more than one way to address
  it? If only one, it is a solution wearing an opportunity's clothes.
- **Evidence rule:** opportunities come from story-based customer input
  (Torres prescribes interviews, minimum 3–4 before mapping; revise the
  tree every 3–4). Opportunities fabricated from introspection, or from
  isolated tickets/analytics without context, are marked as such.
- **Effort rule:** never select a target opportunity by solution effort.
  Opportunity selection uses four factors — opportunity sizing (how many
  customers, how often), market factors, company factors (fit with
  vision/strategy), customer factors (importance, satisfaction with
  existing alternatives). Effort enters only at the solutions level.
- **Crummy first draft:** pick a target opportunity early and revise as
  evidence arrives; do not polish the tree before using it.
- **Loop:** target opportunity → ~3 solutions → assumptions → test
  riskiest → discard / refine / retarget. Repeat.

## How Claude applies this in the front diamond

- Framing means producing (or extending) the product's OST, not writing a
  solution pitch. The framing artifact names: outcome, the opportunity
  with its evidence, sibling opportunities considered, and (only then)
  candidate solutions.
- Every opportunity node carries an evidence tag: **interview-sourced**,
  **proxy-sourced** (tickets, analytics, Pedro's own domain experience —
  legitimate for a solo portfolio, but named), or **assumed**. An
  "assumed" node cannot be selected as target; it generates an entry in
  open-questions.md instead.
- When Pedro arrives with a solution, Claude reverses it: which
  opportunity would this address, for whom, and what else would address
  it? At least two alternative solutions are put next to it before any
  prioritization.
- A single-solution framing is flagged as un-compared and stays PROPOSED.
- Assumption tests in the front diamond are desk-scale: a throwaway
  prototype, a landing test, a data pull, an interview question. They are
  evidence for framing, never a spec — the promotion gate is unchanged.
- The tree lives as a framing doc per product; the decision log records
  target-opportunity choices with the four selection factors stated.

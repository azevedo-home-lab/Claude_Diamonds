# Candidate spec 10 — Generic labels in all method and product docs

Status: PROPOSED 2026-08-15. The mechanical cleanup below was executed
same day by explicit Owner order (PII removal); the standing rule
awaits the Owner's decision per the CLAUDE.md spec process.

## Origin

Product-side decision D-017 (a product's decision log, 2026-08-15):
no personal names and no private project or repo names in product
docs — generic labels only (the Owner, Repo A/B). D-017 flagged that
the canonical front-diamond contract does not yet carry this rule and
named it a candidate spec for the method repo. This is that spec.

## Cleanup executed (Owner-ordered, this PR)

A repo-wide search found the personal name in six files; all were
substituted with "the Owner" (mechanical replacement, no content
change): CLAUDE.md, docs/repo-contract.md,
docs/methods/opportunity-solution-tree.claude.md,
docs/specs/2026-08-14-8-double-diamond-clarification.md,
docs/specs/2026-08-14-9-bloat-and-drift-corrections.md,
docs/templates/claude-desktop-project-instructions-front-diamond.md.

Reservation, on the record: specs 8 and 9 are historical records; a
substitution inside them edits history. Judged acceptable because the
change is a PII label swap that alters no decision, finding, or
meaning — and the Owner ordered the cleanup explicitly. The template
change implies the re-paste ritual (noted in the PR).

## Proposed standing rule (awaiting decision)

Add to the front-diamond template's working rules and to CLAUDE.md:

> Generic labels only, in every doc this method produces — method repo
> docs, product docs, published specs, and site pages. No personal
> names; no private project or repo names. Standard labels: "the
> Owner" (the human decider), "Repo A/B" (private product repos).
> Public repo names of the method itself are allowed. New docs comply
> at creation; an old doc found in violation is cleaned in a dedicated
> commit that names the substitution and nothing else.

## Consequences if adopted

- The template gains the rule → re-paste ritual for bound projects.
- The GitHub account/organization name itself remains visible in URLs
  and commit metadata — out of scope; the rule governs doc text only.
- Future specs quoting an Owner decision use the label, keeping specs
  publishable by default.

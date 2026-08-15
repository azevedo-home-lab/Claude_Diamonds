# Candidate spec 10 — Generic labels; literal-wording rule

Status: PROPOSED 2026-08-15. The mechanical cleanup below was executed
same day by explicit Owner order (PII removal, merged in PR #30); the
two standing rules await the Owner's decision per the CLAUDE.md spec
process.

## Origin

Product-side decision D-017 (a product's decision log, 2026-08-15):
no personal names and no private project or repo names in product
docs — generic labels only (the Owner, Repo A/B). D-017 flagged that
the canonical front-diamond contract does not yet carry this rule and
named it a candidate spec for the method repo. This is that spec.
Rule 2 was added after a same-day incident where a session
over-interpreted a literal UI instruction (hub top bar, fixed in
PR #33).

## Cleanup executed (Owner-ordered, PR #30)

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
change implies the re-paste ritual (noted in PR #30).

## Proposed rule 1 — generic labels (awaiting decision)

Add to the front-diamond template's working rules and to CLAUDE.md:

> Generic labels only, in every doc this method produces — method repo
> docs, product docs, published specs, and site pages. No personal
> names; no private project or repo names. Standard labels: "the
> Owner" (the human decider), "Repo A/B" (private product repos).
> Public repo names of the method itself are allowed. New docs comply
> at creation; an old doc found in violation is cleaned in a dedicated
> commit that names the substitution and nothing else.

## Proposed rule 2 — literal wording wins (awaiting decision)

Add to the front-diamond template's working rules:

> When the Owner specifies an output element literally — a label, a
> menu, a structure, exact wording — the literal specification wins
> over any interpretation or embellishment. If the literal reading and
> the session's interpretation diverge, ask before building; if the
> Owner is away, build the literal version and note the alternative.

Counterargument on record: taken too far, this rule could suppress
useful design judgment on genuinely underspecified requests. The rule
therefore binds only where the Owner's wording is concrete and
enumerable (labels, orderings, named sections), not where the request
is open ("beautify", "improve").

## Consequences if adopted

- The template gains both rules → re-paste ritual for bound projects.
- The GitHub account/organization name itself remains visible in URLs
  and commit metadata — out of scope; the rules govern doc text only.
- Future specs quoting an Owner decision use the label, keeping specs
  publishable by default.

## Note on CLAUDE.md state discipline (same PR, not part of this spec)

The "State discipline" section added to CLAUDE.md alongside this spec
revision was an explicit Owner order (spec-9 precedent for same-day
execution) and is recorded here for the trail, not proposed for
decision.

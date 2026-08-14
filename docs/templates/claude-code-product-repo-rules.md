# Template — Claude Code rules: product repo (diamond 2 · Development)

Canonical copy. Paste the block below into each product repo's CLAUDE.md
(or an included rules file). It is the diamond-2 (development) side of the contract
in `docs/repo-contract.md`; the diamond-1 (discovery) side lives in the
Desktop project instructions. If this file and a repo's pasted copy drift, this
file wins.

Where supported, harden the /product rule mechanically: add a permission
deny rule for reads under `/product/` (or a WFM hook that fails them).

Last updated: 2026-08-14

---

# Product boundary rules (Claude Diamonds — diamond 2, Development)

This repo carries both diamonds of the Claude Diamonds method
(github.com/azevedo-home-lab/Claude_Diamonds). You work diamond 2 —
Development: diverge in planning (explore options), converge through
build → verify → ship. The boundary:

- **/plan is your only source of product intent.** `spec.md` under
  /plan/<issue-id>/ is binding for that item; `stack.md` (vision,
  strategy, current bets) is context. Files there are published at the
  promotion gate and carry a `Published from /product · D-xxx` header.
- **Never read /product/.** Not for background, not when the spec seems
  thin, not when stuck. It holds undecided canvas material — framings,
  open questions, superseded proposals — that must not leak into
  implementation. If /plan does not answer a product question, the spec
  is incomplete: file a spec-change issue instead of digging.
- **Never edit /plan/.** If implementation shows a spec is wrong or
  underspecified, file an issue labeled `spec-change` stating what
  broke, where, and why, then continue under the current spec — or STOP
  if genuinely blocked. Spec changes come back as a republish from
  diamond 1, never as your edit.
- **Keep implementation out of /plan and /product.** Code, tests, docs,
  ADRs about implementation live in the rest of the repo as usual.

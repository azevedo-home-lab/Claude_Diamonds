# CLAUDE.md — working rules for this repository

## PR process (mandatory)

- Work starts on a fresh branch with a PR opened immediately — before the
  second commit exists.
- Every subsequent commit lands inside that open PR. Never commit to main;
  never push to a branch whose PR has merged.
- A merge closes the loop: next work, next branch, next PR.
- If a PR merges while work is still in flight, stop pushing to that
  branch; open a new branch and PR for the remainder immediately.

## State discipline (added 2026-08-15, Owner order, after a
stranded-commit incident — see PR #32's process note)

- Verify state live before every mutation; never act on remembered
  state. Concretely: check the PR's open/merged state before any push
  to its branch, and fetch a file's current content from the target
  branch before modifying it.
- Session start ritual for repo work: list open PRs and branches
  before starting anything new.
- A merged PR's branch is deleted promptly. A commit landing on a
  merged branch is stranded — unpublished and invisible; re-land it on
  a fresh branch from main, never leave it as the only copy.

## Repo boundaries

- This repo holds the method and its learning site: README, docs/methods
  (foundations), docs/templates (canonical paste blocks), docs/specs
  (candidate specs), docs/repo-contract.md, docs/canvas-snapshot.md, and
  docs-site/ (the published learning site — an official resident per
  spec 9, D9-1). Product artifacts never land here — they live in each
  product's own repo under the repo contract.
- Method changes are captured as dated, numbered candidate specs in
  docs/specs/, decided by the Owner, then executed in a later loop. Never
  applied ad hoc in the same conversation they were proposed.
- Specs are closed on merge: the PR that ships a spec updates that
  spec's Status line (e.g. "Done — shipped in PR #NN") in the same PR.
  A spec folder that records proposals but never outcomes is drift
  (spec 9, D9-4).
- Templates are canonical copies: each states where its pasted snapshot
  lives (Desktop project instructions, product-repo CLAUDE.md). The file
  in this repo wins over any snapshot; changing a template implies the
  re-paste ritual, and the PR description says so.

## File conventions — docs/methods/

- `<name>.md` — human learning doc: the model explained, with sources.
  Background for Claude; read only when extra context is genuinely
  needed, not on first approach.
- `<name>.claude.md` — compact operating instructions. These are the
  files uploaded to the front-diamond project knowledge and bound by the
  project instructions. Keep them short; depth belongs in the human doc.

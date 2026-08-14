# CLAUDE.md — working rules for this repository

## PR process (mandatory)

- Work starts on a fresh branch with a PR opened immediately — before the
  second commit exists.
- Every subsequent commit lands inside that open PR. Never commit to main;
  never push to a branch whose PR has merged.
- A merge closes the loop: next work, next branch, next PR.
- If a PR merges while work is still in flight, stop pushing to that
  branch; open a new branch and PR for the remainder immediately.

## Repo boundaries

- This repo holds the method only: README, docs/methods (foundations),
  docs/templates (canonical paste blocks), docs/specs (candidate specs),
  docs/repo-contract.md. Product artifacts never land here — they live in
  each product's own repo under the repo contract.
- Method changes are captured as dated, numbered candidate specs in
  docs/specs/, decided by Pedro, then executed in a later loop. Never
  applied ad hoc in the same conversation they were proposed.
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

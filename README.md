# Claude Diamonds

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

A method for running product decisions end to end with Claude, from raw
idea to shipped code. Two diamonds, each diverging then converging, with
one deliberate human gate between them: **Discovery & Solution Design**
(Claude Desktop / Cowork) ends in a Product Spec; **Development**
(Claude Code) turns that spec into judged, shipped code. Ideas live on a
canvas where they move, merge, and mostly die; committed work lives in a
ledger with identity and history. Asking one surface to hold both is the
failure this method exists to prevent.

![The Claude Diamonds method: Diamond 1 (Discovery & Solution Design — Discover, Define, Ideate, Decide), the promotion gate (DECIDED entry → issue → publish the spec), and Diamond 2 (Development — Plan, then Build · verify · ship).](docs-site/assets/diamonds.svg)

The canonical diagram source is
[`docs-site/assets/diamonds.svg`](docs-site/assets/diamonds.svg) — the
method page embeds the same file (spec 9, D9-7). The learning companion
site is at
[azevedo-home-lab.github.io/Claude_Diamonds](https://azevedo-home-lab.github.io/Claude_Diamonds/) —
its [Method page](https://azevedo-home-lab.github.io/Claude_Diamonds/method.html)
is the visual version of this README.

## Foundations

Each foundation's canonical summary is its learning doc in
[`docs/methods/`](docs/methods/) (spec 9, D9-5); a compact `.claude.md`
operating file beside it is what binds Claude. The blurbs below only
locate each foundation in the method — the learning doc is the summary.

### Double Diamond — Design Council (2004)

The shape: both diamonds diverge then converge, and the boundary between
them is a *converged artifact* — here the Product Spec.
[Framework for Innovation](https://www.designcouncil.org.uk/resources/framework-for-innovation/) ·
[spec 8](docs/specs/2026-08-14-8-double-diamond-clarification.md).

### The Decision Stack — Martin Eriksson

The vertical *why*, and the how/why test that finds the missing work.
Canonical summary: [decision-stack.md](docs/methods/decision-stack.md).

### Continuous Discovery & the Opportunity Solution Tree — Teresa Torres

The problem diamond and the divergent half of solution design.
Canonical summary:
[opportunity-solution-tree.md](docs/methods/opportunity-solution-tree.md).

### Prioritization — John Cutler

Diamond 1's convergence: force-ranked bets, never scored buckets.
Canonical summary:
[cutler-prioritization.md](docs/methods/cutler-prioritization.md).

### Spec-driven development, measured — WFM

Diamond 2 runs against the published spec with deterministic enforcement
(hooks, judges, evals) that must *earn its place* against a recorded
failure of the bare model.
[claude-code-workflows](https://github.com/azevedo-home-lab/claude-code-workflows#goal).

## How to run it

1. **Capture** into the parking lot — no commitment, no framing.
2. **Frame**: opportunity + evidence on the product's OST.
3. **Design**: ~3 compared solutions, riskiest assumptions tested cheaply.
4. **Rank**: force-ranked bets; check the stack — no trace up, no crossing.
5. **Promote**: DECIDED log entry → GitHub issue → publish the spec into
   `/plan`.
6. **Develop** against the published spec, judged — never against the
   vision.

## The repo contract

Each product repo carries both diamonds: `/product` (canvas + append-only
decision memory, diamond 1 only), `/plan` (the published spec and stack,
Claude Code's only source of product intent), and implementation. One-way
publish at the gate; a `spec-change` issue is the only channel back.
Full contract: [`docs/repo-contract.md`](docs/repo-contract.md).

## Repo map and scope

- [`docs/methods/`](docs/methods/) — the foundations: human learning
  docs (canonical summaries) plus their `.claude.md` operating files.
- [`docs/templates/`](docs/templates/) — canonical paste blocks for the
  Desktop project instructions and the product-repo CLAUDE.md.
- [`docs/specs/`](docs/specs/) — dated candidate specs: how this method
  changes, closed on merge.
- [`docs/repo-contract.md`](docs/repo-contract.md) — the /product ·
  /plan contract and the one-way publish.
- [`docs/canvas-snapshot.md`](docs/canvas-snapshot.md) —
  board-as-snapshot guidance.
- [`docs-site/`](docs-site/) — the learning site and the method's
  visual page, published via GitHub Pages.
- [`CLAUDE.md`](CLAUDE.md) — working rules for this repo (PR-based,
  mandatory).

In scope: the method, the zones, the gate, the contract, the templates.
Out of scope: enforcement machinery — hooks, judges, evals live in
[claude-code-workflows](https://github.com/azevedo-home-lab/claude-code-workflows)
and are cited, never duplicated.

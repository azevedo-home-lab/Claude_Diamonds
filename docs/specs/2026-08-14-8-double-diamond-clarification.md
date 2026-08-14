# Candidate spec — Correct the diamond framing: both diamonds diverge and converge

Status: PROPOSED 2026-08-14. Research and pinpointing done; doc corrections
are the next loop, after Pedro confirms the corrected framing.

## The misunderstanding, pinpointed

The repo currently equates **front diamond = divergence** and
**back diamond = convergence**. The equation originates in `README.md` and
has propagated:

- `README.md:21` — "The divergent half — capture an idea, frame it as a
  problem, weigh it against other problems, decide what comes first —
  wants a canvas."
- `README.md:25` — "The convergent half — spec, plan, build, prove, ship —
  wants a ledger."
- `README.md:38` — "Two diamonds. A canvas for divergence, a ledger for
  convergence, and one deliberate gate between them."
- `README.md:44` (mermaid) — "Canvas · Claude Desktop — diverge".
- `README.md:78` — "## The front diamond — divergent";
  `README.md:139` — "## The back diamond — convergent".
- Propagated to `docs/specs/2026-08-13-7-new-product-surface-pattern.md:23`
  ("Desktop diverges, the human gates, Code converges"), to
  `docs/templates/claude-desktop-project-instructions-front-diamond.md`
  ("This project is the divergent surface"), and — same day this spec was
  written — to `docs/repo-contract.md` and the repo-contract visual
  artifact ("Front diamond · diverge", "Back diamond · converge").

A second, related misplacement: `README.md:66` puts **spec** inside the
back diamond ("plan → spec → plan → judged build → ship"), while the repo
contract (docs/repo-contract.md, DECIDED the same day) has the spec
**published at the gate** — i.e., produced by the front diamond. The two
now contradict each other.

## The canonical model (verified live 2026-08-14)

Design Council Double Diamond (2004): **each diamond diverges then
converges.** Diamond 1 is the problem space — Discover (diverge: understand
rather than assume the problem) then Define (converge: reframe into a clear
challenge). Diamond 2 is the solution space — Develop (diverge: multiple
answers to the defined problem) then Deliver (converge: test, eliminate,
refine). The boundary between diamonds is the *defined problem*, not a
switch from divergent to convergent thinking.
Source: designcouncil.org.uk/resources/framework-for-innovation/.

Product-management adaptations (Huryn; consistent with Torres) relabel the
diamonds for discovery — Explore → Define → Ideate → Test — and observe
that discovery's output is a validated backlog/spec, with delivery as its
own subsequent process. Source: huryn.medium.com (Double Diamond of
Product Discovery / Triple Diamond of Product Management).

## The corrected framing (Pedro's, confirmed by the research)

- **Front diamond — Discovery / Solution Design** (Claude Desktop/Cowork).
  Internally it is itself a double diamond:
  - *Problem diamond:* Discover (diverge — parking lot, OST opportunity
    space) → Define (converge — target opportunity, framed with evidence).
  - *Solution-design diamond:* Ideate (diverge — ~3 compared candidate
    solutions, assumption tests) → Converge (prioritization, the winning
    solution written up).
  Its terminal, converged output is the **Product Spec** — the boundary
  artifact, published into /plan at the promotion gate.
- **Back diamond — Development** (Claude Code). Also diverge-then-converge:
  technical planning explores options (plan mode, architecture
  alternatives) before converging through build → verify → ship.
- **What survives unchanged:** the canvas/ledger distinction and the gate.
  Canvas vs ledger is about *artifact identity* (ideas that move, merge,
  and die vs items with state and history), not about diverge vs converge.
  The original framing conflated these two axes; decoupling them is the
  whole correction. Zones, methods docs, the repo contract's mechanics,
  and the gate ritual all stand.

## Why it matters (consequences, not naming)

1. "Front = diverge" denies the convergence the method already practices
   there (target-opportunity selection, force-ranked bets) — and a surface
   told it is divergent under-weights its convergent duties, i.e. specs
   stay vague.
2. "Back = converge" erases legitimate divergence in development (plan
   options, architecture alternatives) — directly relevant to the WFM 4.0
   architecture question (WFM4.0 D-003), which should model a
   diverge-then-converge development diamond, not a monotone pipeline.
3. The spec's home is currently stated in two contradictory places. The
   corrected model resolves it: the spec is the *end of front-diamond
   convergence*, published at the gate. Open question for the next loop:
   how WFM's in-repo spec-PR stage is reinterpreted — review/refinement of
   the published spec, rather than spec authoring. (Flagged, not decided.)

## README restructure (proposed outline, ~80 lines from ~220)

Research and sources first, per Pedro's direction; one sub-chapter per
foundational concept.

1. **What** — one paragraph + one corrected mermaid diagram: two diamonds,
   each diverge→converge — Discovery/Solution Design ending in the Product
   Spec, the human gate, Development ending in shipped code. Three lines of
   the board-asked-to-hold-ideas failure story, compressed, not deleted.
2. **Foundations** (sub-chapters, 3–5 lines each: what the method takes
   from it + primary source + in-repo summary link):
   Double Diamond (Design Council) · Decision Stack (Eriksson) ·
   Continuous Discovery & OST (Torres) · Prioritization (Cutler) ·
   Spec-driven development + WFM eval evidence.
3. **How to run it** — the six steps, one line each; "promote" becomes
   "publish the spec into /plan".
4. **The repo contract** — three lines + link to docs/repo-contract.md.
5. **Repo map and scope** — docs/methods, docs/templates, docs/specs;
   enforcement cited to WFM, never duplicated.

Moves, not deletions: canvas-snapshot guidance (localStorage caveat,
Claude Design constraints) → docs/canvas-snapshot.md; four-pillars table
and persona rationale → two lines + WFM links; zones/stack detail is
already carried by docs/methods/.

Counterargument on record: research-first can bury "what is this" for a
first-time visitor (mitigated by the What paragraph on top), and the split
adds one file to keep honest (docs/canvas-snapshot.md).

## Correction checklist (next loop)

- `README.md` — rewrite per the outline above: two diamonds, each
  diverge+converge; problem/solution-design vs development; canvas/ledger
  as identity axis; move spec out of the back-diamond chain; fix the
  mermaid labels and the front/back section headings.
- `docs/repo-contract.md` — relabel surfaces (Discovery/Solution Design ·
  Development); mechanics unchanged.
- `docs/templates/claude-desktop-project-instructions-front-diamond.md` —
  "divergent surface" → "discovery and solution-design surface (diverges
  and converges; output: the product spec)". Re-paste ritual applies.
- `docs/templates/claude-code-product-repo-rules.md` — one-line framing
  fix ("you work the development diamond").
- `docs/specs/2026-08-13-7-new-product-surface-pattern.md` — historical
  spec; add an erratum note rather than editing (append-only spirit).
- Repo-contract visual artifact — regenerate labels.
- WFM 4.0: feed consequence (2) into D-003.

## Sources

- Design Council, Framework for Innovation (Double Diamond, 2004) —
  https://www.designcouncil.org.uk/resources/framework-for-innovation/
- Paweł Huryn, How to Fix the Double Diamond of Design Thinking —
  https://huryn.medium.com/how-to-fix-the-double-diamond-of-design-thinking-327c1e2be41e
- Repo pinpointing: grep of README.md, docs/specs/, docs/templates/,
  docs/repo-contract.md at branch methods-docs, 2026-08-14.

# The method foundations — a reading guide

This folder holds the three methodologies the front diamond runs on, plus
the file convention that keeps Claude's context lean.

## Why these three

They cover the three questions every product decision must answer, in
order: **The Decision Stack** (Eriksson) answers *why*, **The
Opportunity Solution Tree** (Torres) answers *what problem and which
solution*, and **Cutler-style prioritization** answers *what first*.
Each model's summary lives in its own learning doc below — canonical
per spec 9 (D9-5); this file only explains how they compose.

Composed, they make the front diamond's two internal diamonds concrete:
Torres runs the problem diamond (discover → define a target opportunity)
and the divergent half of the solution-design diamond (~3 compared
candidates); Cutler runs its convergence (the ranked bet that becomes a
spec); Eriksson's stack is the traceability check the whole way down.
The product spec that exits the gate should survive all three: it traces
up the stack, it addresses an evidenced opportunity, and it displaced
something explicit to get built.

## Reading order

For a first pass: decision-stack.md → opportunity-solution-tree.md →
cutler-prioritization.md — each is a short, sourced summary of the
original author's model. The primary sources cited in each file are
better than any summary; these files exist so the method has a stable,
verified reference that does not drift with the web.

## The file convention (human / claude split)

Each methodology has two files. `<name>.md` (this folder's default) is
the **human learning doc**: the model explained in full, with sources —
Claude treats it as optional background, read only when extra context is
needed. `<name>.claude.md` is the **operating file**: compact
instructions, no theory — it is what gets uploaded to the front-diamond
project knowledge and bound by the project instructions. If the two ever
disagree, the .claude.md file is the one Claude follows; fix the drift
in the same PR that finds it.

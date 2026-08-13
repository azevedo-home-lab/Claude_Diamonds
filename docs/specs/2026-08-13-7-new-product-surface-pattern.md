# Surface pattern for starting a new product

## TLDR

A new product idea gets one Claude Project, and each of its three founding
artifacts gets the surface the method already prescribes for it. Vision is
divergent work and lives in Project chats on Claude Desktop. The high-level
spec is the gate artifact and is authored as files in a Cowork session
attached to the same Project. Architecture sits on the repo side of the
gate, drafted as versioned markdown with Mermaid/C4 diagrams by the coding
surface. This document records the pattern, checks it against how the
industry ran product ideation in 2026, and names what the industry does
that the method should absorb — and what it should not.

## Metadata

- **Issue:** —
- **Date:** 2026-08-13
- **Status:** Draft

## Context

The two-diamond method defines the boundary contract — Desktop diverges,
the human gates, Code converges — but it does not say how to *start* a new
product: which container to create first, and where each founding artifact
(vision, high-level spec, architecture) is authored. Asked directly, the
question was: new Claude Project in chat, or Cowork, and is this even the
right pattern given how industry and research teams run product ideation
in chat-plus-visual form?

A survey of the 2026 landscape found four recognizable camps:

| Camp | Representative tools | What it optimizes |
|---|---|---|
| Doc-centric chat | ChatPRD, Productboard AI, Notion AI | conversational PRD and vision generation |
| Visual canvas | Miro AI Innovation Workspace, FigJam AI, Whimsical | multiplayer divergence: clustering, OST mapping |
| Prototype-as-spec | Figma Make, Lovable, v0 | a clickable prototype as the communication artifact |
| Spec-driven development | Kiro, GitHub Spec Kit, BMAD-METHOD, OpenSpec | requirements → design → tasks before code |

The two-diamond method already straddles all four: the front diamond is a
solo doc-centric canvas, the back diamond is spec-driven development by
another name. Two findings from the survey are worth absorbing, and one
temptation is worth refusing.

**Worth absorbing.** First, the prototype-as-spec shift (Figma's
"prototypes are the new PRDs"; Teresa Torres's AI-prototyping work with
Lovable) fits the framing zone as a *lens*: a throwaway prototype is
evidence for an opportunity, not a spec, so it slots into zone 2 without
breaking the boundary contract. Second, Kiro's three-file split —
`requirements.md`, `design.md`, `tasks.md` — is a clean template for the
back diamond's artifacts: the design file *is* the high-level architecture
document, produced after the spec and before the build.

**Worth refusing.** A live multiplayer canvas (Miro, FigJam) is the
industry's answer to *collaborative* divergence. Solo, it is a second
system of record that drifts from the repo. It earns its place only when
a second human joins the front diamond.

## Goal

Someone starting a new product with this method can name, without
deliberation, the container to create and the surface each founding
artifact is authored on — and can say why each alternative was rejected.

## The pattern

One product, one Claude Project, created on Claude Desktop before anything
else. The Project's knowledge holds the decision stack (vision → North
Star → bets) so it accumulates across sessions instead of dying with each
chat. Project instructions carry the boundary contract and the lens
definitions.

| Artifact | Diamond | Surface | Form |
|---|---|---|---|
| Product vision | front | Project chats, Claude Desktop | decision-stack docs in Project knowledge |
| Opportunity docs, snapshot board | front | Cowork session attached to the Project, workspace folder connected | committed files |
| High-level spec | gate | Cowork, then the human promotes | spec file + GitHub issue + decision record |
| Architecture | back | Claude Code on the repo | `design.md`-style markdown with Mermaid/C4, versioned |

The division of labor between chat and Cowork inside the front diamond:
chat discusses, Cowork produces files. A vision conversation needs no
filesystem; an opportunity doc, a snapshot board, or a spec is a file and
belongs in a session that can write one.

Architecture stays behind the gate because of the method's own rule: give
the coding agent specs, not vision. It is drafted against the promoted
spec, in the repo, as reviewable markdown — never in the strategy chat.

## User stories

### P1 — Start a new product without re-deriving the pattern

As the product's founder, I want the founding sequence written down, so
that starting product N+1 costs a checklist and not a research session.

- **Given** a raw product idea, **when** I start, **then** the first act
  is creating a Claude Project for it on Desktop, with the decision-stack
  template and boundary contract seeded into Project knowledge.
- **Given** the Project exists, **when** vision work happens, **then** it
  happens in Project chats, and no vision text is pasted into the coding
  surface.
- **Given** an idea survives prioritization, **when** artifacts are
  needed, **then** a Cowork session attached to the same Project writes
  them into the workspace folder, and the promotion gate files the issue
  and decision record by hand.

### P2 — Architecture lands in the repo, traceably

As the person running the back diamond, I want architecture as a
versioned repo artifact, so that the build is judged against a design and
the design against a spec.

- **Given** a promoted issue, **when** architecture is drafted, **then**
  it lands as markdown with Mermaid/C4 diagrams in the repo, citing the
  spec and the decision record it serves.
- **Given** the architecture doc, **when** any claim in it is questioned,
  **then** it traces up: design → spec → issue → decision record → stack.

## Success criteria

- The founding sequence (Project → chats → Cowork → gate → repo) is
  stated in one place and matches the boundary contract table in the
  README — no new surface, no new zone.
- Each of the three founding artifacts names exactly one authoring
  surface, and each rejected alternative (live canvas as system of
  record, architecture in chat, vision in the coding agent) is rejected
  in writing with its reason.
- The two absorbed industry findings are actionable: prototype-as-lens is
  available in framing, and the spec/design/tasks file split is the named
  shape of the back diamond's artifacts.

## Out of scope

Adopting Miro or FigJam (deferred until the front diamond has a second
human); any tool-to-tool sync between Desktop, Cowork, and Code (the
shared folder and `CLAUDE.md` remain the only pipe); automating the
promotion gate.

## References

- Figma, [Prototypes are the new PRDs](https://www.figma.com/blog/prototypes-are-the-new-prds/) — prototype-as-spec, the 2026 framing.
- Teresa Torres, [AI Prototyping: How 11 Real-World Teams Are Transforming Their Work with Lovable](https://www.producttalk.org/ai-prototyping-lovable/) — prototypes as discovery evidence, from the OST author herself.
- MarkTechPost, [9 Best AI Tools for Spec-Driven Development in 2026](https://www.marktechpost.com/2026/05/08/9-best-ai-tools-for-spec-driven-development-in-2026-kiro-bmad-gsd-and-more-compare/) — Kiro, Spec Kit, BMAD compared; source of the three-file split.
- BCMS, [Spec-Driven Development: The Definitive 2026 Guide](https://www.thebcms.com/blog/spec-driven-development/) — SDD as the industry's back diamond.
- Productboard, [Best AI Tools for Writing Product Specs in 2026](https://www.productboard.com/blog/ai-tools-for-writing-product-specs/) — the doc-centric camp.
- Storyflow, [The 12 Best Visual Thinking Tools in 2026](https://storyflow.so/blog/best-visual-thinking-tools-2026) — the visual-canvas camp.

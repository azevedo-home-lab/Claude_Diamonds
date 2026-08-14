# The canvas is a snapshot, not live state

Moved here from the README (correction loop, spec 8) — unchanged in
substance.

Hand-author the prioritization board as committed HTML. State lives in the
browser's `localStorage`, so the committed file is a **starting
arrangement, not a system of record**. WFM's `docs/prioritization/` is the
precedent and carries the same caveat in its own README. The board is
republished as a snapshot when its arrangement changes; the ledger carries
state from there on.

Do not build the board on Claude Design. Design runs VM-isolated with a
separate localhost and has no automatic pipe from Desktop — you upload to
it by hand. That makes it a view and deck tool: use it to author the
*look* of a board or a shareable vision deck, never to hold the board's
data. Marc Bara's stack breakdown is the source for both constraints.

Two things people expect on the canvas are deliberately absent. A
**funnel** is not a zone — it is the motion between the three zones.
**Sequence** is not a zone either — it is a view of prioritization. That
is why the front surface has three zones and not five.

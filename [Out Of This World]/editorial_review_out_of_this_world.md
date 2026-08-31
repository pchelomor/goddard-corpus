# Editorial Review — Out Of This World

## Status
Hard editorial pass completed under `EDITORIAL_POLICY.md` using `SOURCE_FIRST_CANONICAL` mode.

## Why source-first mode was used
The extraction worker retained **493 candidate windows** from a canonical source of **189 paragraphs**, with **73 duplicate groups**. The candidate layer is useful for discovery, but reviewing every overlapping window independently would duplicate editorial work and distort coverage.

The canonical `master_text_out_of_this_world.txt` was therefore reviewed from beginning to end across all **4 chapters / 189 paragraphs**. Final selections were taken as exact Neville-only semantic fragments directly from the canonical source.

## Result
- Raw worker retained candidates: 493 (`417 CANDIDATE` + `76 REVIEW_RECOMMENDED`)
- Worker rejected: 11
- Worker failed verification: 0
- Raw duplicate groups: 73
- Canonical chapters reviewed: 4 / 4
- Canonical paragraphs covered: 189 / 189
- SELECT fragments: 20
- Strict SELECT density vs retained worker candidates: 4.1%
- Strict SELECT density vs canonical paragraphs: 10.6%

## Main editorial actions
- Collapsed repeated wish-fulfilled, assumption, SATS, and imaginal-action windows to the strongest standalone formulations.
- Retained the book's clearest practical language on attention, assumption, imagination, inner conversation, and self-concept.
- Excluded pure scripture from Neville attribution.
- Kept literal fourth-dimensional physics, serial-universe, precognition, and out-of-body claims out of the main automatic pool when they read as categorical scientific or metaphysical assertions rather than useful standalone philosophy.
- Held passages that imply direct control of other people's behavior, absolute manifestation guarantees, or universal external causation.
- Held or dropped medical/healing/sanity material and the mystical healing vision rather than turning it into context-free daily guidance.
- Treated the long quotation from Neville's earlier `The Search` as prior-work/self-quotation provenance rather than duplicating it in this local shortlist.
- Rejected context-sensitive formulations that could read as blaming a person for painful circumstances, conflict, illness, or other external events.

## Strongest thematic clusters
1. **Self-concept** — identity as the organizing principle of experience.
2. **Assumption** — assuming the fulfilled state rather than waiting for external confirmation.
3. **Imaginal action** — participating from first person, here and now, in a short act that implies fulfillment.
4. **Attention** — withdrawing attention from sense evidence and stabilizing it on the desired state with minimal effort.
5. **Inner conversation** — using spontaneous mental dialogue as evidence of the current self-concept.

## Files created
- `curated_out_of_this_world.jsonl`
- `editorial_decisions_out_of_this_world.jsonl`
- `editorial_review_out_of_this_world.md`
- `editorial_complete.json`

Raw extraction, rejected-candidate, source, and worker-report files were not modified.

# Editorial Review — Awakened Imagination

## Status
Hard editorial pass completed under `EDITORIAL_POLICY.md` using `SOURCE_FIRST_CANONICAL` mode.

## Why source-first mode was used
The worker retained **1,232 candidate windows** from a canonical source of **504 paragraphs**, with **182 duplicate groups**. The candidate layer is therefore useful for discovery, but too overlap-heavy to serve as the unit of final editorial judgment.

The canonical `master_text_awakened_imagination.txt` was reviewed from beginning to end across all **8 chapters / 504 paragraphs**. Final selections were taken as exact Neville-only semantic fragments directly from the canonical source.

## Result
- Raw worker retained candidates: 1,232 (`979 CANDIDATE` + `253 REVIEW_RECOMMENDED`)
- Worker rejected: 40
- Worker failed verification: 0
- Raw duplicate groups: 182
- Canonical chapters reviewed: 8 / 8
- Canonical paragraphs covered: 504 / 504
- SELECT fragments: 36
- Strict SELECT density vs retained worker candidates: 2.9%
- Strict SELECT density vs canonical paragraphs: 7.1%

## Editorial structure
`editorial_decisions_awakened_imagination.jsonl` uses **chapter-level source-first audit units**. Each chapter record confirms full review and records the selected quote IDs together with the principal HOLD/DROP reasons applied to non-selected material. This avoids serializing more than a thousand artificial sliding-window decisions while preserving full source coverage.

## Main editorial actions
- Collapsed repeated `thinking of` / `thinking from` windows to the strongest formulations.
- Kept the clearest definitions of **state**, **inner speech**, **revision**, **habit**, **feeling of the wish fulfilled**, and **thinking from the end**.
- Excluded pure scripture and quotations from Blake, Emerson, Yeats, Lawrence, Quintilian, Hermes and other external authors from Neville attribution.
- Kept long autobiographical and testimonial material out of the automatic pool when the surrounding narrative was stronger than the standalone maxim.
- Held the blind-girl and healing narratives rather than treating them as general medical claims.
- Held passages that make categorical medical, financial, miraculous, bilocation, or universal-causation claims when the passage would need context or an epistemic note.
- Chapter 8 was kept as `HOLD` for a future spiritual/scriptural opt-in layer; no main-pool quotation was selected from it.

## Strongest thematic clusters
1. **Thinking from the end** — participation in the fulfilled state rather than observation of it.
2. **Revision** — changing the inner representation of a lived event, with emphasis on forgiveness and self-change.
3. **Inner conversation** — treating habitual inner speech as a practical signal of the state being occupied.
4. **Habit and state** — repeated moods, beliefs and imaginative patterns as the mechanism of continued occupancy.
5. **Imagination as practice** — concrete inner scenes and felt movement rather than abstract wishing.

## Files created
- `curated_awakened_imagination.jsonl`
- `editorial_decisions_awakened_imagination.jsonl`
- `editorial_review_awakened_imagination.md`
- `editorial_complete.json`

Raw extraction and source files were not modified.

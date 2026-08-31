# Editorial Review — I Know My Father

## Status
Hard editorial pass completed under `EDITORIAL_POLICY.md` using `SOURCE_FIRST_CANONICAL` mode.

## Why source-first mode was used
The worker retained **892 candidate windows** from a canonical source of **177 paragraphs**, with **86 duplicate groups**. The extraction layer is therefore useful for discovery but materially overgenerated for direct candidate-by-candidate editorial review.

The complete canonical `master_text_i_know_my_father.txt` was reviewed from beginning to end across the full **10-chapter / 177-paragraph** book. Final selections were taken as exact Neville-only semantic fragments directly from the canonical source rather than choosing among overlapping worker windows.

## Result
- Raw worker retained candidates: 892 (`712 CANDIDATE` + `180 REVIEW_RECOMMENDED`)
- Worker rejected: 14
- Worker failed verification: 0
- Raw duplicate groups: 86
- Canonical chapters reviewed: 10 / 10
- Canonical paragraphs covered: 177 / 177
- SELECT fragments: 17
- Strict SELECT density vs retained worker candidates: 1.9%
- Strict SELECT density vs canonical paragraphs: 9.6%

## Main editorial actions
- Collapsed repeated I AM, awareness, self-concept, and present-tense windows into the strongest standalone formulations.
- Preserved core Neville wording on self-conception, feeling, naturalness, assumption, and awareness when the fragment remained clean and understandable on its own.
- Excluded pure scripture and scripture-dominant retellings from Neville attribution.
- Held long circumcision, crucifixion/resurrection, and other theological allegory for contextual or spiritual opt-in use rather than the main automatic pool.
- Kept categorical medical and mental-health claims out of the automatic pool, including passages dismissing germs/diagnoses or promising cure through consciousness alone.
- Excluded the passage that transfers healing/strength/security away from drugs, diet, or money because it would be unsafe and misleading when delivered without context.
- Kept categorical financial guarantees, poverty/blame formulations, political/war causation, and strong universal-causation passages out of the automatic pool.
- Held sensory-evidence-denial passages when decontextualization could encourage ignoring material evidence rather than using imagination as a reflective practice.
- Retained a small number of strong metaphysical formulations when they are clearly recognizable as Neville's philosophy and do not depend on a dangerous practical inference.

## Strongest thematic clusters
1. **Self-concept** — the conception of self as the lens through which experience is interpreted.
2. **I AM / awareness** — awareness distinguished from the particular identity or state it assumes.
3. **Feeling and naturalness** — asking how fulfillment would feel and making the new feeling natural.
4. **Present-tense assumption** — moving from “I shall be” to the consciousness of being now.
5. **Expression** — Neville's recurring claim that expression follows the state with which consciousness is identified.

## Files created
- `curated_i_know_my_father.jsonl`
- `editorial_decisions_i_know_my_father.jsonl`
- `editorial_review_i_know_my_father.md`
- `editorial_complete.json`

Raw extraction and source files were not modified.

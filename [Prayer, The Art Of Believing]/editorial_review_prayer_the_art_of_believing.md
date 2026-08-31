# Editorial Review — Prayer, The Art Of Believing

## Status
Hard editorial pass completed under `EDITORIAL_POLICY.md` using `SOURCE_FIRST_CANONICAL` mode.

## Why source-first mode was used
The worker retained **700 candidate windows** from a canonical source of **192 paragraphs**, with **89 duplicate groups**. The extraction is useful for discovery but contains substantial overlap, nested variants, and repeated formulations.

The canonical `master_text_prayer_the_art_of_believing.txt` was reviewed from beginning to end across all **7 chapters / 192 paragraphs**. Final selections were taken as exact Neville-only semantic fragments directly from the canonical source.

## Result
- Raw worker retained candidates: 700 (`581 CANDIDATE` + `119 REVIEW_RECOMMENDED`)
- Worker rejected: 11
- Worker failed verification: 0
- Raw duplicate groups: 89
- Canonical chapters reviewed: 7 / 7
- Canonical paragraphs covered: 192 / 192
- SELECT exact fragments: 21
- Strict SELECT density vs retained worker candidates: 3.0%
- Strict SELECT density vs canonical paragraphs: 10.9%

## Main editorial actions
- Collapsed repeated prayer / assumption / fulfilled-desire windows to the strongest standalone formulations.
- Preserved core Neville wording about faith, feeling, imagination, attention, belief, self-concept, and inner conversation when clean and self-contained.
- Excluded the Tennyson epigraph, pure scripture, Augustine, and other external wording from Neville attribution.
- Kept the book's historical `law of reversibility` argument contextual where it is presented as a universal scientific law; selected only clean practical fragments that do not depend on that pseudo-scientific framing.
- Excluded categorical claims that expectation or suggestion can cure what medical treatment cannot, and passages that could discourage appropriate medical care.
- Excluded or held claims about telepathy, hypnotic control, covert suggestion without consent, inability of another person to resist, and deterministic denial of free will.
- Excluded categorical claims about causing another person's behavior, remote healing/wealth, internal causation of sunburn, age/decay as merely sleeping health, and rebound of malicious thoughts.
- Held strong spiritual identity material such as `I AM Christ` for an opt-in spiritual layer rather than the main automatic pool.
- Dropped poverty-as-sleep-of-wealth and similar formulations where decontextualization could become misleading or blame-oriented.

## Strongest thematic clusters
1. **Prayer as assumed fulfillment** — prayer as feeling and accepting the completed state rather than continued seeking.
2. **Belief and assumption** — fixed belief as more decisive than effort or will.
3. **Imagination** — imagination as the formative faculty and controlled reverie as a practice.
4. **Attention** — the state receiving attention as the state that dominates experience.
5. **Inner conversation** — self-talk and mental speech as an important form of prayer.
6. **Self-concept** — changing one's conception as the route to changing experienced conditions.

## Files created
- `curated_prayer_the_art_of_believing.jsonl`
- `editorial_decisions_prayer_the_art_of_believing.jsonl`
- `editorial_review_prayer_the_art_of_believing.md`
- `editorial_complete.json`

Raw extraction and source files were not modified.

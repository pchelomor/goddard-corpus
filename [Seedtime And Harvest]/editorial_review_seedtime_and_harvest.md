# Editorial Review — Seedtime And Harvest

## Status
Hard editorial pass completed under `EDITORIAL_POLICY.md` using `SOURCE_FIRST_CANONICAL` mode.

## Why source-first mode was used
The worker retained **1,145 candidate windows** from **360 canonical paragraphs**, with **149 duplicate groups**. The extraction layer therefore contains substantial overlapping and nested variants that are useful for discovery but inefficient as independent editorial units.

The complete canonical `master_text_seedtime_and_harvest.txt` was reviewed from beginning to end across all **9 chapters / 360 paragraphs**. Final selections were taken as exact Neville-only semantic fragments directly from the canonical source.

## Result
- Raw worker retained candidates: 1,145 (`913 CANDIDATE` + `232 REVIEW_RECOMMENDED`)
- Worker rejected: 15
- Worker failed verification: 0
- Raw duplicate groups: 149
- Canonical chapters reviewed: 9 / 9
- Canonical paragraphs covered: 360 / 360
- SELECT exact fragments: 23
- Strict SELECT density vs retained worker candidates: 2.0%
- Strict SELECT density vs canonical paragraphs: 6.4%

## Main editorial actions
- Collapsed repeated worker windows around the `Four Mighty Ones`, wish-fulfilled scenes, attention, inner conversation, and state-change material into one preferred formulation per editorial idea.
- Preserved strong practical Neville wording on constructing the final scene, participating in imaginal action, controlling attention, inner speech, and feeling oneself already in the desired state.
- Excluded Blake, Shakespeare, Angelus Silesius, Browning, Thoreau, Scripture, and other external wording from Neville attribution.
- Kept scripture-heavy allegory and theological symbolism as contextual `HOLD` when the passage did not survive as a clean Neville-only daily quotation.
- Excluded the birthmark cure and sick-cat healing stories, plus categorical healing implications, from the automatic pool.
- Excluded or held passages that attribute accidents, death, discriminatory burial events, poverty, theft recovery, or another person's behavior to the individual's state of consciousness when decontextualization could become misleading or victim-blaming.
- Held direct-control-of-others formulations and testimonial passages where another person's conduct is presented as compelled by the imaginal act.
- Kept the practical inner-conversation material from the `game of life` section while excluding stronger financial-prosperity implications.
- Retained concise core metaphysical wording when it is clean and self-contained, while holding stronger claims that the entire physical world is solely a construction of mind.

## Strongest thematic clusters
1. **Wish fulfilled / final scene** — constructing the last scene rather than mentally rehearsing the path to it.
2. **Directed attention** — repeatedly returning attention to the imaginal action until it becomes natural.
3. **Inner conversation** — treating habitual inward speech as a train of thought that can be observed and redirected.
4. **State change** — changing attitude and self-position rather than fighting an external opponent.
5. **Applied imagination** — converting knowledge into action rather than leaving it at the level of theory.

## Files created
- `curated_seedtime_and_harvest.jsonl`
- `editorial_decisions_seedtime_and_harvest.jsonl`
- `editorial_review_seedtime_and_harvest.md`
- `editorial_complete.json`

Raw extraction and source files were not modified.

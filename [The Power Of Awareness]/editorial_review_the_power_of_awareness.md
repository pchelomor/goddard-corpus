# Editorial Review — The Power Of Awareness (1953 lecture)

## Status
Hard editorial pass completed under `EDITORIAL_POLICY.md` using `SOURCE_FIRST_CANONICAL` mode.

## Identity note
This folder is **not the 1952 book** commonly known as *The Power of Awareness*. Its `source_manifest.md` identifies it as corpus item **L0185**, a **1953-01-01 spoken lecture** of the same title. It is therefore reviewed as a distinct lecture work. The legacy book row in `EDITORIAL_JOURNAL.md` should remain unresolved until a separate canonical book source exists in the repository.

## Why source-first mode was required
The worker retained **375 candidate windows** (`300 CANDIDATE` + `75 REVIEW_RECOMMENDED`) from only **32 canonical paragraphs**, with **28 duplicate groups**. The candidate set is dominated by overlapping sliding windows and nested variants, so the canonical transcript is the appropriate editorial authority.

The complete `master_text_the_power_of_awareness.txt` was reviewed from beginning to end across all **32 paragraphs**. Final selections were cut directly from Neville's own prose rather than from worker window boundaries.

## Result
- Raw worker retained candidates: 375
- Worker rejected: 13
- Worker failed verification: 0
- Raw duplicate groups: 28
- Canonical paragraphs covered: 32 / 32
- SELECT exact Neville fragments: 12
- Strict SELECT density vs retained worker candidates: 3.2%
- Strict SELECT density vs canonical paragraphs: 37.5%

The high paragraph-level density reflects the lecture's structure: each paragraph is long and often contains several semantic units, while the worker overgenerated many overlapping windows from each paragraph.

## Main editorial actions
- Preserved the cleanest Neville-only formulations on consciousness in action as imagination, identity versus state, viewpoint, thinking from an end, deliberate self-observation, and the feeling of the fulfilled state.
- Excluded pure scripture and scripture-dominant paraphrase from Neville attribution.
- Held Christological and `Second Man` symbolism for a spiritual/contextual layer rather than the automatic pool.
- Excluded categorical formulations that assign all painful events to a person's own choice or imply blame for circumstances beyond their control.
- Held strong sensory-evidence-denial, dimensional-world, and direct-influence-of-others passages where decontextualization could become misleading.
- Collapsed repeated `state`, `thinking from`, `imagination`, and fulfilled-desire formulations to the strongest local wording.
- Preserved obvious transcription/OCR meaning while avoiding editorial expansion or rewriting of Neville's ideas.

## Strongest main-pool clusters
1. **Identity and state** — separating the enduring self from the state of consciousness presently occupied.
2. **Viewpoint** — recognizing that the state from which one observes shapes the description one gives of the world.
3. **Thinking from the end** — moving from thinking *of* a desired state to thinking *from* it.
4. **Self-observation** — watching how imagination operates and noticing habitual mental movement.
5. **Fulfilled-state awareness** — deliberately becoming aware of the felt state associated with a fulfilled desire.

## Files created
- `curated_the_power_of_awareness.jsonl`
- `editorial_decisions_the_power_of_awareness.jsonl`
- `editorial_review_the_power_of_awareness.md`
- `editorial_complete.json`

Raw extraction, candidate, rejected, source, and worker-report files were not modified.

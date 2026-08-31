# Editorial Review — He Breaks The Shell

## Status
Hard editorial pass completed under `EDITORIAL_POLICY.md` using `SOURCE_FIRST_CANONICAL` mode.

## Why source-first mode was used
The worker retained **188 candidate windows** from a canonical source of **98 paragraphs**, with **34 duplicate groups**. The candidate layer is useful for discovery, but section-level canonical review is the more reliable editorial unit.

The complete monograph was reviewed from beginning to end: **Introduction + Acts 1–4 + Conclusion**, covering all **98 canonical paragraphs**.

## Result
- Raw worker retained candidates: 188 (`166 CANDIDATE` + `22 REVIEW_RECOMMENDED`)
- Worker rejected: 6
- Worker failed verification: 0
- Raw duplicate groups: 34
- Canonical paragraphs covered: 98 / 98
- SELECT fragments for the main automatic pool: **0**
- HOLD: all substantive Promise/mystical material not otherwise dropped
- DROP: primarily external/scripture-dominant introductory material and weak standalone units

## Why the curated main-pool file is intentionally empty
This work is almost entirely a concentrated statement of Neville's later **Promise** theology: resurrection in the skull, supernatural birth, Davidic fatherhood, the split body/serpent imagery, the dove experience, and categorical identity claims about Christ and man. These passages are historically central to Neville's teaching, but their value depends on explicit spiritual/metaphysical context.

Under the current editorial policy, highly sectarian or strongly literal metaphysical material is better retained as `HOLD` for a future **spiritual / Promise opt-in layer** rather than delivered automatically as context-free daily quotations.

This is therefore not a judgment that the monograph lacks importance. It is a product-suitability decision: **archivally important, but no fragment cleared the stricter automatic main-pool threshold without context**.

## Main editorial actions
- Excluded Blake's opening line and pure Bible quotations from Neville attribution.
- Avoided promoting scripture-dependent fragments whose standalone meaning changes when detached from the surrounding argument.
- Held the four supernatural acts as contextual material rather than converting them into short universal claims.
- Held the concluding formulations about God, Christ, resurrection, and identity for a future Promise/spiritual opt-in corpus.
- Preserved the raw source, candidates, rejected file, report, and manifest unchanged.

## Files created
- `curated_he_breaks_the_shell.jsonl` — intentionally empty main-pool shortlist
- `editorial_decisions_he_breaks_the_shell.jsonl`
- `editorial_review_he_breaks_the_shell.md`
- `editorial_complete.json`

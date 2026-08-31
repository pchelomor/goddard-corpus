# Editorial Review — At Your Command

## Status
Hard editorial pass completed under `EDITORIAL_POLICY.md` using `SOURCE_FIRST_CANONICAL` mode.

## Why source-first mode was used
The worker produced **711 candidate windows from 110 source paragraphs**, including **171 duplicate groups**. Many candidates are nested or overlapping windows of the same paragraph rather than independent quotations. Treating all 711 windows as separate editorial objects would preserve the worker's overgeneration instead of correcting it.

Therefore the canonical `master_text_at_your_command.txt` was reviewed from beginning to end, paragraph by paragraph. Exact Neville-only fragments were selected directly from the source; the raw worker candidate files remain untouched as discovery/provenance material.

## Result
- Raw worker candidates: 711
- Canonical source paragraphs reviewed: 110 / 110
- SELECT fragments: 20
- HOLD paragraphs: 67
- DROP paragraphs: 23
- Strict SELECT density vs raw worker candidates: 2.8%
- Source paragraph coverage: 100%

## Main editorial actions
- Collapsed the large sliding-window overgeneration instead of treating near-identical windows as separate quotes.
- Excluded scripture-dominant passages from the main Neville-only daily pool.
- Kept spiritual/scriptural interpretations in HOLD when they are useful for a future opt-in thematic layer.
- Excluded categorical medical-healing claims and the worker's medical/financial miracle examples from the main pool.
- Excluded or held passages that can imply victim-blaming or that all accidents, interpersonal harm, poverty, or illness are self-caused.
- Held literal problem-avoidance passages where a standalone daily card could be read as advice to ignore concrete problems.
- Retained Neville's metaphysical voice when a formulation is clean, exact, memorable, source-independent enough, and central to the work.

## Representative SELECT themes
The 20 selected fragments concentrate on:
- decreeing as an act of consciousness rather than verbal repetition;
- self-concept and how one sees oneself;
- changing consciousness rather than merely fighting appearances;
- the order "signs follow, they do not precede";
- leaving old beliefs, fears, and limitations behind;
- naturalness, conviction, gratitude, and wish-fulfilled practice;
- desire, worthiness, and self-expression;
- recognition and embodiment of states.

## Representative HOLD categories
- scripture-centered exegesis and theological framing;
- long I AM / biblical symbolism passages;
- absolute metaphysical guarantees;
- financial or health examples that are historically part of the book but unsuitable for automatic daily delivery;
- longer technique passages whose meaning depends on the surrounding metaphor or story;
- spiritual statements better reserved for opt-in reading.

## Representative DROP categories
- pure scripture or scripture-dominant text;
- narrative setup and parable retelling with no standalone Neville insight;
- tithing exposition that is not useful as a daily quotation;
- categorical medical healing anecdotes;
- categorical financial guarantees;
- victim-blaming formulations about accidents, other people's behavior, condemnation, poverty, or illness;
- violence discussion and anecdotal filler.

## Files produced
- `curated_at_your_command.jsonl` — 20 exact SELECT fragments.
- `editorial_decisions_at_your_command.jsonl` — decision for all 110 canonical source paragraphs.
- `editorial_review_at_your_command.md` — this report.
- `editorial_complete.json` — machine-readable completion marker for this editorial pass.

## Notes for later global deduplication
Several core ideas in this book are likely to recur in later works, especially:
- consciousness as cause / doorway;
- self-concept determines expression;
- signs follow rather than precede;
- do not concern yourself with the HOW;
- gratitude before sensory evidence;
- desire accepted as already fulfilled.

These should not be deduplicated globally until all book-level curated files exist.

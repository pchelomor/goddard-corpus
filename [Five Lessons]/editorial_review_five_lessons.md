# Editorial Review — Five Lessons (Master Class)

- **Corpus ID:** `S001`
- **Review mode:** `SOURCE_FIRST_CANONICAL`
- **Authoritative canonical file:** `master_text_five_lessons.txt`
- **Canonical sections reviewed:** 6 / 6 — Lesson 1, Lesson 2, Lesson 3, Lesson 4, Lesson 5, Master class Q&A
- **Canonical paragraphs reviewed:** 858 / 858
- **Retained worker windows:** 4,516 (`3,749` candidate + `767` review-recommended)
- **Worker rejected windows:** 105
- **Raw duplicate groups:** 612
- **Strict SELECT fragments:** 19

## Canonical identity decision

`corpus_registry.json` defines `S001` as a single corpus item, **Five Lessons (Master Class)**, and lists the five lesson titles plus `Lessons Q & A` as alternate titles. The `[Five Lessons]/source_manifest.md` independently defines the authoritative S001 master as the complete five-lesson course plus the full Q&A: 858 paragraphs and approximately 45,609 words.

The similarly named top-level folders are not component files that must be concatenated to construct S001. Their manifests identify them as separate lecture corpus items: Lesson 1 is `L0099`, Lesson 2 `L0100`, Lesson 3 `L0101`, Lesson 4 `L0102`, Lesson 5 `L0103`, and `Lessons Q & A` is `L0104`. The Dutch-titled `Les 1 – Bewustzijn Is De Enige Werkelijkheid` is separately registered as `L0098`. These items can be used for cross-checking and later cross-work deduplication, but they do not replace the authoritative S001 master.

## Source-first coverage

The complete canonical master was read sequentially from the opening `Lesson 1` heading through the final Q&A answer and `THE END.`. Worker candidate windows were used only as discovery/provenance support. They were not treated as source coverage, because the extraction produced extensive sliding-window overlap.

The worker report records 4,621 generated windows, of which 4,516 were retained for candidate/review consideration and 105 rejected; it also records 612 duplicate groups. The canonical source remains the authoritative editorial denominator: 858 source paragraphs, all reviewed.

## Editorial result

The provisional editorial layer already present in the folder was re-reviewed rather than accepted at face value. Its 27 SELECT fragments were reduced to **19** after applying the strict automatic-pool threshold to the full source.

The final automatic pool favors exact, compact Neville formulations about clarifying desire, imaginal participation, attention without strain, the feeling of the wish fulfilled, constructing a single implied event, testing the teaching in experience, and self-concept. Strong fragments that were missed by the provisional shortlist were added where the canonical source supplied a cleaner standalone boundary.

## HOLD treatment

Material was held for contextual or opt-in use when it depended on extended scripture interpretation, complex theological symbolism, spiritual-identity claims, dimensional or mystical models, strong literal metaphysical claims, predetermination, testimonial context, or claims that another person's behavior is influenced by one's inner state.

Several famous Neville formulations were deliberately not promoted to the automatic pool when their standalone wording becomes a literal guarantee or an unsafe universal-causation claim. Historical or doctrinal importance was not treated as sufficient for SELECT.

## DROP treatment

The automatic pool excludes pure scripture and external quotations; categorical medical, bodily, or pain claims; passages discouraging medical or dietary reliance; financial guarantees; guaranteed physical outcomes; victim-blaming or event-causation formulations; coercive/control-of-others language; pseudo-scientific claims; weak generic fragments; and weaker local duplicates.

Lesson 4 contains a substantial self-reprinted passage from `The Search`. Quotations originating in that embedded reprint were not duplicated into the S001 daily shortlist merely because they reappear inside the master class. This preserves provenance and avoids inflating the corpus with a second local SELECT for the same wording.

## Auditability

`editorial_decisions_five_lessons.jsonl` now contains an audit summary plus six section-level decision records, one for each canonical section. Each record identifies the selected quote IDs and the principal HOLD/DROP reason families applied to the rest of that fully reviewed section. This replaces the earlier single-record decision file, which was too coarse to demonstrate source-first section coverage.

## Files written

- `curated_five_lessons.jsonl`
- `editorial_decisions_five_lessons.jsonl`
- `editorial_review_five_lessons.md`
- `editorial_complete.json`

Raw source and worker artifacts were not changed: `master_text_five_lessons.txt`, `candidates_five_lessons.jsonl`, `rejected_five_lessons.jsonl`, `report_five_lessons.md`, `source_manifest.md`, `source_variations.md`, and `processing_complete.json` remain untouched.

# Editorial Policy — Hard Selection

This repository stores **raw archival candidates** and a separate **strict editorial layer** for the final Neville Goddard quote corpus.

## Principle

Raw extraction is intentionally broad. The editorial layer is intentionally severe.

The goal is **not to preserve the maximum number of quotations**. The goal is to keep only formulations that are strong enough to deserve repeated use in a high-quality daily quote product.

## Raw files are immutable

Do not delete or rewrite:

- `candidates_*.jsonl`
- `rejected_*.jsonl`
- `master_text_*.txt`
- `source_manifest.md`
- `source_variations.md`
- worker reports

Editorial work is added as new files beside them.

## Editorial outputs per work

For every book/work create:

- `curated_<slug>.jsonl` — strict accepted shortlist only.
- `editorial_decisions_<slug>.jsonl` — compact decision record for every reviewed candidate.
- `editorial_review_<slug>.md` — human-readable review summary.

## Decisions

Each source candidate receives one of three decisions:

- `SELECT` — strong enough for the main corpus and potentially eligible for daily delivery.
- `HOLD` — valuable archival/contextual material, but not strong or safe enough for the main automatic pool.
- `DROP` — redundant, weak, context-dependent, misbounded, mostly scripture/external quotation, or otherwise not worth retaining in the curated layer.

`curated_<slug>.jsonl` contains only `SELECT` records.

## Hard-selection criteria

A `SELECT` quotation should normally satisfy all of the following:

1. **Exact authorship** — verified as Neville Goddard's own wording.
2. **Standalone meaning** — understandable without reading the preceding page.
3. **One clear idea** — not a large explanatory paragraph containing several ideas.
4. **Memorability** — concise, distinctive, and worth rereading.
5. **Author specificity** — recognizably relevant to Neville's philosophy rather than generic advice.
6. **Clean boundaries** — no arbitrary sliding-window variants or unnecessary lead-in/tail text.
7. **Low context dependency** — no missing antecedent, hidden condition, or misleading truncation.
8. **No stronger duplicate** — if the same idea is expressed better elsewhere in the same work, keep the strongest wording only.
9. **Daily-product suitability** — something a user could receive on its own without the bot needing to repair the quotation.

## Preferred length

Length is not a mechanical rule, but for the main pool:

- ideal: about 8–45 words;
- acceptable: up to about 60 words when needed for completeness;
- above 60 words: rare and requires a clear editorial reason.

A shorter quotation is **not automatically better** if shortening destroys the author's meaning.

## Scripture and external quotations

Pure scripture or another author's words are not selected as Neville quotations.

If Neville's own point surrounds a biblical quotation:

- prefer extracting Neville's own standalone wording;
- otherwise classify as `HOLD` unless the mixed passage is uniquely important.

## Risk-sensitive content

The following normally do not enter the automatic daily pool without a specific reason/context:

- categorical medical or mental-health claims;
- categorical scientific claims;
- financial guarantees;
- passages whose value depends on literal acceptance of a strong metaphysical assertion;
- highly sectarian/spiritual passages better suited to an opt-in topic.

Such text may still be historically important and can remain `HOLD`.

## Duplicate policy inside one work

Worker-generated extraction often contains overlapping windows of the same passage. Treat these as one editorial idea cluster.

For every cluster:

1. identify the cleanest semantic unit;
2. keep at most one `SELECT` wording unless two variants genuinely express different ideas;
3. mark the others `DROP` or `HOLD` with a duplicate reason.

## Cross-work duplication

After all books are reviewed, perform a global pass across the curated files.

For repeated ideas across books:

- select one **canonical quotation**;
- preserve alternate occurrences as provenance/variants;
- do not inflate the final corpus with near-identical formulations.

## Scores from extraction workers

Worker scores are advisory metadata only.

Do **not** accept a quotation merely because `overall_score` is high. Editorial judgment is independent of worker scores, because extraction runs may systematically over-score or create many overlapping high-scoring variants.

## Target density

There is no fixed quota per book.

However, strict editorial density should be dramatically lower than raw extraction. A work should contribute only its genuinely strongest and most distinctive formulations.

The final book corpus should favor **hundreds of excellent unique quotations**, not thousands of merely acceptable fragments.

## Final global corpus

After local reviews create:

- `curated_books_master.jsonl`
- `cross_book_duplicates.jsonl`
- `BOOKS_EDITORIAL_SUMMARY.md`

The master corpus should contain the canonical, globally deduplicated selections from all reviewed books.

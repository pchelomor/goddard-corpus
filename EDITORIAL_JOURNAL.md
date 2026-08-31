# Editorial Journal — Neville Goddard Corpus

This journal tracks the strict book-by-book review defined in `EDITORIAL_POLICY.md`.

## Decision vocabulary
- **SELECT** — main curated corpus / daily-pool candidate.
- **HOLD** — valuable but contextual, sensitive, mixed-source, or not strong enough for automatic delivery.
- **DROP** — weak, duplicate, misbounded, mostly external/scripture, generic, or unsuitable for the curated layer.

## Progress

| Work | Status | Reviewed | SELECT | HOLD | DROP | Output |
|---|---:|---:|---:|---:|---:|---|
| Feeling Is the Secret | COMPLETE | 88 candidates | 29 | 46 | 13 | `Feeling Is the Secret/curated_feeling_is_the_secret.jsonl` |
| At Your Command | COMPLETE | 110 paragraphs / 711 raw windows | 20 | 67 | 23 | `[At Your Command]/curated_at_your_command.jsonl` |
| Awakened Imagination | COMPLETE | 8 chapters / 504 paragraphs / 1,232 raw windows | 36 | section-level | section-level | `[Awakened Imagination]/curated_awakened_imagination.jsonl` |
| Freedom For All | COMPLETE | Intro + 9 chapters / 323 paragraphs / 841 raw windows | 32 | section-level | section-level | `[Freedom For All]/curated_freedom_for_all.jsonl` |
| He Breaks The Shell | TODO | — | — | — | — | — |
| I Know My Father | TODO | — | — | — | — | — |
| Out Of This World | TODO | — | — | — | — | — |
| Prayer, The Art Of Believing | TODO | — | — | — | — | — |
| Resurrection, A Confession Of Faith | TODO | — | — | — | — | — |
| Seedtime And Harvest | TODO | — | — | — | — | — |
| The Law And The Promise | TODO | — | — | — | — | — |
| The Power Of Awareness | TODO | — | — | — | — | — |
| The Search | TODO | — | — | — | — | — |
| Your Faith Is Your Fortune | TODO | — | — | — | — | — |

## 2026-08-31 — Feeling Is the Secret
Completed the first hard editorial pass.

Key decisions:
- enforced a substantially stricter pool than the earlier ACCEPT/REVIEW/REJECT pass;
- reduced 88 reviewed candidates to 29 SELECTs;
- moved mixed-scripture material to HOLD rather than treating it as Neville-only quotation text;
- dropped the categorical “all disease” medical claim;
- collapsed overlapping idea clusters to preferred formulations;
- retained core metaphysical quotations where they are clean, standalone, and recognizably Neville.

Files written in the work folder:
- `curated_feeling_is_the_secret.jsonl`
- `editorial_decisions_feeling_is_the_secret.jsonl`
- `editorial_review_feeling_is_the_secret.md`

Raw candidate and source files were not changed.

## 2026-08-31 — At Your Command
Completed a source-first hard editorial pass.

Why the method changed:
- the worker generated 711 candidate windows from only 110 canonical source paragraphs;
- 171 raw duplicate groups showed that candidate-by-candidate review would mostly review artificial sliding-window variants;
- `EDITORIAL_POLICY.md` was extended with `SOURCE_FIRST_CANONICAL` mode so overgenerated works can be reviewed against the canonical master text paragraph-by-paragraph.

Result:
- canonical paragraphs reviewed: 110 / 110;
- SELECT exact fragments: 20;
- HOLD paragraphs: 67;
- DROP paragraphs: 23;
- strict SELECT density vs 711 raw worker windows: 2.8%.

Notable filtering:
- scripture-dominant and parable-retelling passages were kept out of the main Neville-only pool;
- categorical medical-healing and financial-guarantee material was dropped from automatic delivery;
- victim-blaming formulations around accidents, interpersonal behavior, poverty, illness, or condemnation were dropped;
- problem-avoidance and very strong literal guarantees were held for context rather than selected;
- core metaphysical/self-concept material was retained when clean, exact, and memorable.

Files written in the work folder:
- `curated_at_your_command.jsonl`
- `editorial_decisions_at_your_command.jsonl`
- `editorial_review_at_your_command.md`
- `editorial_complete.json`

Raw candidate and source files were not changed.

## 2026-08-31 — Awakened Imagination
Completed a source-first hard editorial pass across the complete canonical 8-chapter book.

Why source-first remained appropriate:
- the worker retained 1,232 candidate windows from 504 canonical paragraphs;
- 182 duplicate groups showed heavy overlap among the extracted windows;
- chapter-level audit records preserve full canonical coverage without serializing hundreds of mechanical near-duplicates as separate editorial judgments.

Result:
- canonical chapters reviewed: 8 / 8;
- canonical paragraphs covered: 504 / 504;
- SELECT exact fragments: 36;
- strict SELECT density vs 1,232 retained worker candidates: 2.9%;
- strict SELECT density vs 504 canonical paragraphs: 7.1%.

Notable filtering:
- external quotations and pure scripture were excluded from Neville attribution;
- repeated `thinking of` / `thinking from` windows were collapsed to the strongest formulations;
- medical-healing, bilocation, financial, miracle, and universal-causation claims were held when context would be necessary;
- long autobiographical/testimonial passages were not used as standalone daily quotations;
- Chapter 8 was reserved for a future spiritual/scriptural opt-in layer rather than the main automatic pool.

Files written in the work folder:
- `curated_awakened_imagination.jsonl`
- `editorial_decisions_awakened_imagination.jsonl`
- `editorial_review_awakened_imagination.md`
- `editorial_complete.json`

Raw candidate and source files were not changed.

## 2026-08-31 — Freedom For All
Completed a source-first hard editorial pass across the complete canonical Introduction + 9 chapters.

Why source-first remained appropriate:
- the worker retained 841 candidate windows from 323 canonical paragraphs;
- 115 duplicate groups showed meaningful sliding-window overlap;
- section-level audit records preserve complete source coverage without treating mechanical overlaps as separate editorial objects.

Result:
- canonical paragraphs covered: 323 / 323;
- SELECT exact fragments: 32;
- strict SELECT density vs 841 retained worker candidates: 3.8%;
- strict SELECT density vs canonical paragraphs: 9.9%.

Notable filtering:
- pure scripture and scripture-dominant allegorical retellings were excluded from Neville attribution;
- core I AM, feeling, assumption, Sabbath, desire, and imaginal-listening formulations were retained;
- categorical healing, remote-healing, financial-guarantee, and universal-blame material was excluded from the automatic pool;
- long Noah, Jacob/Esau, crucifixion, leprosy, mustard-seed, and Immaculate Conception explanations were held where context is more important than standalone delivery;
- repeated formulations were collapsed to preferred local variants.

Files written in the work folder:
- `curated_freedom_for_all.jsonl`
- `editorial_decisions_freedom_for_all.jsonl`
- `editorial_review_freedom_for_all.md`
- `editorial_complete.json`

Raw candidate and source files were not changed.

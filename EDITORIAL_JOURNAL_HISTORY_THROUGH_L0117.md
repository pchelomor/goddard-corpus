# Editorial Journal — Neville Goddard Corpus

This is the current operational journal for the strict editorial layer defined in `EDITORIAL_POLICY.md`.

> Historical note: the detailed journal state through `L0107` is preserved verbatim in `EDITORIAL_JOURNAL_HISTORY_THROUGH_L0107.md` (same Git blob as the pre-repair journal). This compact journal supersedes stale queue-identity statements in that snapshot while preserving the full historical record.

## Decision vocabulary

- **SELECT** — main curated corpus / automatic daily-pool candidate.
- **HOLD** — valuable but contextual, spiritually specialized, sensitive, mixed-source, or otherwise unsuitable for automatic delivery without context.
- **DROP** — weak, duplicate, misbounded, external/scripture, generic, unsafe/misleading when isolated, or otherwise unsuitable for the curated layer.

## Mandatory workflow

The authoritative processing identity is `corpus_id` from the **current** `corpus_registry.json`, not a remembered title or an older queue note.

For overlapping worker extraction use `SOURCE_FIRST_CANONICAL`:

1. verify corpus identity and physical canonical object;
2. read the complete `master_text_*` from beginning to end;
3. review every canonical paragraph/section;
4. select only exact Neville wording with clean standalone boundaries;
5. create `curated_*`, `editorial_decisions_*`, `editorial_review_*`, and `editorial_complete.json`;
6. update this journal;
7. re-fetch the written files from GitHub before considering the item complete.

Raw `candidates_*`, `rejected_*`, `master_text_*`, source manifests/variations, worker reports, and `processing_complete.json` remain immutable during editorial review.

## B/S priority audit

| Corpus ID | Work | Status | Canonical coverage | SELECT |
|---|---|---:|---:|---:|
| B001 | At Your Command | COMPLETE | 110 paragraphs | 20 |
| B002 | Your Faith Is Your Fortune | COMPLETE | 1,046 paragraphs | 35 |
| B003 | Freedom For All | COMPLETE | 323 paragraphs | 32 |
| B004 | Feeling Is the Secret | COMPLETE | strict completed pass | 29 |
| B005 | Prayer, The Art Of Believing | COMPLETE | 192 paragraphs | 21 |
| B006 | The Search | COMPLETE | 43 paragraphs | 12 |
| B007 | Out Of This World | COMPLETE | 189 paragraphs | 20 |
| B008 | The Power Of Awareness (book) | **BLOCKED / UNFINISHED** | distinct canonical book master missing | — |
| B009 | Awakened Imagination | COMPLETE | 504 paragraphs | 36 |
| B010 | Seedtime And Harvest | COMPLETE | 360 paragraphs | 23 |
| B011 | The Law And The Promise | COMPLETE | 798 paragraphs | 34 |
| B012 | I Know My Father | COMPLETE | 177 paragraphs | 17 |
| B013 | Resurrection, A Confession Of Faith | COMPLETE | 168 paragraphs | 0 |
| B014 | He Breaks The Shell | COMPLETE | 98 paragraphs | 0 |
| S001 | Five Lessons (Master Class) | COMPLETE | 6 sections / 858 paragraphs | 19 |
| S002 | The KECA Radio Talks | COMPLETE | 9 broadcasts / 107 paragraphs | 22 |
| S003 | The Creative Use Of Imagination | COMPLETE | 271 paragraphs | 20 |

`B008` remains isolated from same-title lecture `L0185`; the lecture package must not be relabeled as the book.

## Lecture editorial progress

All ranges below were completed under `SOURCE_FIRST_CANONICAL` unless an identity-repair note says otherwise.

| Corpus range | Status | Final SELECT | Note |
|---|---:|---:|---|
| L0001–L0005 | COMPLETE | 8 | five-lecture batch |
| L0006–L0010 | COMPLETE | 8 | five-lecture batch |
| L0011–L0015 | COMPLETE | 10 | includes restored dated L0011 object |
| L0016–L0020 | COMPLETE | 7 | includes reprint/lecture identity overlays |
| L0021–L0025 | COMPLETE | 6 | five-lecture batch |
| L0026–L0030 | COMPLETE | 11 | five-lecture batch |
| L0031–L0035 | COMPLETE | 12 | includes one long single-paragraph master |
| L0036–L0040 | COMPLETE | 2 | four intentional zero-SELECT works |
| L0041–L0045 | COMPLETE | 11 | five-lecture batch |
| L0046–L0050 | COMPLETE | 8 | five-lecture batch |
| L0051–L0055 | COMPLETE | 5 | five-lecture batch |
| L0056–L0060 | COMPLETE | 7 | five-lecture batch |
| L0061–L0065 | COMPLETE | 9 | five-lecture batch |
| L0066–L0070 | COMPLETE | 3 | five-lecture batch |
| L0071–L0075 | COMPLETE | 1 | five-lecture batch |
| L0076–L0085 | COMPLETE | 3 | ten-lecture batch |
| L0086–L0095 | COMPLETE | 6 | ten-lecture batch |
| L0096–L0105 | **COMPLETE after identity repair** | 0 | L0105 is `Love Endureth`, not stale `Live In The End` |
| L0106 | COMPLETE | 8 | Mental Diets |
| L0107 | COMPLETE | 0 | Moses – Elijah – Jesus |
| L0108–L0117 | COMPLETE | 5 | current ten-lecture batch |

Detailed historical filtering notes through L0107 remain in `EDITORIAL_JOURNAL_HISTORY_THROUGH_L0107.md`; current and future work is recorded below.

## 2026-09-02 — L0105 identity correction and completion

A post-audit registry check exposed a real queue-identity defect in the previous journal.

The stale journal/ISS-008 mapped `L0105` to *Live In The End* and called the item `BLOCKED / MISSING_CANONICAL_OBJECT`. The current authoritative `corpus_registry.json` instead maps `L0105` to **Love Endureth**, dated **1959-11-13**. The physical `[Love Endureth]` folder exists and its raw report/processing metadata also identify `corpus_id: L0105`.

`L0105 Love Endureth` was therefore reviewed end-to-end rather than left blocked:

- authoritative source: `[Love Endureth]/master_text_love_endureth.txt`;
- canonical source SHA: `23c4176a987eb9f2ffd1e633e680d506f525f142`;
- canonical paragraphs: **27 / 27**;
- worker windows generated: **372**;
- retained worker windows: **357** (`285` candidate + `72` review-recommended);
- worker rejected: **15**;
- raw duplicate groups: **24**;
- final SELECT: **0**, intentionally.

The lecture is predominantly love/Promise theology, scripture-adjacent wording, literal mystical fulfillment and abundance/direct-response claims. Generic love aphorisms were not admitted merely to create density.

Files written:
- `[Love Endureth]/curated_love_endureth.jsonl` (intentionally empty)
- `[Love Endureth]/editorial_decisions_love_endureth.jsonl`
- `[Love Endureth]/editorial_review_love_endureth.md`
- `[Love Endureth]/editorial_complete.json`

`corpus_issues.md` ISS-008 has been corrected to record the identity drift and its resolution. The raw registry/extraction files were not rewritten by the editorial pass.

Corrected totals for `L0096–L0105` are now:

- canonical paragraphs reviewed: **1,130 / 1,130**;
- worker windows generated: **6,541**;
- retained worker windows: **6,396**;
- worker rejected windows: **145**;
- raw duplicate groups: **812**;
- final new SELECT: **0**.

## 2026-09-02 — L0106 Mental Diets

- canonical coverage: **50 / 50 paragraphs**;
- worker windows generated / retained / rejected: **342 / 331 / 11**;
- duplicate groups: **39**;
- SELECT: **8**.

The shortlist keeps clean Neville-only formulations on inner conversation, assumption, self-concept and active imaginal participation. Employer-causation, victim-blaming, categorical health/wealth effects, pseudo-scientific certainty and guaranteed externalization were excluded.

Files:
- `[Mental Diets]/curated_mental_diets.jsonl`
- `[Mental Diets]/editorial_decisions_mental_diets.jsonl`
- `[Mental Diets]/editorial_review_mental_diets.md`
- `[Mental Diets]/editorial_complete.json`

## 2026-09-02 — L0107 Moses – Elijah – Jesus

- canonical coverage: **40 / 40 paragraphs**;
- worker windows generated / retained / rejected: **549 / 531 / 18**;
- duplicate groups: **35**;
- SELECT: **0**, intentionally.

The lecture is overwhelmingly Moses/Elijah/Jesus state theology, I-AM exegesis, Promise/Christology, mystical testimony, serpent/transfiguration/divine-light material and strong supernatural claims. No safe distinctive main-pool boundary justified selection.

Files:
- `[Moses – Elijah – Jesus]/curated_moses_elijah_jesus.jsonl` (intentionally empty)
- `[Moses – Elijah – Jesus]/editorial_decisions_moses_elijah_jesus.jsonl`
- `[Moses – Elijah – Jesus]/editorial_review_moses_elijah_jesus.md`
- `[Moses – Elijah – Jesus]/editorial_complete.json`

## 2026-09-02 — Lecture batch L0108–L0117

Completed ten corpus IDs under `SOURCE_FIRST_CANONICAL`.

| Corpus ID | Work | Canonical paragraphs | Retained worker windows | SELECT |
|---|---|---:|---:|---:|
| L0108 | My Word | 19 / 19 | 291 | 0 |
| L0109 | Neville’s Purpose Revealed | 131 / 131 | 668 | 1 |
| L0110 | No Other Foundation 10-10-1969 | 46 / 46 | 347 | 0 |
| L0111 | No Other Foundation 11-4-1968 | 40 / 40 | 385 | 0 |
| L0112 | No Other God | 35 / 35 | 355 | 1 |
| L0113 | North Of The Strip | 32 / 32 | 462 | 0 |
| L0114 | Occupant Or Inmate | 32 / 32 | 428 | 2 |
| L0115 | One Thousand Two Hundred Sixty Days | 35 / 35 | 359 | 0 |
| L0116 | Paul’s Autobiography | 31 / 31 | 433 | 0 |
| L0117 | Perception | 26 / 26 | 218 | 1 |

Batch result:

- canonical paragraphs reviewed: **427 / 427**;
- worker windows generated: **4,053**;
- retained worker windows: **3,946**;
- worker rejected windows: **107**;
- raw duplicate groups: **317**;
- final SELECT fragments: **5**.

Selected boundaries:

- `L0109`: `In your dreams dare to assume that you are the man that you want to be.`
- `L0112`: `Search for and find the feeling that would be yours if things were as you desire them to be.`
- `L0114`: `Every state, regardless of what it is, is waiting for occupancy.`
- `L0114`: `And the state to which you most constantly return constitutes your dwelling place.`
- `L0117`: `You can reproduce and duplicate any perception you have ever encountered, in your imagination.`

Notable filtering:

- `L0108` intentionally 0 SELECT: Pattern-Man/Promise theology, deterministic violence roles, health/wealth guarantees.
- `L0109` keeps one desired-self assumption sentence; adjacent harden-into-fact and bridge guarantees are excluded.
- `L0110` intentionally 0 SELECT: dream metaphysics, Promise, universal causation, violence-role framing; revision language is a weaker cross-work duplicate.
- `L0111` intentionally 0 SELECT: externalization/compulsion of other people and guarantees; safer slogans are too generic.
- `L0112` keeps one fulfilled-feeling instruction; pig/tree symbolism, Promise theology and no-consent alteration of others are excluded.
- `L0113` intentionally 0 SELECT: property/financial proof, medical healing-at-distance, gambling success, direct-other alteration and universal causation.
- `L0114` keeps two distinctive states formulations; victim-blaming, universal causation and repeated direct-other revision are excluded.
- `L0115` intentionally 0 SELECT: literal 1,260-day Promise chronology, mystical birth/David/serpent/transfiguration and spiritual-identity claims.
- `L0116` intentionally 0 SELECT: Pauline exegesis, Christ/imagination theology and direct-other imagining.
- `L0117` keeps one sensory-imagination sentence; Blake wording, categorical objectification, direct-other control and reason-denigration are excluded.

### L0115 date/provenance discrepancy

`corpus_registry.json` is internally inconsistent for `L0115`: `year`/`date` and the source manifest identify **1968-09-13**, while `full_date` is **1963-01-01**. The editorial layer records the discrepancy and uses the canonical source-manifest/repository date **1968-09-13** without rewriting raw registry metadata.

All ten works have `curated_*`, `editorial_decisions_*`, `editorial_review_*`, and corpus-ID-matching `editorial_complete.json` packages. Raw extraction/source files were not modified.

## Current queue

- `B008` remains blocked pending a distinct canonical *The Power of Awareness* book object.
- Lecture queue is complete through **L0117**.
- Next lecture corpus item: **L0118 — Persistent Assumption**.

Before advancing, completion must always be verified by re-fetching the package from GitHub, not by trusting a prior chat statement or stale journal title mapping.

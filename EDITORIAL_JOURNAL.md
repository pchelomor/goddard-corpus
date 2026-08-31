# Editorial Journal — Neville Goddard Corpus

This journal tracks the strict work-by-work review defined in `EDITORIAL_POLICY.md`. Raw extraction/source files remain immutable; the editorial layer is derivative and is complete only when the four required work files exist and the work is recorded here.

## Decision vocabulary
- **SELECT** — main curated corpus / automatic daily-pool candidate.
- **HOLD** — valuable but contextual, sensitive, mixed-source, spiritually specialized, or otherwise unsuitable for automatic delivery without context.
- **DROP** — weak, duplicate, misbounded, mostly external/scripture/testimonial, generic, unsafe/misleading when isolated, or otherwise unsuitable for the curated layer.

## Mandatory processing order

The authoritative priority is by `corpus_id` in `corpus_registry.json`, never by title alone:

1. finish every canonical `B001`–`B014` and `S001`–`S003` item;
2. only after all 17 are editorially complete, continue unfinished `L*` lectures in corpus order;
3. same-title books and lectures are separate corpus objects and must not share an editorial identity merely because their folder/title text matches;
4. when worker extraction contains overlapping/sliding windows, use `SOURCE_FIRST_CANONICAL`: review the complete canonical master from beginning to end and treat worker windows as discovery/provenance rather than independent editorial units.

## B/S priority audit

| Corpus ID | Work | Status | Canonical coverage | SELECT | Output / note |
|---|---|---:|---:|---:|---|
| B001 | Feeling Is the Secret | COMPLETE | strict completed pass | 29 | `Feeling Is the Secret/curated_feeling_is_the_secret.jsonl` |
| B002 | Your Faith Is Your Fortune | COMPLETE | 1,046 paragraphs / 2,279 worker candidates | 35 | `[Your Faith Is Your Fortune]/curated_your_faith_is_your_fortune.jsonl` |
| B003 | Freedom For All | COMPLETE | 323 paragraphs / 841 worker candidates | 32 | `[Freedom For All]/curated_freedom_for_all.jsonl` |
| B004 | Prayer, The Art Of Believing | COMPLETE | 192 paragraphs / 700 worker candidates | 21 | `[Prayer, The Art Of Believing]/curated_prayer_the_art_of_believing.jsonl` |
| B005 | At Your Command | COMPLETE | 110 paragraphs / 711 worker candidates | 20 | `[At Your Command]/curated_at_your_command.jsonl` |
| B006 | The Search | COMPLETE | 43 paragraphs / 150 worker candidates | 12 | `[The Search]/curated_the_search.jsonl` |
| B007 | Out Of This World | COMPLETE | 189 paragraphs / 493 worker candidates | 20 | `[Out Of This World]/curated_out_of_this_world.jsonl` |
| B008 | The Power Of Awareness (book) | **BLOCKED / UNFINISHED** | canonical book `master_text_*` not present as a distinct book object | — | same-title collision with `L0185`; see issue note below |
| B009 | Awakened Imagination | COMPLETE | 504 paragraphs / 1,232 worker candidates | 36 | `[Awakened Imagination]/curated_awakened_imagination.jsonl` |
| B010 | Seedtime And Harvest | COMPLETE | 360 paragraphs / 1,145 worker candidates | 23 | `[Seedtime And Harvest]/curated_seedtime_and_harvest.jsonl` |
| B011 | The Law And The Promise | COMPLETE | 798 paragraphs / 3,036 worker candidates | 34 | `[The Law And The Promise]/curated_the_law_and_the_promise.jsonl` |
| B012 | I Know My Father | COMPLETE | 177 paragraphs / 892 worker candidates | 17 | `[I Know My Father]/curated_i_know_my_father.jsonl` |
| B013 | Resurrection, A Confession Of Faith | COMPLETE | 168 paragraphs / 457 worker candidates | 0 | intentional empty main-pool shortlist |
| B014 | He Breaks The Shell | COMPLETE | 98 paragraphs / 188 worker candidates | 0 | intentional empty main-pool shortlist |
| S001 | Five Lessons (Master Class) | COMPLETE | 6 sections / 858 paragraphs / 4,516 retained windows | 19 | `[Five Lessons]/curated_five_lessons.jsonl` |
| S002 | The KECA Radio Talks | COMPLETE | 107 paragraphs / 1,771 worker candidates | 27 | `[The KECA Radio Talks]/curated_keca_radio_talks.jsonl` |
| S003 | The Creative Use Of Imagination | COMPLETE | 271 paragraphs / 2,923 worker candidates | 20 | `[The Creative Use Of Imagination]/curated_the_creative_use_of_imagination.jsonl` |

**Current gate:** `B008` is the only unfinished B/S priority object. No additional `L*` lecture should be processed until B008 is repaired and receives its own verified four-file editorial package.

## Repository-wide queue

`corpus_progress.json` reports an extraction-complete corpus of 252 items: 14 core books, 3 supplementary works, and 235 canonical lectures. Extraction completeness is not equivalent to editorial completeness.

A work leaves the editorial queue only after all of the following are true:
- the correct corpus identity is verified against `corpus_registry.json`;
- the complete authoritative canonical source has been reviewed;
- `curated_<slug>.jsonl` exists;
- `editorial_decisions_<slug>.jsonl` exists;
- `editorial_review_<slug>.md` exists;
- `editorial_complete.json` exists and identifies the correct `corpus_id`;
- this journal is updated;
- the written files are re-fetched/verified in GitHub.

## Global editorial rules retained from completed passes

Across the corpus, strict review continues to enforce these rules:
- preserve exact Neville wording for SELECT fragments; do not manufacture aphorisms by joining non-contiguous sentences;
- exclude pure scripture and quotations from Blake, Shakespeare, Jung, Yeats, Shelley, Rossetti, Tennyson, Angelus Silesius/Scheffler, correspondents, testimonials, editors, and other external voices from Neville attribution;
- collapse overlapping worker windows and weaker local duplicates to the strongest canonical formulation;
- keep categorical medical or mental-health claims, discouragement of appropriate medical care, financial guarantees, guaranteed physical outcomes, gambling-success material, victim-blaming/event-causation formulations, covert influence/control claims, and misleading pseudo-scientific literal claims out of the automatic pool;
- use HOLD for Promise material, mystical experiences, strong theological identity claims, dimensional/literal metaphysical claims, and other context-dependent content that remains valuable for an opt-in contextual layer;
- no quota is imposed: a historically important work may legitimately produce zero SELECT fragments.

## 2026-08-31 — Historical completed core passes

The following core/supplementary passes were completed under the strict policy before the current priority audit and retain their existing four-file editorial packages:

- `B001` Feeling Is the Secret — 29 SELECT; mixed scripture and categorical medical material excluded from the automatic pool.
- `B002` Your Faith Is Your Fortune — 35 SELECT from 1,046 canonical paragraphs; full `SOURCE_FIRST_CANONICAL` package verified.
- `B003` Freedom For All — 32 SELECT from 323 canonical paragraphs; scripture-dominant allegory and categorical healing/financial/universal-blame material excluded or held.
- `B004` Prayer, The Art Of Believing — 21 SELECT from 192 canonical paragraphs; telepathy/hypnosis/control, categorical cure claims, pseudo-scientific and victim-blaming material excluded or held.
- `B005` At Your Command — 20 SELECT from 110 canonical paragraphs; 711 overlapping worker windows collapsed source-first.
- `B006` The Search — 12 SELECT from 43 canonical paragraphs; completed package exists even though an older journal table previously still showed TODO.
- `B007` Out Of This World — 20 SELECT from 189 canonical paragraphs; literal fourth-dimensional/precognition/bilocation claims and control-of-others material held or excluded.
- `B009` Awakened Imagination — 36 SELECT from 504 canonical paragraphs; chapter 8 Promise/spiritual material reserved for contextual use.
- `B010` Seedtime And Harvest — 23 SELECT from 360 canonical paragraphs; external quotations, healing stories, event-causation/victim-blaming and direct-control material excluded or held.
- `B011` The Law And The Promise — 34 SELECT from 798 canonical paragraphs; letters/testimonials were not attributed to Neville; gambling, medical cure, disaster/war/death causation and direct influence material kept out of the main pool.
- `B012` I Know My Father — 17 SELECT from 177 canonical paragraphs; medical, financial, political/war, blame and unsafe sensory-evidence-denial formulations excluded or held.
- `B013` Resurrection, A Confession Of Faith — 0 SELECT intentionally; Promise/theological material retained contextually and external/scripture wording excluded from Neville attribution.
- `B014` He Breaks The Shell — 0 SELECT intentionally; Promise material retained for an opt-in spiritual layer.
- `S001` Five Lessons (Master Class) — 19 SELECT after a complete six-section / 858-paragraph source-first reread; a provisional larger shortlist was reduced and the embedded self-reprint from `The Search` was not duplicated.
- `S002` The KECA Radio Talks — 27 SELECT from 107 canonical paragraphs; complete source-first package exists.

Raw candidate, rejected, master-text, manifest, variation, worker-report, and processing files for these completed works were not changed by editorial review.

## 2026-08-31 — Earlier lecture batch L0001–L0005

A five-lecture batch had already been completed before the present corpus-ID priority gate was made explicit:

| Corpus ID | Work | Canonical paragraphs | Retained worker windows | SELECT |
|---|---|---:|---:|---:|
| L0001 | A Divine Event | 33 / 33 | 398 | 1 |
| L0002 | A Lesson In Scripture | 27 / 27 | 399 | 2 |
| L0003 | A Movement Of Mind | 26 / 26 | 266 | 2 |
| L0004 | A Movement Within God | 31 / 31 | 398 | 2 |
| L0005 | A Parabolic Revelation | 35 / 35 | 403 | 1 |

These packages remain valid, but **no further L* work is authorized until B008 is complete**. The batch filtered Promise/theological material to HOLD where context was required, excluded pure scripture/external quotations, and kept categorical health/financial/political/war/control/universal-causation/victim-blaming formulations out of the main pool.

## 2026-08-31 — L0185 same-title lecture identity

The top-level folder `[The Power Of Awareness]` is already editorially complete, but its `editorial_complete.json` identifies it as **`L0185`**, a distinct 1953 spoken lecture, not book `B008`.

L0185 result:
- 32 canonical paragraphs reviewed end-to-end;
- 375 retained worker windows collapsed source-first;
- 12 SELECT fragments;
- Christological symbolism, strong sensory-evidence-denial, dimensional claims, direct influence and victim-blaming formulations held or excluded under the strict policy.

The L0185 files must not be overwritten or relabeled as B008.

## 2026-08-31 — B008 blocking identity/source issue

`corpus_issues.md` explicitly records the distinction between the 1952 book *The Power of Awareness* and the same-title lecture. Repository inspection confirms the collision is real:

- `[The Power Of Awareness]/editorial_complete.json` = `L0185`, not `B008`;
- the folder's `master_text_the_power_of_awareness.txt` is the short lecture transcript, not the ~20k-word book;
- root `scratch_poa_rn.txt` is also the RealNeville lecture source;
- root `scratch_poa_mynev.txt` contains a modern MyNeville webpage wrapper with the 1952 book body embedded inside it (foreword + chapters 1–27), but it is a scratch/raw web capture, not a distinct canonical B008 `master_text_*` object;
- no separate B008 canonical folder/master was found in the current repository tree/search.

Therefore B008 is **not being falsely marked COMPLETE**. The next B008 work must first recover/establish an unambiguous canonical book source without modifying the raw scratch capture, then perform a complete source-first book review and write a B008-specific four-file package. Until that happens, the B/S priority gate remains closed.

## 2026-08-31 — S003 The Creative Use Of Imagination

Completed/verified the strict supplementary editorial package for `S003`.

Identity and method:
- `corpus_id`: `S003`;
- `work_class`: `EDITED_COLLECTION`;
- review mode: `SOURCE_FIRST_CANONICAL`;
- attribution status: `EDITORIALLY_MEDIATED`, consistent with the repository issue noting posthumous editorial smoothing/merging in this collection.

Result:
- canonical source paragraphs reviewed: **271 / 271**;
- raw worker candidates collapsed through source-first review: **2,923**;
- raw duplicate groups: **245**;
- final main-pool SELECT fragments: **20**.

Notable filtering:
- editor preface/testimonial wording, pure scripture and external quotations were excluded from Neville attribution;
- edited-collection attribution uncertainty, scripture-centered interpretation, spiritual identity claims and stronger universal-causation/metaphysical passages were held where context was necessary;
- categorical medical claims, discouragement of medical reliance, financial guarantees, victim-blaming/event-causation, direct control of others, misleading scientific claims, weak/context-dependent fragments and weaker duplicates were kept out of the automatic pool.

Files verified/written in `[The Creative Use Of Imagination]`:
- `curated_the_creative_use_of_imagination.jsonl`
- `editorial_decisions_the_creative_use_of_imagination.jsonl`
- `editorial_review_the_creative_use_of_imagination.md`
- `editorial_complete.json`

Raw candidate, rejected, master-text, manifest, variation, worker-report, and processing files were not changed.

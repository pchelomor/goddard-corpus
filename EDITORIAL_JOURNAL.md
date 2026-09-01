# Editorial Journal — Neville Goddard Corpus

This journal tracks the strict work-by-work review defined in `EDITORIAL_POLICY.md`. Raw extraction/source files remain immutable; the editorial layer is derivative and is complete only when the four required work files exist and the work is recorded here.

## Decision vocabulary
- **SELECT** — main curated corpus / automatic daily-pool candidate.
- **HOLD** — valuable but contextual, sensitive, mixed-source, spiritually specialized, or otherwise unsuitable for automatic delivery without context.
- **DROP** — weak, duplicate, misbounded, mostly external/scripture/testimonial, generic, unsafe/misleading when isolated, or otherwise unsuitable for the curated layer.

## Mandatory processing order

The authoritative priority is by `corpus_id` in `corpus_registry.json`, never by title alone:

1. finish every canonical `B001`–`B014` and `S001`–`S003` item;
2. continue unfinished `L*` lectures in corpus order when directed by the user;
3. same-title books and lectures are separate corpus objects and must not share an editorial identity merely because their folder/title text matches;
4. when worker extraction contains overlapping/sliding windows, use `SOURCE_FIRST_CANONICAL`: review the complete canonical master from beginning to end and treat worker windows as discovery/provenance rather than independent editorial units.

## B/S priority audit

| Corpus ID | Work | Status | Canonical coverage | SELECT | Output / note |
|---|---|---:|---:|---:|---|
| B001 | At Your Command | COMPLETE | 110 paragraphs / 711 worker candidates | 20 | `[At Your Command]/curated_at_your_command.jsonl` |
| B002 | Your Faith Is Your Fortune | COMPLETE | 1,046 paragraphs / 2,279 worker candidates | 35 | `[Your Faith Is Your Fortune]/curated_your_faith_is_your_fortune.jsonl` |
| B003 | Freedom For All | COMPLETE | 323 paragraphs / 841 worker candidates | 32 | `[Freedom For All]/curated_freedom_for_all.jsonl` |
| B004 | Feeling Is the Secret | COMPLETE | strict completed pass | 29 | `Feeling Is the Secret/curated_feeling_is_the_secret.jsonl` |
| B005 | Prayer, The Art Of Believing | COMPLETE | 192 paragraphs / 700 worker candidates | 21 | `[Prayer, The Art Of Believing]/curated_prayer_the_art_of_believing.jsonl` |
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
| S002 | The KECA Radio Talks | COMPLETE | 9 broadcasts / 107 paragraphs / 1,771 retained windows | 22 | `[The KECA Radio Talks]/curated_keca_radio_talks.jsonl` |
| S003 | The Creative Use Of Imagination | COMPLETE | 271 paragraphs / 2,923 worker candidates | 20 | `[The Creative Use Of Imagination]/curated_the_creative_use_of_imagination.jsonl` |
**B008 status:** `B008` remains the only unfinished B/S priority object because its distinct canonical book master is missing. By explicit user direction, the lecture editorial queue continues in corpus order while B008 remains isolated and must not be conflated with `L0185`.

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

- `B001` At Your Command — 20 SELECT from 110 canonical paragraphs; 711 overlapping worker windows collapsed source-first.
- `B002` Your Faith Is Your Fortune — 35 SELECT from 1,046 canonical paragraphs; full `SOURCE_FIRST_CANONICAL` package verified.
- `B003` Freedom For All — 32 SELECT from 323 canonical paragraphs; scripture-dominant allegory and categorical healing/financial/universal-blame material excluded or held.
- `B004` Feeling Is the Secret — 29 SELECT; mixed scripture and categorical medical material excluded from the automatic pool.
- `B005` Prayer, The Art Of Believing — 21 SELECT from 192 canonical paragraphs; telepathy/hypnosis/control, categorical cure claims, pseudo-scientific and victim-blaming material excluded or held.
- `B006` The Search — 12 SELECT from 43 canonical paragraphs; completed package exists even though an older journal table previously still showed TODO.
- `B007` Out Of This World — 20 SELECT from 189 canonical paragraphs; literal fourth-dimensional/precognition/bilocation claims and control-of-others material held or excluded.
- `B009` Awakened Imagination — 36 SELECT from 504 canonical paragraphs; chapter 8 Promise/spiritual material reserved for contextual use.
- `B010` Seedtime And Harvest — 23 SELECT from 360 canonical paragraphs; external quotations, healing stories, event-causation/victim-blaming and direct-control material excluded or held.
- `B011` The Law And The Promise — 34 SELECT from 798 canonical paragraphs; letters/testimonials were not attributed to Neville; gambling, medical cure, disaster/war/death causation and direct influence material kept out of the main pool.
- `B012` I Know My Father — 17 SELECT from 177 canonical paragraphs; medical, financial, political/war, blame and unsafe sensory-evidence-denial formulations excluded or held.
- `B013` Resurrection, A Confession Of Faith — 0 SELECT intentionally; Promise/theological material retained contextually and external/scripture wording excluded from Neville attribution.
- `B014` He Breaks The Shell — 0 SELECT intentionally; Promise material retained for an opt-in spiritual layer.
- `S001` Five Lessons (Master Class) — 19 SELECT after a complete six-section / 858-paragraph source-first reread; a provisional larger shortlist was reduced and the embedded self-reprint from `The Search` was not duplicated.
- `S002` The KECA Radio Talks — 22 SELECT after a complete nine-broadcast / 107-paragraph source-first reread; the provisional 27-fragment shortlist was tightened and the audit was upgraded to broadcast-level decisions.
Raw candidate, rejected, master-text, manifest, variation, worker-report, and processing files for these completed works were not changed by editorial review.

## 2026-08-31 — Earlier lecture batch L0001–L0005

A five-lecture batch was completed source-first:

| Corpus ID | Work | Canonical paragraphs | Retained worker windows | SELECT |
|---|---|---:|---:|---:|
| L0001 | A Divine Event | 33 / 33 | 398 | 1 |
| L0002 | A Lesson In Scripture | 27 / 27 | 399 | 2 |
| L0003 | A Movement Of Mind | 26 / 26 | 266 | 2 |
| L0004 | A Movement Within God | 31 / 31 | 398 | 2 |
| L0005 | A Parabolic Revelation | 35 / 35 | 403 | 1 |

These packages remain valid. The earlier pause on further `L*` work has been superseded by explicit user direction to continue the lecture queue in corpus order while `B008` remains blocked and untouched. The batch filtered Promise/theological material to HOLD where context was required, excluded pure scripture/external quotations, and kept categorical health/financial/political/war/control/universal-causation/victim-blaming formulations out of the main pool.

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

Therefore B008 is **not being falsely marked COMPLETE**. A future B008 repair must recover/establish an unambiguous canonical book source without modifying the raw scratch capture, then perform a complete source-first book review and write a B008-specific four-file package. This issue does not authorize relabeling or overwriting the existing L0185 lecture package.

## 2026-08-31 — S002 The KECA Radio Talks

Re-reviewed and finalized the strict supplementary editorial package for `S002` rather than relying on the pre-existing provisional `complete` marker.

Identity and method:
- `corpus_id`: `S002`;
- registry work class: `RADIO_TALK`;
- canonical registry year: `1951`;
- review mode: `SOURCE_FIRST_CANONICAL`;
- authoritative source: `[The KECA Radio Talks]/master_text_keca_radio_talks.txt`;
- canonical structure: **9 broadcasts**, **107 paragraphs**.

Result:
- canonical broadcasts reviewed: **9 / 9**;
- canonical paragraphs reviewed: **107 / 107**;
- worker windows generated: **1,793**;
- retained worker windows: **1,771** (`1,384` candidate + `387` review-recommended);
- worker rejected windows: **22**;
- raw duplicate groups: **80**;
- final main-pool SELECT fragments: **22**;
- provisional shortlist reduced from **27 → 22**;
- decisions upgraded from one coarse whole-series record to an audit summary plus **9 broadcast-level records**.

Notable filtering:
- pure scripture and external wording from Millikan, Yeats, Blake, Browning, Emerson, Keats and other quoted voices were excluded from Neville attribution;
- the Millikan income affirmation was treated as external wording, not a Neville quote;
- categorical health/healing causation, financial guarantees, guaranteed physical outcomes, unverified university/scientific claims, direct influence/control of another person, victim-blaming/event-causation, deterministic/no-action claims and misleading absolutes were kept out of the automatic pool;
- weak generic slogans such as `Don't blame; only resolve`, `Love is our birthright`, and `Love is the fundamental necessity of our life` were removed under the author-specificity threshold;
- Broadcast 7, *Stone, Water or Wine?*, intentionally produced **0 SELECT** because its value is predominantly scripture-symbolic and contextual;
- stronger missed canonical fragments on answered prayer, attention, imagination and self-concept were added where they had clean standalone boundaries.

Date/provenance note:
- `corpus_registry.json` records 1951 and the alternate title `9 Radio Talks delivered in Los Angeles (1951)`;
- the source manifest/report also contain July 1953 dating language and a July 1951 / July 1953 source-tradition note;
- editorial metadata preserves the canonical registry year `1951` and records the discrepancy instead of silently rewriting source metadata.

Files written and verified in `[The KECA Radio Talks]`:
- `curated_keca_radio_talks.jsonl`
- `editorial_decisions_keca_radio_talks.jsonl`
- `editorial_review_keca_radio_talks.md`
- `editorial_complete.json`

Raw candidate, rejected, master-text, manifest, variation, worker-report, and processing files were not changed.

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

## 2026-08-31 — Lecture batch L0006–L0010

Completed a five-lecture `SOURCE_FIRST_CANONICAL` editorial batch at the user's explicit direction, continuing the lecture list after the already completed `L0001–L0005` batch.

| Corpus ID | Work | Canonical paragraphs | Retained worker windows | SELECT |
|---|---|---:|---:|---:|
| L0006 | A Prophecy | 49 / 49 | 383 | 2 |
| L0007 | A Riddle | 33 / 33 | 411 | 0 |
| L0008 | A State Called Moses | 26 / 26 | 383 | 1 |
| L0009 | All That Is Divine | 38 / 38 | 445 | 1 |
| L0010 | All That You Behold | 40 / 40 | 449 | 4 |

Batch result:
- canonical paragraphs reviewed: **186 / 186**;
- worker windows generated: **2,109**;
- retained worker windows: **2,071**;
- worker rejected windows: **38**;
- raw duplicate groups: **166**;
- final main-pool SELECT fragments: **8**;
- all five works now contain `curated_*`, `editorial_decisions_*`, `editorial_review_*`, and `editorial_complete.json` and were re-fetched from GitHub after writing.

Notable filtering across the batch:
- `A Riddle` intentionally produced **0 SELECT** because its value is overwhelmingly Promise/Christology/mystical context; the empty curated file is deliberate;
- Blake and other external quotations plus pure scripture were excluded from Neville attribution;
- Promise, Christmas/rebirth, Davidic fatherhood, mystical serpent/dove/body symbolism, spiritual identity and salvation-history claims were generally held for contextual/opt-in use;
- categorical medical or health claims, passages discouraging medical authority, financial guarantees, guaranteed physical outcomes, direct control of others, and victim-blaming/event-causation material were excluded from the automatic pool;
- claims that another person must conform to one's imaginal representation were excluded;
- the `All That You Behold` story assigning a woman's death/disaster to her fear was explicitly kept out of the automatic pool;
- practical assumption, state, attention, conviction, and fulfilled-desire fragments were retained only where they had clean standalone boundaries without the stronger guarantees around them.

Files written and verified:
- `[A Prophecy]/curated_a_prophecy.jsonl`
- `[A Prophecy]/editorial_decisions_a_prophecy.jsonl`
- `[A Prophecy]/editorial_review_a_prophecy.md`
- `[A Prophecy]/editorial_complete.json`
- `[A Riddle]/curated_a_riddle.jsonl` (intentionally empty)
- `[A Riddle]/editorial_decisions_a_riddle.jsonl`
- `[A Riddle]/editorial_review_a_riddle.md`
- `[A Riddle]/editorial_complete.json`
- `[A State Called Moses]/curated_a_state_called_moses.jsonl`
- `[A State Called Moses]/editorial_decisions_a_state_called_moses.jsonl`
- `[A State Called Moses]/editorial_review_a_state_called_moses.md`
- `[A State Called Moses]/editorial_complete.json`
- `[All That Is Divine]/curated_all_that_is_divine.jsonl`
- `[All That Is Divine]/editorial_decisions_all_that_is_divine.jsonl`
- `[All That Is Divine]/editorial_review_all_that_is_divine.md`
- `[All That Is Divine]/editorial_complete.json`
- `[All That You Behold]/curated_all_that_you_behold.jsonl`
- `[All That You Behold]/editorial_decisions_all_that_you_behold.jsonl`
- `[All That You Behold]/editorial_review_all_that_you_behold.md`
- `[All That You Behold]/editorial_complete.json`

Raw candidate, rejected, master-text, manifest, variation, worker-report, and processing files were not changed.
## 2026-08-31 — Lecture batch L0011–L0015

Completed the next five corpus IDs under `SOURCE_FIRST_CANONICAL`, including recovery of the missing same-title `L0011` object.

| Corpus ID | Work | Canonical paragraphs | Retained worker windows | SELECT |
|---|---|---:|---:|---:|
| L0011 | All Things Are Possible (1967-11-03) | 32 / 32 | n/a — recovered canonical item | 0 |
| L0012 | All Things Are Possible (1969-05-12) | 35 / 35 | 462 | 4 |
| L0013 | All Things Exist | 38 / 38 | 259 | 3 |
| L0014 | An Assured Understanding | 35 / 35 | 375 | 0 |
| L0015 | An Inner Conviction | 29 / 29 | 329 | 3 |

Batch result:
- canonical paragraphs reviewed: **169 / 169**;
- known worker windows generated for L0012-L0015: **1,451**;
- retained worker windows for L0012-L0015: **1,425**;
- worker rejected windows for L0012-L0015: **26**;
- raw duplicate groups for L0012-L0015: **118**;
- final main-pool SELECT fragments: **10**;
- `L0011` intentionally produced **0 SELECT** because the recovered 1967 lecture is overwhelmingly Promise/Christology and its law-oriented ending depends on strong guaranteed-outcome language.

Identity/source repair:
- `L0011` and `L0012` are distinct same-title lectures, not duplicates;
- the repository had lost the separate L0011 physical object through a title/metadata collision;
- L0011 was restored under `[All Things Are Possible – 11-03-1967]` with a dated canonical master and editorial package;
- `corpus_registry.json` was normalized so L0011 now uses `1967-11-03` and the 1967 source, while L0012 uses `1969-05-12` and the separate 1969 source;
- `corpus_issues.md` ISS-006 records the collision and resolution.

Notable filtering:
- Promise/Christology, Davidic fatherhood, mystical vision material, and strong spiritual identity claims were generally held for contextual delivery;
- scripture/external quotations were not attributed to Neville;
- medical/healing causation, financial guarantees, direct influence/control of others, universal-causation/victim-blaming, and guaranteed physical outcomes were excluded from the automatic pool;
- `L0014` intentionally produced **0 SELECT** because its value is almost entirely context-dependent Promise/Christology.

All five corpus IDs have a corpus-ID-matching editorial completion marker. L0011's restored source files are a corpus-repair exception; pre-existing extraction files for L0012-L0015 were not modified by editorial review.

## 2026-08-31 — Lecture batch L0016–L0020

Completed the next five corpus IDs under `SOURCE_FIRST_CANONICAL`, with explicit handling of two bare-title raw/editorial overlays.

| Corpus ID | Work | Canonical paragraphs | Retained worker windows | SELECT |
|---|---|---:|---:|---:|
| L0016 | Arise | 23 / 23 | 140 | 3 |
| L0017 | At Your Command (`BOOK_REPRINT`, parent B001) | 118 / 118 | 717 | 0 |
| L0018 | Awake O Sleeper | 52 / 52 | 323 | 1 |
| L0019 | Awakened Imagination (1954 lecture) | 33 / 33 | 285 | 1 |
| L0020 | Barabbas Or Jesus | 45 / 45 | 663 | 2 |

Batch result:
- canonical paragraphs reviewed: **271 / 271**;
- worker windows generated: **2,175**;
- retained worker windows: **2,128**;
- worker rejected windows: **47**;
- raw duplicate groups: **222**;
- final main-pool SELECT fragments: **7**.

Identity handling:
- `[At Your Command]` raw metadata identifies `L0017`, while the editorial layer already occupying that folder identifies `B001`; registry independently marks L0017 as `BOOK_REPRINT` with `canonical_parent_id=B001`. The full 118-paragraph reprint was read and contributes **0 new SELECT**. Its derivative completion layer is stored in `[At Your Command – L0017 Reprint]` so B001 is not overwritten.
- `[Awakened Imagination]` raw metadata identifies `L0019`, a distinct 33-paragraph 1954 lecture, while the editorial layer already occupying that folder identifies `B009`, the 504-paragraph book. L0019 was reviewed independently and its derivative completion layer is stored in `[Awakened Imagination – L0019 Lecture]`.
- `corpus_issues.md` ISS-007 records these raw/editorial corpus-ID overlays and establishes that queue completion must match `editorial_complete.json.corpus_id`, not merely filename/folder presence.

Notable filtering:
- `L0017` is wholly suppressed as a cross-work reprint duplicate of B001 rather than inflating the final corpus;
- `L0018` is predominantly Promise/postmortem cosmology and Davidic theology; its categorical heart-transplant/medical passage and mental-health guarantee were excluded;
- `L0019` revision material asserting control over relatives/employers, guaranteed results, rejection of external facts, or self-causation of interpersonal harm was excluded or held; the final strict shortlist was reduced to one clean active-imagination formulation;
- `L0020` financial/inheritance/job guarantees, hospital/health revision, sensory-evidence denial, and theological absolutes were held or dropped; two clean Neville-only fragments survived, including an explicitly loving/ethical use-of-imagination formulation.

All five corpus IDs now have corpus-ID-matching editorial completion markers, including separate derivative folders for L0017 and L0019 where the bare-title folders are occupied by different book editorial identities.

## 2026-08-31 — Lecture batch L0021–L0025

Completed the next five corpus IDs under `SOURCE_FIRST_CANONICAL`.

| Corpus ID | Work | Canonical paragraphs | Retained worker windows | SELECT |
|---|---|---:|---:|---:|
| L0021 | Be Imitators Of God | 32 / 32 | 303 | 1 |
| L0022 | Bear Ye One Another’S Burdens | 36 / 36 | 363 | 2 |
| L0023 | Before Abraham, Was I Am | 32 / 32 | 296 | 1 |
| L0024 | Behold The Dreamer | 39 / 39 | 393 | 0 |
| L0025 | Believe In Him | 47 / 47 | 395 | 2 |

Batch result:
- canonical paragraphs reviewed: **186 / 186**;
- worker windows generated: **1,770**;
- retained worker windows: **1,750**;
- worker rejected windows: **20**;
- raw duplicate groups: **163**;
- final main-pool SELECT fragments: **6**.

Notable filtering:
- `L0021` is predominantly Promise/risen-Christ testimony; one clean self-image/imagination instruction survives, while mystical, postmortem and guaranteed-outcome material remains contextual;
- `L0022` keeps a self-limitation warning and the formulation of faith as loyalty to unseen reality; claims that another person must change through one's imagining, plus categorical financial/health outcomes, were kept out of the automatic pool;
- `L0023` contributes one distinctive states formulation separating a person from the state currently occupied; Abraham/Christ allegory, resurrection and mystical vision remain HOLD;
- `L0024` intentionally produces **0 SELECT** because its strongest material depends on literal dream metaphysics, alternate-time/postmortem cosmology, spiritual identity or universal-causation framing; the empty curated file is deliberate;
- `L0025` contributes an ethical motive test centered on love and a concise wish-fulfilled assumption instruction; Promise theology, mystical testimony, categorical financial guarantees, sensitive biographical material with causal framing, and strong outcome guarantees were excluded or held;
- scripture and external-author wording were not attributed to Neville, and weaker overlapping worker variants were collapsed throughout.

Date/provenance note for `L0025`:
- `corpus_registry.json` records the exact `full_date` **1969-02-28**;
- the pre-existing raw `source_manifest.md` retains `1969-01-01` as a year-level placeholder;
- the editorial layer uses the exact registry date without rewriting the raw manifest.

All five works now contain `curated_*`, `editorial_decisions_*`, `editorial_review_*`, and corpus-ID-matching `editorial_complete.json` files. Raw candidate, rejected, master-text, source-manifest, source-variation, worker-report, and processing files were not modified.

## 2026-08-31 — Lecture batch L0026–L0030

Completed the next five corpus IDs under `SOURCE_FIRST_CANONICAL`.

| Corpus ID | Work | Canonical paragraphs | Retained worker windows | SELECT |
|---|---|---:|---:|---:|
| L0026 | Believe It In | 31 / 31 | 417 | 3 |
| L0027 | Biblical Language | 32 / 32 | 351 | 2 |
| L0028 | Blake On Religion | 115 / 115 | 646 | 2 |
| L0029 | Brazen Impudence | 29 / 29 | 384 | 3 |
| L0030 | Building Your Temple | 20 / 20 | 221 | 1 |

Batch result:
- canonical paragraphs reviewed: **227 / 227**;
- worker windows generated: **2,090**;
- retained worker windows: **2,019**;
- worker rejected windows: **71**;
- raw duplicate groups: **145**;
- final main-pool SELECT fragments: **11**.

Notable filtering:
- `L0026` retains three practical Neville-only instructions on clarifying desire, self-observation, and assuming the feeling of fulfillment; direct-control, universal-causation, mental-health disparagement, financial guarantees, scripture/external wording and Promise material were excluded or held;
- `L0027` is predominantly theological/symbolic and retains two formulations: biblical language as evocative rather than descriptive, and faith as the link between imaginal act and objective hope; medical anecdotes/generalizations, control language, Promise/resurrection and strong metaphysical claims remain outside the automatic pool;
- `L0028` received a strict authorship pass because the lecture quotes William Blake extensively. All direct Blake wording and other external quotations were excluded from Neville attribution. Two Neville-only formulations survive; Blake-dependent paraphrase and mystical/postmortem/control material remain contextual;
- `L0029` retains three persistence/assumption/scene-construction formulations. The central personal case used to claim causal responsibility for another person's misconduct and to describe others as compelled instruments of one's will was excluded from the automatic pool, together with bilocation, medical/end-of-life context and strong guarantees;
- `L0030` is overwhelmingly Promise/temple symbolism and contributes one practical revision instruction. Blake quotations, scripture, mystical temple/resurrection identity, predestination, war/event-causation and universal-causation remain HOLD/DROP;
- overlapping worker variants were collapsed source-first throughout; no quota was imposed.

All five works now contain `curated_*`, `editorial_decisions_*`, `editorial_review_*`, and corpus-ID-matching `editorial_complete.json` files. Raw candidate, rejected, master-text, source-manifest, source-variation, worker-report, and processing files were not modified.

## 2026-08-31 — Lecture batch L0031–L0035

Completed the next five corpus IDs under `SOURCE_FIRST_CANONICAL`.

| Corpus ID | Work | Canonical source units | Retained worker windows | SELECT |
|---|---|---:|---:|---:|
| L0031 | By Water And Blood – June 24 1956 | 1 / 1 long source paragraph; full ~4,470-word master | 549 | 2 |
| L0032 | Catch The Mood | 69 / 69 paragraphs | 826 | 4 |
| L0033 | Changing The Feeling Of “I” | 22 / 22 paragraphs | 452 | 4 |
| L0034 | Christ Bears Our Sins | 40 / 40 paragraphs | 305 | 0 |
| L0035 | Christ In Man | 30 / 30 paragraphs | 326 | 2 |

Batch result:
- canonical source units reviewed: **162 / 162**;
- worker windows generated: **2,536**;
- retained worker windows: **2,458**;
- worker rejected windows: **78**;
- raw duplicate groups: **148**;
- final main-pool SELECT fragments: **12**.

Notable filtering:
- `L0031` is physically stored as one long canonical paragraph, so the full ~4,470-word master was read end-to-end; two practical Neville-only fragments survive on vivid imaginal representation and faithful assumption. Water/blood/incarnation symbolism, direct-other influence, universal causation and guaranteed health/financial outcomes remain contextual or excluded;
- `L0032` contributes four strong formulations on entering a state, thinking from it, prayer as subjective appropriation, and the habitual state from which one views the world. Absolute no-failure claims, direct-other causation, zero-sum outcome rationalization and strong theological identity are excluded or held;
- `L0033` contributes four self-observation/state-change formulations. The racial-discrimination case and other passages framing external mistreatment or other people's conduct as caused by the subject's inner state are explicitly excluded as victim-blaming/universal-causation material;
- `L0034` intentionally produces **0 SELECT**. Its strongest passages remain inseparable from medical/pain causation, universal identity/causation, Promise/postmortem theology, or guaranteed financial/relationship outcomes;
- `L0035` contributes two clean revision formulations. Guaranteed external confirmation, direct change of others, deterministic criminal/violent-state language, universal causation, mystical theology and scripture remain HOLD/DROP;
- pure scripture/external wording and weaker overlapping worker variants were excluded throughout.

Date/provenance notes:
- `L0031` editorial metadata uses registry `full_date` **1956-06-24**; raw `date`/manifest retain `1956-01-01` as a placeholder;
- `L0032` and `L0033` have no exact `full_date` in repository metadata, so `1968-01-01` and `1953-01-01` are explicitly marked as year-level placeholders;
- `L0034` editorial metadata uses registry `full_date` **1969-02-24** while raw `date`/manifest retain `1969-01-01` as a placeholder;
- `L0035` uses the exact date **1966-10-17**.

All five works now contain `curated_*`, `editorial_decisions_*`, `editorial_review_*`, and corpus-ID-matching `editorial_complete.json` files. Raw candidate, rejected, master-text, source-manifest, source-variation, worker-report, and processing files were not modified.

## 2026-08-31 — Lecture batch L0036–L0040

Completed the next five corpus IDs under `SOURCE_FIRST_CANONICAL`.

| Corpus ID | Work | Canonical paragraphs | Retained worker windows | SELECT |
|---|---|---:|---:|---:|
| L0036 | Christ In You | 32 / 32 | 439 | 2 |
| L0037 | Christ Is Your Life | 42 / 42 | 374 | 0 |
| L0038 | Christ Unveiled | 34 / 34 | 645 | 0 |
| L0039 | Christmas-Man’s Birth as God | 53 / 53 | 350 | 0 |
| L0040 | Come O Blessed | 25 / 25 | 303 | 0 |

Batch result:
- canonical paragraphs reviewed: **186 / 186**;
- worker windows generated: **2,165**;
- retained worker windows: **2,111**;
- worker rejected windows: **54**;
- raw duplicate groups: **162**;
- final main-pool SELECT fragments: **2**.

Notable filtering:
- `L0036` contributes two clean Neville-only formulations: the habitual state to which thought returns as one’s dwelling place, and a fulfilled-desire self-inquiry framed through what one would hear, see, and experience. Promise/Christology, mystical David material, direct-other influence, categorical mental-health causation, guaranteed manifestation language, scripture/external wording, and weaker overlaps remain HOLD/DROP;
- `L0037` intentionally produces **0 SELECT**. Its practical passages repeatedly depend on influencing other people, guaranteed outer correspondence, financial acquisition, or universal-causation framing; the remainder is predominantly Promise/Christology, prophetic vision, scripture interpretation, and supernatural identity material;
- `L0038` intentionally produces **0 SELECT**. The lecture is overwhelmingly Promise/Christology and scriptural exegesis, while its concrete power demonstrations include literal immobilization/control of other people and a violent hypothetical, which are excluded rather than decontextualized;
- `L0039` intentionally produces **0 SELECT**. It is primarily Christmas/Promise theology and mystical identity, and its later causal section makes categorical claims linking moods/reactions with influenza, cancer, pain, and other events, including victim-blaming/event-causation material;
- `L0040` intentionally produces **0 SELECT**. Its main practical examples concern imagining financial or career outcomes for other people and treating inheritance, schooling, business ownership, or prosperity as causal confirmation; several material-help passages become misleading when isolated, and Blake/scripture wording is external;
- no quota was imposed, and worker scores did not override source-first safety/authorship review.

Date/provenance notes:
- `L0036` uses the exact date **1969-05-06**;
- `L0037` uses the exact date **1968-10-18**;
- `L0038` editorial metadata uses registry `full_date` **1963-03-15**, while the pre-existing raw report/manifest retain `1963-01-01` as a year-level placeholder;
- `L0039` has no registry `full_date`; repository `date: 1968-01-01` is retained only as a year-level placeholder, and the unusual physical folder spelling `[Christmas-Man’S Birth As God]` is preserved unchanged;
- `L0040` uses the exact date **1967-11-10**.

All five works now contain `curated_*`, `editorial_decisions_*`, `editorial_review_*`, and corpus-ID-matching `editorial_complete.json` files. Raw candidate, rejected, master-text, source-manifest, source-variation, worker-report, and processing files were not modified.

## 2026-09-01 — Lecture batch L0041–L0045

Completed the next five corpus IDs under `SOURCE_FIRST_CANONICAL`.

| Corpus ID | Work | Canonical paragraphs | Retained worker windows | SELECT |
|---|---|---:|---:|---:|
| L0041 | Conception | 31 / 31 | 367 | 2 |
| L0042 | Creation-Faith | 57 / 57 | 336 | 3 |
| L0043 | Divine Signs | 42 / 42 | 280 | 3 |
| L0044 | Election And Change Of Consciousness | 30 / 30 | 405 | 2 |
| L0045 | Enter The Dream | 31 / 31 | 346 | 1 |

Batch result:
- canonical paragraphs reviewed: **191 / 191**;
- worker windows generated: **1,774**;
- retained worker windows: **1,734**;
- worker rejected windows: **40**;
- raw duplicate groups: **165**;
- final main-pool SELECT fragments: **11**.

Notable filtering:
- `L0041` contributes two practical formulations on entering a state by assumption/thinking from it and deliberately occupying a desired state. Guaranteed bridge-of-events language, war/event causation, universal causation, Promise theology, mystical sexual symbolism, scripture/external wording, and weaker overlaps remain HOLD/DROP;
- `L0042` contributes three formulations on faith as loyalty to unseen reality, listening to the implication of inner speech, and mentally structuring desire as already possessed. Direct-other influence, guaranteed externalization, blame framing, violent power demonstrations, Promise/postmortem material and external wording remain outside the automatic pool;
- `L0043` contributes three formulations on assuming the fulfilled identity, focusing on the end rather than means, and imagination requiring operative assumption. Absolute no-failure claims, debt/financial causal examples, universal-causation claims, Promise theology, mystical sexual symbolism, scripture/external wording, and weaker overlaps remain HOLD/DROP;
- `L0044` contributes two formulations on feeling as movement between states and remaining psychologically in the selected state. Promise/resurrection material, dream exegesis, financial-status examples, guaranteed objective-birth language, strong metaphysics, scripture/external wording and weaker overlaps remain HOLD/DROP;
- `L0045` contributes one concise assumption instruction. The neighboring guarantee that one will become the assumed identity was deliberately excluded. Passages rationalizing murder/rape as states of experience, universal actor/causation and control claims, postmortem cosmology, alternate-world testimony, and Blake/Huxley/Lawrence/scripture wording remain HOLD/DROP;
- no quota was imposed, and worker scores did not override source-first safety/authorship review.

Date/provenance notes:
- `L0041` uses exact registry `full_date` **1968-03-11**;
- `L0042` editorial metadata uses exact registry `full_date` **1968-05-20**, while the pre-existing raw report/manifest retain **1968-01-01** as a year-level placeholder;
- `L0043` uses exact registry `full_date` **1968-05-01**;
- `L0044` has registry `full_date: null`; repository `date` and `source_manifest.md` both record **1963-02-24**, which is preserved as repository/source date without presenting it as registry-verified full_date;
- `L0045` uses exact registry `full_date` **1969-11-21**.

All five works now contain `curated_*`, `editorial_decisions_*`, `editorial_review_*`, and corpus-ID-matching `editorial_complete.json` files. Raw candidate, rejected, master-text, source-manifest, source-variation, worker-report, and processing files were not modified.

## 2026-09-01 — Lecture batch L0046–L0050

Completed the next five corpus IDs under `SOURCE_FIRST_CANONICAL`.

| Corpus ID | Work | Canonical paragraphs | Retained worker windows | SELECT |
|---|---|---:|---:|---:|
| L0046 | Esau – Jacob – Israel | 36 / 36 | 567 | 3 |
| L0047 | Esau And Jacob | 42 / 42 | 576 | 2 |
| L0048 | Eschatology-The Doctrine Of The End | 45 / 45 | 385 | 0 |
| L0049 | Eschatology-The Drama Of The End | 30 / 30 | 334 | 0 |
| L0050 | Eternal States | 18 / 18 | 232 | 3 |

Batch result:
- canonical paragraphs reviewed: **171 / 171**;
- worker windows generated: **2,157**;
- retained worker windows: **2,094**;
- worker rejected windows: **63**;
- raw duplicate groups: **149**;
- final main-pool SELECT fragments: **8**.

Notable filtering:
- `L0046` contributes three Neville-only formulations on the inner arranging faculty, beginning from the desired end, and seeing/feeling from fulfillment. Guaranteed crystallization, direct-other persuasion, universal fulfillment/event-causation, mystical Esau symbolism, Promise/David theology, scripture/external wording and weaker overlaps remain HOLD/DROP;
- `L0047` contributes two concise identification/absorption formulations. Passages describing other people as automatons or compelled servants of imaginal command, no-power-can-stop guarantees, broad universal causation, psychoanalysis disparagement, mystical bilocation/out-of-body claims and external wording remain outside the automatic pool;
- `L0048` intentionally produces **0 SELECT**. It is overwhelmingly eschatology/Promise, mystical testimony, postmortem cosmology and scriptural exegesis. Its non-condemnation passages depend on the stronger claim that everyone must enact every evil role, so they are not decontextualized into daily advice;
- `L0049` intentionally produces **0 SELECT**. Its revision/repentance idea is a weaker cross-work duplicate of the already selected L0035 formulation; the rest is dominated by eschatology, dream symbolism, guaranteed supernatural unfolding, and a passage framing killer and victim as roles of one actor;
- `L0050` contributes three formulations on self-inquiry into one's state, stable identity across states, and assuming the desired feeling now. Universal-causation, direct control of others without consent, guaranteed outcomes, literal world-freezing/animation, pseudo-scientific validation, mystical/postmortem material, scripture/external wording and weaker overlaps remain HOLD/DROP;
- no quota was imposed, and worker scores did not override source-first safety/authorship review.

All five works now contain `curated_*`, `editorial_decisions_*`, `editorial_review_*`, and corpus-ID-matching `editorial_complete.json` files. Raw candidate, rejected, master-text, source-manifest, source-variation, worker-report, and processing files were not modified.

## 2026-09-01 — Lecture batch L0051–L0055

Completed the next five corpus IDs under `SOURCE_FIRST_CANONICAL`.

| Corpus ID | Work | Canonical paragraphs | Retained worker windows | SELECT |
|---|---|---:|---:|---:|
| L0051 | Eternity Within | 38 / 38 | 488 | 0 |
| L0052 | Every Natural Effect | 23 / 23 | 853 | 2 |
| L0053 | Experience Scripture | 85 / 85 | 779 | 0 |
| L0054 | Faith | 71 / 71 | 1,002 | 1 |
| L0055 | Faith In God | 28 / 28 | 278 | 2 |

Batch result:
- canonical paragraphs reviewed: **245 / 245**;
- worker windows generated: **3,562**;
- retained worker windows: **3,400**;
- worker rejected windows: **162**;
- raw duplicate groups: **201**;
- final main-pool SELECT fragments: **5**.

Notable filtering:
- `L0051` intentionally produces **0 SELECT**. Its practical assumption passages are tied to categorical outcome claims or are weaker than already selected formulations; the lecture is predominantly Promise, Davidic fatherhood, postmortem cosmology, mystical testimony and universal-role framing;
- `L0052` contributes two formulations: remaining faithful to a desired self-state, and distinguishing the person from the state currently occupied. Universal/event causation, direct-other influence, health-related causation, guaranteed outcomes, Promise/dream symbolism and external wording remain HOLD/DROP;
- `L0053` intentionally produces **0 SELECT**. It is overwhelmingly Christology, eschatology, scripture fulfillment and mystical testimony, with concrete power passages depending on literal dominion/control or strong metaphysical claims;
- `L0054` contributes one concise question about seeing present facts while retaining faith in an unseen state. Its faith-as-loyalty formulation is suppressed as a cross-work near-duplicate of the cleaner L0042 selection; health/event causation, direct influence, guaranteed outcomes, scientific-validation framing and external wording remain outside the automatic pool;
- `L0055` contributes two formulations on the feeling of possession and making a desired future present. Direct-other influence, financial/job outcome guarantees, broad harm/health causation, causal-proof anecdotes, Promise material and external wording remain HOLD/DROP;
- no quota was imposed, and worker scores did not override source-first safety/authorship review.

Date/provenance notes:
- `L0051` editorial metadata uses registry `full_date` **1966-10-04**, while raw report/manifest retain **1966-01-01** as a year-level placeholder;
- `L0052` has registry `full_date: null`; repository `date: 1968-01-01` is retained only as a year-level placeholder;
- `L0053` editorial metadata uses registry `full_date` **1971-05-28**, while raw report/manifest retain **1971-01-01** as a year-level placeholder;
- `L0054` editorial metadata uses registry `full_date` **1968-07-22**, while raw report/manifest retain **1968-01-01** as a year-level placeholder;
- `L0055` uses exact registry `full_date` **1968-02-05**.

All five works now contain `curated_*`, `editorial_decisions_*`, `editorial_review_*`, and corpus-ID-matching `editorial_complete.json` files. Raw candidate, rejected, master-text, source-manifest, source-variation, worker-report, and processing files were not modified.

## 2026-09-01 — Lecture batch L0056–L0060

Completed the next five corpus IDs under `SOURCE_FIRST_CANONICAL`.

| Corpus ID | Work | Canonical paragraphs | Retained worker windows | SELECT |
|---|---|---:|---:|---:|
| L0056 | Faith, Hope And Love | 24 / 24 | 292 | 1 |
| L0057 | Feed My Sheep – July 1 1956 | 21 / 21 | 567 | 2 |
| L0058 | Feel Deeply | 29 / 29 | 428 | 3 |
| L0059 | Follow Me | 54 / 54 | 437 | 0 |
| L0060 | Follow The Pattern | 21 / 21 | 399 | 1 |

Batch result:
- canonical paragraphs reviewed: **149 / 149**;
- worker windows generated: **2,178**;
- retained worker windows: **2,123**;
- worker rejected windows: **55**;
- raw duplicate groups: **140**;
- final main-pool SELECT fragments: **7**.

Notable filtering:
- `L0056` contributes one self-observation question about present imagining. Promise/Father theology, mystical testimony, the railroad-disaster causation example, universal-causation language and external wording remain HOLD/DROP;
- `L0057` contributes two formulations on practicing understanding and a simple spatial assumption exercise. Passages discouraging reliance on doctors/patient evidence, substituting imaginal treatment for outward recommendations, direct transformation of others and guaranteed correspondence remain outside the automatic pool;
- `L0058` contributes three formulations on deep feeling, assuming desire as present fact and thinking from fulfillment. Guaranteed externalization, health/wealth outcome language, zero-sum/other-person causation and stronger mystical material remain HOLD/DROP;
- `L0059` intentionally produces **0 SELECT**. It is dominated by Promise/Christology, mystical resurrection and postmortem cosmology; its concrete power claims include literal freezing/re-animation and universal actor/causation framing;
- `L0060` contributes one formulation on limiting belief directing thought. Direct-other influence, no-power-can-stop language, guaranteed salary/result examples, universal causation, Promise/serpent theology and external wording remain HOLD/DROP;
- no quota was imposed, and worker scores did not override source-first safety/authorship review.

Date/provenance notes:
- `L0056` has registry `full_date: null`; repository `date: 1968-01-01` is retained only as a year-level placeholder;
- `L0057` editorial metadata uses registry `full_date` **1956-07-01**, while the raw report/manifest retain **1956-01-01** as a year-level placeholder;
- `L0058` uses exact registry `full_date` **1969-05-30**;
- `L0059` uses exact registry `full_date` **1968-11-11**;
- `L0060` uses exact registry `full_date` **1968-03-25**.

All five works now contain `curated_*`, `editorial_decisions_*`, `editorial_review_*`, and corpus-ID-matching `editorial_complete.json` files. Raw candidate, rejected, master-text, source-manifest, source-variation, worker-report, and processing files were not modified.

## 2026-09-01 — Lecture batch L0061–L0065

Completed the next five corpus IDs under `SOURCE_FIRST_CANONICAL`.

| Corpus ID | Work | Canonical paragraphs | Retained worker windows | SELECT |
|---|---|---:|---:|---:|
| L0061 | Four Fold Vision | 44 / 44 | 344 | 2 |
| L0062 | Four Mighty Ones – June 17 1956 | 1 / 1 | 448 | 2 |
| L0063 | Freedom | 23 / 23 | 399 | 0 |
| L0064 | Fulfillment Of God’s Plan | 26 / 26 | 870 | 1 |
| L0065 | Fundamentals | 23 / 23 | 93 | 4 |

Batch result:
- canonical paragraphs/source units reviewed: **117 / 117**;
- worker windows generated: **2,231**;
- retained worker windows: **2,154**;
- worker rejected windows: **77**;
- raw duplicate groups: **98**;
- final main-pool SELECT fragments: **9**.

Notable filtering:
- `L0061` contributes two practical formulations on making imagination a daily practice and not confusing hearing an idea with actually doing it. Medical/diet dismissal, the skin-cancer disappearance example, broad create/un-create causation, direct-other framing, Promise/postmortem material and external wording remain HOLD/DROP;
- `L0062` contributes two practical fragments: a four-question self-inquiry for clarifying an implied end, and a concise instruction to assume the desired identity. Universal first-cause/self-blame claims, serious-injury self-causation, assigning other people roles without consent, guaranteed hardening-into-fact language, symbolic theology and scripture remain outside the automatic pool;
- `L0063` intentionally produces **0 SELECT**. Its central argument repeatedly attributes misfortune, injury, illness, conflict, firing and other people’s actions to the individual imagination; softer-looking sentences cannot be detached honestly from that pervasive universal-causation/self-blame premise;
- `L0064` contributes one late practical fragment on continuing to dream noble dreams without attaching a guaranteed timetable. The lecture is otherwise overwhelmingly Promise/Christology, Davidic fatherhood, resurrection testimony and scripture interpretation, with no-accident/spiritual-cause claims and causal daydream anecdotes excluded;
- `L0065` contributes four practical formulations on present self-observation, measuring reactions against a defined aim, assuming a preferred loving identity while observing reactions, and detaching from habitual reactions. Categorical circumstance-causation, blame-heavy examples, Emerson wording and stronger metaphysical claims remain HOLD/DROP;
- no quota was imposed, and worker scores did not override source-first safety/authorship review.

Date/provenance notes:
- `L0061` uses exact registry `full_date` **1968-01-26**;
- `L0062` registry `full_date` is null and raw `date` remains the year-level placeholder **1956-01-01**; editorial metadata records **1956-06-17** because that exact date is embedded in the canonical title/folder and primary-source slug. Registry/raw provenance was not rewritten;
- `L0063` uses exact registry `full_date` **1968-10-28**;
- `L0064` has registry `full_date: null`; repository `date: 1968-01-01` is retained only as a year-level placeholder;
- `L0065` has registry `full_date: null`; repository `date: 1953-01-01` is retained only as a year-level placeholder, while the canonical source header identifies INTA Bulletin, New Thought, summer 1953.

All five works now contain `curated_*`, `editorial_decisions_*`, `editorial_review_*`, and corpus-ID-matching `editorial_complete.json` files. Raw candidate, rejected, master-text, source-manifest, source-variation, worker-report, and processing files were not modified.

## 2026-09-01 — Lecture batch L0066–L0070

Completed the next five corpus IDs under `SOURCE_FIRST_CANONICAL`.

| Corpus ID | Work | Canonical paragraphs | Retained worker windows | SELECT |
|---|---|---:|---:|---:|
| L0066 | God Became Man | 16 / 16 | 261 | 0 |
| L0067 | God Is Light | 25 / 25 | 399 | 0 |
| L0068 | God Only Acts | 31 / 31 | 228 | 0 |
| L0069 | God Speaks To Man | 41 / 41 | 334 | 2 |
| L0070 | God’s Almighty Power | 24 / 24 | 362 | 1 |

Batch result:
- canonical paragraphs reviewed: **137 / 137**;
- worker windows generated: **1,609**;
- retained worker windows: **1,584**;
- worker rejected windows: **25**;
- raw duplicate groups: **121**;
- final main-pool SELECT fragments: **3**.

Notable filtering:
- `L0066` intentionally produces **0 SELECT**. It is dominated by literal God-identity, Promise/Davidic fatherhood, mystical testimony, universal-role claims and scripture interpretation; short benign phrases become generic or context-broken when isolated;
- `L0067` intentionally produces **0 SELECT**. Its strongest practical assumption block is a weaker/near-duplicate of cleaner corpus selections and carries categorical fulfillment language; healing-as-proof, literal light/love identity, fiery-arrow influence, postmortem material and scripture remain HOLD/DROP;
- `L0068` intentionally produces **0 SELECT**. Its central God-only-acts thesis treats harmful and benevolent actions as one divine actor, while the practical section directs imaginal alteration of others and promises conformity. A safe hear-and-do formulation is suppressed as a weaker duplicate of L0061;
- `L0069` contributes two clean Neville-only fragments: one on reading a dream for its central message rather than every detail, and one on becoming selective and assuming something wonderful for oneself. Universal causation, no-consent role assignment, postmortem/alternate-world claims and medical/life-extension disparagement remain outside the pool;
- `L0070` contributes one vivid practical fragment on entering the mood of the wish fulfilled before sleep. Financial guarantees, categorical outcome promises, no-consent role mechanisms, causal-proof anecdotes and strong literal God/Christ identity remain HOLD/DROP;
- no quota was imposed, and worker scores did not override source-first safety/authorship review.

Date/provenance notes:
- `L0066` uses exact registry `full_date` **1969-02-24**;
- `L0067` has registry `full_date: null`; repository `date` and canonical worker report record **1967-10-09**, preserved as repository/source date without presenting it as registry-verified `full_date`;
- `L0068` editorial metadata uses exact registry `full_date` **1966-09-20**, while the raw worker report retains **1966-01-01** as a year-level placeholder;
- `L0069` uses exact registry `full_date` **1968-01-18**;
- `L0070` uses exact registry `full_date` **1968-12-02**.

All five works now contain `curated_*`, `editorial_decisions_*`, `editorial_review_*`, and corpus-ID-matching `editorial_complete.json` files. Raw candidate, rejected, master-text, source-manifest, source-variation, worker-report, and processing files were not modified.

## 2026-09-01 — Lecture batch L0071–L0075

Completed the next five corpus IDs under `SOURCE_FIRST_CANONICAL`.

| Corpus ID | Work | Canonical paragraphs | Retained worker windows | SELECT |
|---|---|---:|---:|---:|
| L0071 | God’s Creative Power | 28 / 28 | 361 | 1 |
| L0072 | God’s Dwelling Place | 37 / 37 | 404 | 0 |
| L0073 | God’s Plan Of Redemption | 31 / 31 | 371 | 0 |
| L0074 | God’s Promise To Man | 26 / 26 | 507 | 0 |
| L0075 | God’s Wisest Creature | 35 / 35 | 208 | 0 |

Batch result:
- canonical paragraphs reviewed: **157 / 157**;
- worker windows generated: **1,893**;
- retained worker windows: **1,851**;
- worker rejected windows: **42**;
- raw duplicate groups: **123**;
- final main-pool SELECT fragments: **1**.

Notable filtering:
- `L0071` contributes one clean self-inquiry on turning to imagination and remaining faithful to the selected state. Literal Christ/God identity, Promise/Davidic fatherhood, guaranteed manifestation, universal causation, no-consent other-person mechanisms, scripture/external wording and weaker duplicates remain HOLD/DROP;
- `L0072` intentionally produces **0 SELECT**. Practical state-entry language depends on completed-state/alternate-world metaphysics and categorical externalization; the rest is dominated by Promise, pre-existence, mystical testimony, universal-role framing and postmortem cosmology;
- `L0073` intentionally produces **0 SELECT**. Practical examples center on horse-racing luck and financial-security outcomes, while categorical imagination-as-cause and guaranteed externalization are mixed with Redemption/Promise and resurrection theology;
- `L0074` intentionally produces **0 SELECT**. The source is overwhelmingly Promise/Davidic fatherhood and mystical resurrection testimony; its explicit Law interlude uses health and wealth affirmations with outcome expectations;
- `L0075` intentionally produces **0 SELECT**. The lecture is dominated by serpent/seraphim symbolism, resurrection, pre-existent divine identity and universal-role theology; its family self-concept anecdote is immediately converted into a financial-growth claim;
- no quota was imposed, and worker scores did not override source-first safety/authorship review.

Date/provenance notes:
- `L0071` uses exact registry `full_date` **1968-02-09**;
- `L0072` uses exact registry `full_date` **1969-05-08**;
- `L0073` uses exact registry `full_date` **1969-03-24**;
- `L0074` editorial metadata uses exact registry `full_date` **1963-02-08**, while the raw worker report retains **1963-01-01** as a year-level placeholder;
- `L0075` editorial metadata uses exact registry `full_date` **1968-09-20**, while the raw worker report retains **1968-01-01** as a year-level placeholder.

All five works now contain `curated_*`, `editorial_decisions_*`, `editorial_review_*`, and corpus-ID-matching `editorial_complete.json` files. Raw candidate, rejected, master-text, source-manifest, source-variation, worker-report, and processing files were not modified.

## 2026-09-01 — Lecture batch L0076–L0085

Completed ten corpus IDs under `SOURCE_FIRST_CANONICAL`, processed internally as two five-work reading checkpoints without relaxing the editorial threshold.

| Corpus ID | Work | Canonical paragraphs | Retained worker windows | SELECT |
|---|---|---:|---:|---:|
| L0076 | God’s Word | 31 / 31 | 249 | 0 |
| L0077 | Good Friday – Easter | 21 / 21 | 364 | 0 |
| L0078 | Grace Vs. Law | 27 / 27 | 527 | 0 |
| L0079 | Have You Found Him? | 33 / 33 | 193 | 0 |
| L0080 | He Dreams In Me | 57 / 57 | 379 | 1 |
| L0081 | He Is Dreaming Now | 53 / 53 | 720 | 0 |
| L0082 | He Is Dreaming Now 1 | 109 / 109 | 889 | 1 |
| L0083 | He Is My Resurrection | 38 / 38 | 324 | 0 |
| L0084 | He Wakes In Me | 34 / 34 | 362 | 0 |
| L0085 | His Name | 27 / 27 | 452 | 1 |

Batch result:
- canonical paragraphs reviewed: **430 / 430**;
- worker windows generated: **4,608**;
- retained worker windows: **4,459**;
- worker rejected windows: **149**;
- raw duplicate groups: **335**;
- final main-pool SELECT fragments: **3**.

Notable filtering:
- `L0076` intentionally produces **0 SELECT**. It is dominated by Promise, tree-of-life/regeneration symbolism and mystical testimony; practical-looking material depends on strong metaphysics/body-causation, direct-other influence, external wording, generic advice or weaker duplicates;
- `L0077` intentionally produces **0 SELECT**. Its practical assumption/transformation passages are mixed with health-related causation, changing other people, guaranteed hardening-into-fact language and Easter/rebirth symbolism;
- `L0078` intentionally produces **0 SELECT**. Its Law passages assert broad mental causation, guaranteed bridges of incidents, no-power-can-stop fulfillment and no-consent other-person conformity; the remainder is grace/salvation, resurrection, predestination and scripture;
- `L0079` intentionally produces **0 SELECT**. It is predominantly Promise/David/Father identity; the late Law section frames security/wealth as states with expected external fruit, while other practical passages concern another person or duplicate cleaner corpus selections;
- `L0080` contributes one clean technical fragment on taking a wish, seeing it fulfilled, contemplating it and merging with the imaginal scene. Neighboring guarantees of objectification were excluded;
- `L0081` intentionally produces **0 SELECT**. It is overwhelmingly Promise/Alice-King dream cosmology and creation metaphysics, with financial/social anecdotes used as causal proof; the safe reverse-day recollection exercise is too generic for the main pool;
- `L0082` contributes one concise fragment on taking a bold inner step that changes a pattern of thinking and living. Financial/property/business proofs, direct or no-consent influence, guaranteed outcomes, universal causation and stronger duplicates remain outside the pool;
- `L0083` intentionally produces **0 SELECT**. It is dominated by resurrection/Promise and Davidic fatherhood, while its Law passages assert inevitable hardening into fact and universal imagination-causes-events, including blame-heavy explanations of harmful events;
- `L0084` intentionally produces **0 SELECT**. It is overwhelmingly resurrection/Christ identity and mystical testimony; later examples reframe harmful events through predetermined redemption and universal actor/causation;
- `L0085` contributes one clean self-observation fragment on keeping what is heard, felt and thought in harmony with one's highest ideal. Oil/wealth, health, guarantee and universal-causation framing was excluded;
- no quota was imposed. Increasing the operational batch from five to ten did not change the source-first threshold: seven of ten works intentionally remained at zero SELECT.

Date/provenance notes:
- `L0076` uses exact registry `full_date` **1967-11-13**;
- `L0077` has registry `full_date: null`; repository `date: 1954-01-01` is retained only as a year-level placeholder;
- `L0078` has registry `full_date: null`; repository date and canonical worker report record **1963-03-12**, preserved as repository/source date;
- `L0079` editorial metadata uses exact registry `full_date` **1967-09-15**, while the raw worker report retains **1967-01-01** as a year-level placeholder;
- `L0080` uses exact registry `full_date` **1967-03-13**;
- `L0081` editorial metadata uses exact registry `full_date` **1970-05-08**, while the raw worker report retains **1970-01-01** as a year-level placeholder;
- `L0082` has registry `full_date: null`; repository `date: 1968-01-01` is retained only as a year-level placeholder;
- `L0083` uses exact registry `full_date` **1968-06-28**;
- `L0084` has registry `full_date: null`; repository date and canonical worker report record **1967-03-24**, preserved as repository/source date;
- `L0085` has registry `full_date: null`; repository date and canonical worker report record **1963-02-26**, preserved as repository/source date.

All ten works now contain `curated_*`, `editorial_decisions_*`, `editorial_review_*`, and corpus-ID-matching `editorial_complete.json` files. Raw candidate, rejected, master-text, source-manifest, source-variation, worker-report, and processing files were not modified.

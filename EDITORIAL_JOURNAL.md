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

# Editorial Journal — Neville Goddard Corpus

This journal tracks the strict book-by-book and work-by-work review defined in `EDITORIAL_POLICY.md`.

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
| He Breaks The Shell | COMPLETE | 98 paragraphs / 188 raw windows | 0 | section-level | section-level | `[He Breaks The Shell]/curated_he_breaks_the_shell.jsonl` |
| I Know My Father | COMPLETE | 10 chapters / 177 paragraphs / 892 raw windows | 17 | section-level | section-level | `[I Know My Father]/curated_i_know_my_father.jsonl` |
| Out Of This World | COMPLETE | 4 chapters / 189 paragraphs / 493 raw windows | 20 | section-level | section-level | `[Out Of This World]/curated_out_of_this_world.jsonl` |
| Prayer, The Art Of Believing | COMPLETE | 7 chapters / 192 paragraphs / 700 raw windows | 21 | section-level | section-level | `[Prayer, The Art Of Believing]/curated_prayer_the_art_of_believing.jsonl` |
| Resurrection, A Confession Of Faith | COMPLETE | 3 chapters / 168 paragraphs / 457 raw windows | 0 | section-level | section-level | `[Resurrection, A Confession Of Faith]/curated_resurrection_a_confession_of_faith.jsonl` |
| Seedtime And Harvest | COMPLETE | 9 chapters / 360 paragraphs / 1,145 raw windows | 23 | section-level | section-level | `[Seedtime And Harvest]/curated_seedtime_and_harvest.jsonl` |
| The Law And The Promise | COMPLETE | Intro + 15 chapters / 798 paragraphs / 3,036 raw windows | 34 | section-level | section-level | `[The Law And The Promise]/curated_the_law_and_the_promise.jsonl` |
| The Power Of Awareness (book) | TODO | — | — | — | — | — |
| The Power Of Awareness (1953 lecture, L0185) | COMPLETE | 32 paragraphs / 375 raw windows | 12 | section-level | section-level | `[The Power Of Awareness]/curated_the_power_of_awareness.jsonl` |
| The Search | TODO | — | — | — | — | — |
| Your Faith Is Your Fortune | TODO | — | — | — | — | — |

## Repository-wide editorial queue

The extraction corpus is now much larger than the original book-only journal. `corpus_progress.json` reports **252 extraction-complete corpus items**: 14 core books, 3 supplementary works, and 235 canonical lectures.

To avoid manual journal maintenance and bureaucratic stops, the strict editorial queue is now **dynamic**:

1. every top-level work folder represented in the completed corpus is considered queued when it has source/worker outputs and does not yet have a completed strict editorial layer;
2. newly added work folders are therefore automatically eligible without requiring a hand-written row here first;
3. the legacy book rows above remain as the current priority sequence;
4. once those are exhausted, the queue continues through the remaining completed works/lectures from the repository tree/registry;
5. a work is removed from the pending queue only after its strict editorial outputs are written and the review is marked complete.

The current repository tree already contains many newly added works beyond the original book list, including `A Divine Event`, `A Lesson In Scripture`, `A Movement Of Mind`, `Mental Diets`, the five lesson transcripts, numerous later lectures, and many Promise-focused works. These are now covered by the dynamic queue rule rather than requiring individual manual insertion before processing.

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

## 2026-08-31 — He Breaks The Shell
Completed a source-first hard editorial pass across the complete 1964 monograph: Introduction + Acts 1–4 + Conclusion.

Why source-first remained appropriate:
- the worker retained 188 candidate windows from 98 canonical paragraphs;
- 34 duplicate groups showed enough overlap that the canonical text remained the authoritative review unit;
- the work is overwhelmingly Promise/spiritual material, so standalone product suitability had to be judged against the stricter automatic-pool policy rather than historical importance alone.

Result:
- canonical paragraphs covered: 98 / 98;
- SELECT exact fragments for the main automatic pool: 0;
- substantive Promise material: HOLD at section level for a future spiritual/Promise opt-in layer;
- scripture/external-dominant or weak standalone units: DROP at section level.

Notable filtering:
- Blake and pure scripture were excluded from Neville attribution;
- resurrection-in-the-skull, supernatural birth, Davidic fatherhood, split-body/serpent, dove, and related mystical descriptions were retained contextually as HOLD rather than converted into context-free maxims;
- categorical identity formulations about God, Christ, and man were held for an opt-in spiritual layer;
- the empty curated file is intentional: this monograph is historically central but no fragment cleared the current main automatic-pool threshold without losing needed theological context.

Files written in the work folder:
- `curated_he_breaks_the_shell.jsonl` (intentionally empty main-pool shortlist)
- `editorial_decisions_he_breaks_the_shell.jsonl`
- `editorial_review_he_breaks_the_shell.md`
- `editorial_complete.json`

Raw candidate and source files were not changed.

## 2026-08-31 — I Know My Father
Completed a source-first hard editorial pass across the complete 1960 10-chapter book.

Why source-first remained appropriate:
- the worker retained 892 candidate windows from 177 canonical paragraphs;
- 86 duplicate groups showed substantial overlap and nested variants;
- the canonical master text was therefore reviewed end-to-end and used as the sole authority for final fragment boundaries.

Result:
- canonical chapters reviewed: 10 / 10;
- canonical paragraphs covered: 177 / 177;
- SELECT exact fragments: 17;
- strict SELECT density vs 892 retained worker candidates: 1.9%;
- strict SELECT density vs 177 canonical paragraphs: 9.6%.

Notable filtering:
- pure scripture and scripture-dominant retellings were excluded from Neville attribution;
- repeated I AM, self-concept, feeling, and present-tense windows were collapsed to preferred exact formulations;
- categorical medical and mental-health healing claims were kept out of the automatic pool;
- passages discouraging reliance on drugs, diet, or money were excluded because they become unsafe or misleading without context;
- categorical financial guarantees, poverty/blame language, political/war causation, and strong universal-causation claims were excluded or held;
- circumcision and crucifixion/resurrection allegory was retained only contextually unless a clean Neville-only fragment stood independently;
- sensory-evidence-denial material was held when decontextualization could encourage ignoring real-world evidence.

Files written in the work folder:
- `curated_i_know_my_father.jsonl`
- `editorial_decisions_i_know_my_father.jsonl`
- `editorial_review_i_know_my_father.md`
- `editorial_complete.json`

Raw candidate and source files were not changed.

## 2026-08-31 — Out Of This World
Completed a source-first hard editorial pass across the complete 1949 four-chapter book.

Why source-first remained appropriate:
- the worker retained 493 candidate windows from 189 canonical paragraphs;
- 73 duplicate groups showed substantial sliding-window overlap;
- the complete canonical master text was reviewed directly so duplicate worker windows did not consume separate editorial passes.

Result:
- canonical chapters reviewed: 4 / 4;
- canonical paragraphs covered: 189 / 189;
- SELECT exact fragments: 20;
- strict SELECT density vs 493 retained worker candidates: 4.1%;
- strict SELECT density vs 189 canonical paragraphs: 10.6%.

Notable filtering:
- pure scripture was excluded from Neville attribution;
- repeated assumption, SATS, wish-fulfilled, attention, and imaginal-action windows were collapsed to the strongest local wording;
- literal fourth-dimensional physics, serial-universe, precognition, and out-of-body claims were held rather than presented as context-free scientific facts;
- medical/healing/sanity claims, absolute external-causation language, and material that could imply blame for painful circumstances were kept out of the automatic pool;
- direct-control-of-others formulations were held for context;
- the long self-quotation from `The Search` was not duplicated into this local curated shortlist.

Files written in the work folder:
- `curated_out_of_this_world.jsonl`
- `editorial_decisions_out_of_this_world.jsonl`
- `editorial_review_out_of_this_world.md`
- `editorial_complete.json`

Raw candidate and source files were not changed.

## 2026-08-31 — Prayer, The Art Of Believing
Completed a source-first hard editorial pass across the complete 1945 seven-chapter book.

Why source-first remained appropriate:
- the worker retained 700 candidate windows from 192 canonical paragraphs;
- 89 duplicate groups showed substantial overlap and nested variants;
- the complete canonical text was reviewed directly and final quote boundaries were taken from the source rather than worker sliding windows.

Result:
- canonical chapters reviewed: 7 / 7;
- canonical paragraphs covered: 192 / 192;
- SELECT exact fragments: 21;
- strict SELECT density vs 700 retained worker candidates: 3.0%;
- strict SELECT density vs 192 canonical paragraphs: 10.9%.

Notable filtering:
- the Tennyson epigraph, scripture, Augustine, and other external wording were excluded from Neville attribution;
- repeated prayer, assumption, fulfilled-desire, imagination, attention, and inner-conversation windows were collapsed to preferred exact fragments;
- pseudo-scientific reversibility, vibration, photophone, telepathy, and thought-transmission explanations were kept contextual rather than treated as scientific facts;
- categorical cure claims, claims superior to medical treatment, remote healing, and passages that could discourage appropriate medical care were excluded from the automatic pool;
- covert suggestion, hypnosis analogies, claims that another person cannot resist, deterministic free-will denial, and behavior-control passages were excluded or held;
- sunburn-from-within, age/decay-as-sleeping-health, poverty-as-sleeping-wealth, victim-blaming, and malicious-thought-rebound claims were excluded;
- `I AM Christ` and related mystical identity passages were held for a future spiritual opt-in layer.

Files written in the work folder:
- `curated_prayer_the_art_of_believing.jsonl`
- `editorial_decisions_prayer_the_art_of_believing.jsonl`
- `editorial_review_prayer_the_art_of_believing.md`
- `editorial_complete.json`

Raw candidate and source files were not changed.

## 2026-08-31 — Resurrection, A Confession Of Faith
Completed a source-first hard editorial pass across the complete 1966 three-chapter title essay.

Why source-first remained appropriate:
- the worker retained 457 candidate windows from 168 canonical paragraphs;
- 55 duplicate groups showed substantial overlap;
- the work is overwhelmingly Promise/spiritual material and contains extensive scripture/external quotation, so canonical-source review avoids both duplication and false Neville attribution.

Result:
- canonical chapters reviewed: 3 / 3;
- canonical paragraphs covered: 168 / 168;
- SELECT exact fragments for the main automatic pool: 0;
- substantive Promise/theological material: HOLD at section level for a future spiritual/Promise opt-in layer;
- pure scripture, external quotations, and weak/context-dependent units: DROP at section level.

Notable filtering:
- pure scripture and wording from William Blake, Johann Scheffler, Edward Thomas, F. W. H. Myers, and other external sources were excluded from Neville attribution;
- Father/Son, David, resurrection, birth-from-above, Golgotha/skull, divine-body, serpent/light, dove, and related mystical descriptions were retained contextually rather than converted into daily maxims;
- categorical supernatural and theological identity claims were held for an opt-in spiritual layer;
- the concise line `Faith is not complete till it has become experience` was not selected because it did not clear the strict author-specificity threshold in isolation;
- the empty curated file is intentional and consistent with the handling of Promise-dominant works such as `He Breaks The Shell`.

Files written in the work folder:
- `curated_resurrection_a_confession_of_faith.jsonl` (intentionally empty main-pool shortlist)
- `editorial_decisions_resurrection_a_confession_of_faith.jsonl`
- `editorial_review_resurrection_a_confession_of_faith.md`
- `editorial_complete.json`

Raw candidate and source files were not changed.

## 2026-08-31 — Seedtime And Harvest
Completed a source-first hard editorial pass across the complete 1956 nine-chapter book.

Why source-first remained appropriate:
- the worker retained 1,145 candidate windows from 360 canonical paragraphs;
- 149 duplicate groups showed substantial overlap and nested variants;
- the complete canonical text was reviewed end-to-end, with final quote boundaries taken from Neville's source wording instead of worker sliding windows.

Result:
- canonical chapters reviewed: 9 / 9;
- canonical paragraphs covered: 360 / 360;
- SELECT exact fragments: 23;
- strict SELECT density vs 1,145 retained worker candidates: 2.0%;
- strict SELECT density vs 360 canonical paragraphs: 6.4%.

Notable filtering:
- scripture and wording from William Blake, Shakespeare, Thoreau, Angelus Silesius, Browning, and other external sources were excluded from Neville attribution;
- repeated `Four Mighty Ones`, final-scene, directed-attention, inner-conversation, and fulfilled-state windows were collapsed to preferred exact formulations;
- the birthmark and sick-cat healing stories, plus categorical healing implications, were excluded from the automatic pool;
- passages attributing accidents, death, discriminatory burial events, poverty, theft recovery, or another person's behavior to an individual's consciousness were excluded or held where decontextualization could become misleading or victim-blaming;
- direct-control-of-others material and testimonials in which another person's behavior is presented as compelled by imaginal action were held;
- stronger claims that the entire physical world is solely a construction of mind were held while clean core metaphysical and practical Neville wording was retained.

Files written in the work folder:
- `curated_seedtime_and_harvest.jsonl`
- `editorial_decisions_seedtime_and_harvest.jsonl`
- `editorial_review_seedtime_and_harvest.md`
- `editorial_complete.json`

Raw candidate and source files were not changed.

## 2026-08-31 — The Law And The Promise
Completed a source-first hard editorial pass across the complete 1961 Introduction + 15 chapters.

Why source-first remained appropriate:
- the worker retained 3,036 candidate windows from 798 canonical paragraphs;
- 357 duplicate groups showed very heavy sliding-window overlap;
- the book contains extensive letters, testimonials, scripture, and external quotations, so canonical review was required to distinguish Neville's own prose from quoted or correspondent wording.

Result:
- canonical sections reviewed: Introduction + 15 chapters;
- canonical paragraphs covered: 798 / 798;
- SELECT exact Neville fragments: 34;
- strict SELECT density vs 3,036 retained worker candidates: 1.1%;
- strict SELECT density vs 798 canonical paragraphs: 4.3%.

Notable filtering:
- correspondent letters and testimonial wording were treated as context/evidence and were not attributed to Neville;
- pure scripture and external wording from Blake, Shakespeare, Yeats, Herbert, Shelley, Rossetti, Fawcett, and other quoted authors were excluded from Neville attribution;
- repeated `imagining creates reality`, `thinking of / thinking from`, wish-fulfilled, revision, mood, and attention windows were collapsed to preferred formulations;
- gambling/race-track stories, categorical financial outcomes, medical cure stories, and material that could discourage appropriate real-world care were kept out of the automatic pool;
- claims assigning imaginal causation to accidents, the Titanic disaster, war, death, legal verdicts, or other people's behavior were excluded or held where decontextualization could become harmful or misleading;
- bilocation, remote-presence, direct mental influence, strong sensory-evidence-denial, and similar context-sensitive passages were held;
- Chapter 15, `The Promise: Four Mystical Experiences`, was reserved for a future spiritual/Promise opt-in layer rather than the main automatic pool.

Files written in the work folder:
- `curated_the_law_and_the_promise.jsonl`
- `editorial_decisions_the_law_and_the_promise.jsonl`
- `editorial_review_the_law_and_the_promise.md`
- `editorial_complete.json`

Raw candidate and source files were not changed.

## 2026-08-31 — The Power Of Awareness (1953 lecture, L0185)
Completed a source-first hard editorial pass across the full 1953-01-01 spoken lecture transcript.

Identity note:
- the folder `[The Power Of Awareness]` is corpus item `L0185`, work class `LECTURE`, not the legacy book of the same title;
- the legacy book remains a separate TODO item until a distinct canonical book source is present in the repository.

Why source-first remained appropriate:
- the worker retained 375 candidate windows from only 32 canonical paragraphs;
- 28 duplicate groups showed heavy overlap among sliding-window variants;
- the complete transcript was reviewed end-to-end and final quote boundaries were taken directly from Neville's own prose.

Result:
- canonical paragraphs covered: 32 / 32;
- SELECT exact Neville fragments: 12;
- strict SELECT density vs 375 retained worker candidates: 3.2%;
- strict SELECT density vs 32 canonical paragraphs: 37.5%.

Notable filtering:
- pure scripture and scripture-dominant paraphrase were excluded from Neville attribution;
- clean state, identity, viewpoint, thinking-from, self-observation, and fulfilled-state formulations were retained;
- Christological and `Second Man` symbolism was held for a spiritual/contextual layer;
- categorical formulations assigning painful circumstances wholly to a person's own choice were excluded from the automatic pool;
- strong sensory-evidence-denial, dimensional-world, direct-influence-of-others, and absolute outer-causation passages were held or dropped where decontextualization could become misleading;
- repeated state/imagination/fulfilled-desire windows were collapsed to preferred exact formulations.

Files written in the work folder:
- `curated_the_power_of_awareness.jsonl`
- `editorial_decisions_the_power_of_awareness.jsonl`
- `editorial_review_the_power_of_awareness.md`
- `editorial_complete.json`

Raw candidate and source files were not changed.

## 2026-08-31 — Dynamic lecture batch L0001–L0005
Completed a five-lecture `SOURCE_FIRST_CANONICAL` editorial batch across the first five pending lecture items in `corpus_registry.json`.

| Corpus ID | Work | Canonical paragraphs | Retained worker windows | SELECT |
|---|---|---:|---:|---:|
| L0001 | A Divine Event | 33 / 33 | 398 | 1 |
| L0002 | A Lesson In Scripture | 27 / 27 | 399 | 2 |
| L0003 | A Movement Of Mind | 26 / 26 | 266 | 2 |
| L0004 | A Movement Within God | 31 / 31 | 398 | 2 |
| L0005 | A Parabolic Revelation | 35 / 35 | 403 | 1 |

Batch result:
- canonical paragraphs reviewed: **152 / 152**;
- retained worker windows reviewed through canonical collapse: **1,864**;
- final main-pool SELECT fragments: **8**;
- all five works now contain `curated_*`, `editorial_decisions_*`, `editorial_review_*`, and `editorial_complete.json`;
- raw candidates, rejected files, master texts, manifests, variations, and worker reports were not changed.

Notable filtering across the batch:
- Promise, Davidic fatherhood, resurrection, birth-from-above, mystical identity, afterlife, and scripture-heavy material was retained mainly as contextual `HOLD` rather than automatic daily content;
- pure scripture and external literary quotations were excluded from Neville attribution;
- categorical health, mental-health, financial, political/war, direct-control-of-others, and universal-causation claims were excluded or held;
- formulations that could become victim-blaming when detached from context were kept out of the main pool;
- clean assumption, feeling, self-persuasion, imaginal-scene, state-transition, and self-concept wording was retained where it remained standalone and exact.

Files written:
- `[A Divine Event]/curated_a_divine_event.jsonl`
- `[A Divine Event]/editorial_decisions_a_divine_event.jsonl`
- `[A Divine Event]/editorial_review_a_divine_event.md`
- `[A Divine Event]/editorial_complete.json`
- `[A Lesson In Scripture]/curated_a_lesson_in_scripture.jsonl`
- `[A Lesson In Scripture]/editorial_decisions_a_lesson_in_scripture.jsonl`
- `[A Lesson In Scripture]/editorial_review_a_lesson_in_scripture.md`
- `[A Lesson In Scripture]/editorial_complete.json`
- `[A Movement Of Mind]/curated_a_movement_of_mind.jsonl`
- `[A Movement Of Mind]/editorial_decisions_a_movement_of_mind.jsonl`
- `[A Movement Of Mind]/editorial_review_a_movement_of_mind.md`
- `[A Movement Of Mind]/editorial_complete.json`
- `[A Movement Within God]/curated_a_movement_within_god.jsonl`
- `[A Movement Within God]/editorial_decisions_a_movement_within_god.jsonl`
- `[A Movement Within God]/editorial_review_a_movement_within_god.md`
- `[A Movement Within God]/editorial_complete.json`
- `[A Parabolic Revelation]/curated_a_parabolic_revelation.jsonl`
- `[A Parabolic Revelation]/editorial_decisions_a_parabolic_revelation.jsonl`
- `[A Parabolic Revelation]/editorial_review_a_parabolic_revelation.md`
- `[A Parabolic Revelation]/editorial_complete.json`

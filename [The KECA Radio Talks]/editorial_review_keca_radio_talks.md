# Editorial Review — The KECA Radio Talks

- **Corpus ID:** `S002`
- **Review mode:** `SOURCE_FIRST_CANONICAL`
- **Authoritative canonical file:** `master_text_keca_radio_talks.txt`
- **Canonical broadcasts reviewed:** 9 / 9
- **Canonical paragraphs reviewed:** 107 / 107
- **Worker windows generated:** 1,793
- **Retained worker windows:** 1,771 (`1,384` candidate + `387` review-recommended)
- **Worker rejected windows:** 22
- **Raw duplicate groups:** 80
- **Strict SELECT fragments:** 22

## Canonical identity

`corpus_registry.json` identifies `S002` as the single supplementary corpus item **The KECA Radio Talks**, work class `RADIO_TALK`, with the alternate title `9 Radio Talks delivered in Los Angeles (1951)`. `[The KECA Radio Talks]/source_manifest.md` defines the authoritative master as the complete nine-broadcast series, totaling 107 canonical paragraphs and approximately 14,225 words.

The nine canonical broadcasts are:

1. *Be What You Wish, Be What You Believe*
2. *By Imagination We Become*
3. *Answered Prayer*
4. *Meditation*
5. *The Law of Assumption*
6. *Truth*
7. *Stone, Water or Wine?*
8. *Feeling Is The Secret (Radio Broadcast)*
9. *Affirm the Reality of Our Own Greatness*

## Source-first coverage

The complete `master_text_keca_radio_talks.txt` was read sequentially from the opening Robert Millikan discussion through the final sentence of Broadcast 9. Worker windows were used only for discovery/provenance and were not treated as canonical coverage because the extraction generated 1,771 retained overlapping windows from only 107 source paragraphs.

The existing 27-fragment editorial package was therefore re-reviewed rather than accepted at face value. After the full canonical reread, the automatic shortlist was reduced to **22 SELECT fragments** and the decision file was upgraded from one whole-series record to an audit summary plus nine broadcast-level records.

## SELECT treatment

The final automatic pool favors the clearest Neville formulations on:

- making the future dream a present mental fact;
- disciplined imagination and sustained attention;
- cultivating virtues rather than merely suppressing impulses;
- prayer as surrender, receptiveness, and a controlled waking dream;
- meditation as controlled imagination plus sustained attention;
- the difference between attention serving a vision and mastering it;
- viewing the world from the fulfilled assumption;
- self-concept as the organizing perspective of experience;
- feeling as the operative element in prayer;
- being rather than merely doing;
- replacing old ideas by fully occupying attention with new ones.

Several stronger canonical fragments missed by the provisional shortlist were added, including the title-defining `Feeling is the secret of successful prayer...`, `The world that moves us is the one we imagine...`, and the Broadcast 9 self-concept question `Who am I? What is my concept of myself?`

## HOLD treatment

Contextual material was held where its value depends on surrounding explanation rather than automatic delivery. This includes scripture-centered interpretation, mystical or theological identity claims, strong literal metaphysical claims, desire-as-divine-voice language, other-directed benevolent imagining, testimonial stories, perception models, and religious definitions of truth.

Broadcast 7, *Stone, Water or Wine?*, is overwhelmingly an exercise in biblical symbolism and religious interpretation. It produced **0 SELECT** for the main automatic pool; that is intentional rather than a completeness failure.

## DROP treatment

The automatic pool excludes:

- pure scripture and external quotations from Millikan, Yeats, Blake, Browning, Emerson, Keats and other quoted voices;
- the Millikan income affirmation as external wording rather than Neville authorship;
- categorical medical/healing causation, including health claims tied directly to mood or prayer;
- financial or guaranteed physical-result formulations;
- unverified university/scientific claims presented as proof of the law of assumption;
- claims that imagination directly dictates or controls another person's behavior;
- victim-blaming or universal event-causation formulations;
- deterministic/no-action claims that become misleading when isolated;
- weak generic slogans, promotional event announcements, and weaker local duplicates.

The earlier short SELECTs `Don't blame; only resolve`, `Love is our birthright`, `Love is the fundamental necessity of our life`, and similarly generic lines were removed because they do not clear the repository's current author-specificity threshold.

## Date note

The canonical registry records `S002` as **1951** (`full_date: 1951-01-01`) and explicitly labels the alternate title as `9 Radio Talks delivered in Los Angeles (1951)`. The source manifest/report also contain 1953 dating language and describe the source tradition as July 1951 / July 1953. The editorial layer preserves the registry year `1951` and records the discrepancy rather than silently rewriting corpus metadata.

## Files written

- `curated_keca_radio_talks.jsonl`
- `editorial_decisions_keca_radio_talks.jsonl`
- `editorial_review_keca_radio_talks.md`
- `editorial_complete.json`

Raw artifacts were not changed: `master_text_keca_radio_talks.txt`, `candidates_keca_radio_talks.jsonl`, `rejected_keca_radio_talks.jsonl`, `report_keca_radio_talks.md`, `source_manifest.md`, `source_variations.md`, and `processing_complete.json` remain untouched.

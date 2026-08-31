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
| Awakened Imagination | TODO | — | — | — | — | — |
| Freedom For All | TODO | — | — | — | — | — |
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

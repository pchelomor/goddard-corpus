# Editorial Review — The KECA Radio Talks

- **Corpus ID:** `S002`
- **Review mode:** `SOURCE_FIRST_CANONICAL`
- **Canonical coverage:** 107 / 107 source paragraphs across all 9 radio talks
- **Retained worker candidates:** 1,771
- **Raw duplicate groups:** 80
- **Strict SELECT fragments:** 27

## Why source-first review was required

The worker extraction produced 1,771 retained windows from only 107 canonical paragraphs, with repeated overlap inside and across talk boundaries. The complete `master_text_keca_radio_talks.txt` was therefore reviewed end-to-end and the canonical text, not the sliding windows, controlled final quotation boundaries.

## Editorial result

The main pool retains clean Neville formulations on self-concept, disciplined imagination, attention, prayer, meditation, love, and inner change. Repeated formulations and promotional/event material were collapsed or excluded.

Scripture-centered explanation, spiritual-identity material, strong universal-causation claims, quasi-scientific or psychological literals, other-directed imaginal demonstrations, and testimonial context were held where they require surrounding explanation. Pure scripture and quotations from named external authors were excluded from Neville attribution.

Categorical medical claims, financial guarantees, victim-blaming or event-causation formulations, claims that imagination directly controls another person, and misleading scientific assertions were kept out of the automatic pool.

## Date note

The canonical registry identifies `S002` as 1951, while the extraction report/source tradition labels the series as 1953 and the text contains period-specific event announcements. This editorial layer preserves the canonical registry year (`1951`) and records the discrepancy rather than silently changing corpus metadata.

## Files written

- `curated_keca_radio_talks.jsonl`
- `editorial_decisions_keca_radio_talks.jsonl`
- `editorial_review_keca_radio_talks.md`
- `editorial_complete.json`

Raw source, candidate, rejected, and processing files were not changed.

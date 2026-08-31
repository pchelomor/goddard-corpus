# Editorial Review — Five Lessons (Master Class)

- **Corpus ID:** `S001`
- **Review mode:** `SOURCE_FIRST_CANONICAL`
- **Canonical coverage:** 858 / 858 source paragraphs across Lessons 1–5 plus the Master Class Q&A
- **Retained worker candidates:** 4,516
- **Raw duplicate groups:** 612
- **Strict SELECT fragments:** 27

## Why source-first review was required

The worker extraction produced thousands of overlapping and nested windows from 858 canonical paragraphs. Treating those windows as independent editorial objects would over-count repeated wording and obscure the source boundaries. The complete `master_text_five_lessons.txt` was therefore reviewed end-to-end, with the canonical text controlling quotation boundaries and attribution.

## Editorial result

The automatic pool retains concise Neville formulations on self-concept, assumption, desire, attention, imaginal action, feeling, and the wish fulfilled when they are clean and self-contained. Repeated formulations across the five lessons and Q&A were collapsed rather than multiplied.

Material centered on scripture exposition, extended biblical allegory, spiritual-identity claims, dimensional or pseudo-scientific explanation, and long teaching demonstrations was held for contextual use. Pure scripture and external quotations were excluded from Neville attribution.

Categorical medical or healing claims, passages discouraging medical or dietary reliance, financial guarantees, victim-blaming or event-causation formulations, and language implying coercive influence or control of other people were kept out of the automatic pool. Testimonial material and mechanically misbounded worker fragments were also excluded where they were not suitable as standalone Neville quotations.

## Files written

- `curated_five_lessons.jsonl`
- `editorial_decisions_five_lessons.jsonl`
- `editorial_review_five_lessons.md`
- `editorial_complete.json`

Raw source, candidate, rejected, and processing files were not changed.

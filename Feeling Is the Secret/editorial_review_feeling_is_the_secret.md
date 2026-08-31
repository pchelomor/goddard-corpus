# Editorial Review — Feeling Is the Secret

## Status
Hard editorial pass completed under `EDITORIAL_POLICY.md`.

## Source reviewed
The strict pass was performed against `candidates_feeling_is_the_secret_curated.jsonl`, which already contains candidate-level source verification and a first editorial classification. The raw extraction files were left unchanged.

## Result
- Reviewed: 88 candidates
- SELECT: 29
- HOLD: 46
- DROP: 13
- Main-pool density: 33.0%

## Main editorial actions
- Removed chapter introductions, generic book-description material, and weak technical transitions.
- Enforced one-preferred-formulation logic inside duplicate idea clusters.
- Kept pure Neville wording in the main pool; mixed scripture passages were moved to HOLD.
- Dropped the categorical medical claim in `fits_ch1_021`.
- Moved strong but context-sensitive metaphysical guarantees, deterministic formulations, and potentially misleading emotion-suppression wording to HOLD.
- Preserved Neville's distinctive metaphysical voice when the quotation was clean, memorable, self-contained, and central to the work.

## Canonical choices inside important duplicate clusters
- `fits_ch1_023` preferred for the change-of-feeling / destiny cluster.
- `fits_ch1_028` preferred for the Chapter 1 wish-fulfilled instruction cluster.
- `fits_ch1_033` preferred for the inside/outside mirror cluster.
- `fits_ch1_036` kept as the strongest “already that which you want to be” formulation.
- `fits_ch2_005` and `fits_ch2_022` retained because they serve different functions: a direct pre-sleep instruction and the chapter's culminating sleep formulation.
- `fits_ch3_015` preferred over the longer play-ending variant `fits_ch3_016`.
- `fits_ch4_004` preferred as the canonical “attract what you are” formulation within this work.
- `fits_ch4_001` preferred over `fits_ch4_002`; `fits_ch4_005` moved to HOLD as an overlapping variant.

## Files produced
- `curated_feeling_is_the_secret.jsonl` — SELECT records only.
- `editorial_decisions_feeling_is_the_secret.jsonl` — decision for all 88 reviewed candidates.
- `editorial_review_feeling_is_the_secret.md` — this summary.

## Next step
Continue work-by-work using the same policy. After every book is completed, run a global cross-book deduplication pass and create the final books master corpus.

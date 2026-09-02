# Neville Goddard Master Corpus — Discrepancies & Issues Registry

This file records textual variations, misattributions, dating conflicts, and editorial discrepancies across editions.

---

## 1. Critical Textual & Attribution Issues

### Issue ISS-001: Web Mirror Script Corruption (Neve Theme Artifacts)
- **Affected Works:** *Feeling Is The Secret*, *At Your Command*, and various lecture mirrors.
- **Description:** Several WordPress mirrors running the 'Neve' theme executed an automated global string replacement replacing the substring \neve with copyright badges (e.g. turning Never into Copyright... r).
- **Resolution:** Normalized against original 1939/1944 print editions.

### Issue ISS-002: Lecture vs. Book Title Overlap (Reprint Detection)
- **Affected Entries:** AT YOUR COMMAND listed in lecture indices.
- **Description:** Some online lecture databases list *At Your Command* as a lecture, but text fingerprinting confirms it is a literal verbatim reprint of the 1939 book.
- **Resolution:** Marked as work_class: BOOK_REPRINT with canonical_parent_id: B001 and status DUPLICATE to prevent redundant quote extraction.

### Issue ISS-003: Distinction between Book and Lecture with Identical Titles
- **Affected Entries:** *Seedtime and Harvest* (Book 1956) vs. *Seedtime and Harvest* (Lecture June 10, 1956); *The Power of Awareness* (Book 1952) vs. *The Power of Awareness* (Lecture 1953 Bailes Church).
- **Description:** Unlike *At Your Command*, Neville occasionally delivered Sunday morning lectures referencing the release or theme of his recent books. Text comparisons reveal distinct spoken lectures with independent content.
- **Resolution:** Maintained as separate canonical entries in their respective classes (BOOK vs LECTURE).

### Issue ISS-004: Posthumous Compilations and Editorial Invasions
- **Affected Entries:** *The Creative Use of Imagination* (S003) and 1980s compilations by J. Watier / DeVorss.
- **Description:** Posthumous compilations frequently smooth, merge, or rephrase Neville's colloquial speech.
- **Resolution:** Assigned work_class: EDITED_COLLECTION and flagged for secondary review; raw historical lecture transcripts take canonical precedence.

### Issue ISS-005: AI Voice Cloning and Modern Synthetic Quotes
- **Affected Scope:** Modern social media, YouTube, Pinterest, quote aggregation websites.
- **Description:** Proliferation of synthetic Neville voice clones, fabricated quotes, and AI summaries.
- **Resolution:** Strict prohibition of secondary quote aggregators. Every quote candidate must be verbatim verified against Tier A/B primary texts.

### Issue ISS-006: Same-Title Collision — *All Things Are Possible* (1967 vs. 1969)
- **Affected Entries:** `L0011` (*All Things Are Possible*, 1967-11-03) and `L0012` (*All Things Are Possible*, 1969-05-12).
- **Description:** The registry contains two distinct lectures with the same base title, but the physical repository originally contained only one undated `[All Things Are Possible]` folder. Its manifest identifies that folder as `L0012`. Before repair, `L0011.date` was correctly `1967-11-03`, while `L0011.full_date` and its source URLs incorrectly pointed to the 1969 lecture. This combination likely caused the 1967 canonical item to be overwritten or skipped during title/slug-based ingestion.
- **Verification:** RealNeville's archive independently lists both `All Things are Possible 11-3-1967` and `All Things are Possible 5-12-1969`; the texts are distinct.
- **Resolution:** Restored `L0011` as a separate dated folder `[All Things Are Possible – 11-03-1967]` with its own canonical master, manifest, source-variation record, and editorial layer. Future ingestion must use `corpus_id` or a date-qualified slug as the physical identity key rather than the bare title.
- **Registry normalization completed (2026-08-31):** `L0011.full_date` and `date` are now `1967-11-03`; its primary/alternate sources point to the 1967 transcript. `L0012.full_date` and `date` are `1969-05-12`; its alternate source now points to the distinct RealNeville `all_things_are_possible2.htm` transcript. The L0012 source manifest cross-check was normalized accordingly.

### Issue ISS-007: Raw/Editorial Corpus-ID Overlay in Same-Title Folders
- **Affected Entries:** `B001` / `L0017` (*At Your Command*) and `B009` / `L0019` (*Awakened Imagination*).
- **Description:** The physical raw folders are keyed by bare title. `[At Your Command]/source_manifest.md` and `processing_complete.json` identify the extraction as `L0017`, while the existing editorial layer in that folder identifies itself as `B001`. Likewise `[Awakened Imagination]/source_manifest.md` and `processing_complete.json` identify the raw extraction as `L0019`, while its existing editorial layer identifies itself as `B009`. Therefore the mere presence of `editorial_complete.json` in a same-title folder is not sufficient evidence that the raw folder's L-ID has been editorially reviewed.
- **L0017 disposition:** Registry classifies `L0017` as `BOOK_REPRINT` with `canonical_parent_id=B001`. Its 118-paragraph master was read end-to-end and contributes zero new SELECT; a corpus-ID-qualified duplicate layer is stored in `[At Your Command – L0017 Reprint]` without overwriting B001.
- **L0019 disposition:** The 33-paragraph L0019 raw master is a distinct 1954 spoken lecture, not the 504-paragraph B009 book. It was reviewed independently and its corpus-ID-qualified derivative layer is stored in `[Awakened Imagination – L0019 Lecture]` without overwriting B009.
- **Resolution rule:** Queue completion must be validated by matching `editorial_complete.json.corpus_id` to the registry item. Same-title books, lectures, and reprints require corpus-ID-qualified storage whenever a bare-title folder already hosts a different editorial identity.

### Issue ISS-008: L0105 Queue Identity Drift — *Love Endureth* vs. stale *Live In The End* record
- **Affected Entry:** `L0105`.
- **Description:** An earlier editorial audit incorrectly recorded `L0105` as *Live In The End* (`1968-07-19`) and marked it `BLOCKED / MISSING_CANONICAL_OBJECT`. The current authoritative `corpus_registry.json`, however, identifies `L0105` as *LOVE ENDURETH* with date `1959-11-13`. The physical repository contains `[Love Endureth]` with `master_text_love_endureth.txt`, source manifest, candidate/rejected sets, worker report, and `processing_complete.json`, all identifying the item as `L0105`.
- **Verification (2026-09-02):** `[Love Endureth]/report_love_endureth.md` and `processing_complete.json` identify `corpus_id: L0105`; the canonical master contains 27 paragraphs and is present at SHA `23c4176a987eb9f2ffd1e633e680d506f525f142`.
- **Editorial impact:** The old `BLOCKED` conclusion was a queue-identity error caused by relying on stale metadata rather than the current corpus-ID registry. It must not suppress the real L0105 object.
- **Resolution:** The stale *Live In The End* blocker is superseded. `L0105 Love Endureth` was reviewed end-to-end under `SOURCE_FIRST_CANONICAL` and given its own corpus-ID-matching editorial package. Future queue audits must resolve identity from the current `corpus_registry.json` first, then verify the physical object by `corpus_id` rather than assuming an older title-to-ID mapping remains current.

### Issue ISS-009: L0165 Canonical Payload Misfile — *The Great Secret* contains *Brazen Impudence*
- **Affected Entries:** `L0165` (*The Great Secret*) and `L0029` (*Brazen Impudence*).
- **Description:** The current registry identifies `L0165` as *The Great Secret* with `full_date: 1969-09-29`, but `[The Great Secret]/master_text_the_great_secret.txt` begins `BRAZEN IMPUDENCE` and the physical report dates the payload `1968-09-27`. Its contents correspond to the separately registered and already editorially complete `L0029 Brazen Impudence`.
- **Editorial impact (2026-09-02):** The physical L0165 payload was read end-to-end for diagnosis, but no quotation from it can be attributed to *The Great Secret*. Duplicate curation would also inflate the three existing L0029 SELECT fragments.
- **Resolution:** `L0165` receives a diagnostic four-file editorial package with `complete:false`, `blocked:true`, `status: BLOCKED_IDENTITY_MISFILE`, and `cross_work_reference: L0029 / Brazen Impudence`. Restore a matching *The Great Secret* canonical master in the source/extraction layer, then rerun `SOURCE_FIRST_CANONICAL` editorial review. The raw misfile is intentionally left unchanged during editorial review.

### Issue ISS-010: L0167 Canonical Payload Misfile — *The Heavenly Vision* contains *By Water And Blood*
- **Affected Entry:** `L0167` (*The Heavenly Vision*).
- **Description:** The registry identifies `L0167` as *The Heavenly Vision* with `full_date: 1968-11-15`, and its source manifest points to the expected Heavenly Vision mirrors. However, `[The Heavenly Vision]/master_text_the_heavenly_vision.txt` begins `BY WATER AND BLOOD` and its complete ~4.5k-word payload is that different lecture. Repository filename/code searches found no separate canonical `By Water And Blood` corpus object to which this payload can safely be reassigned.
- **Editorial impact (2026-09-02):** The single long physical payload was read end-to-end for diagnosis, but none of its wording can be attributed to `L0167 The Heavenly Vision`. The intended Heavenly Vision text therefore remains unreviewed.
- **Resolution:** `L0167` receives a diagnostic four-file editorial package with `complete:false`, `blocked:true`, and `status: BLOCKED_IDENTITY_MISFILE`. Restore a matching *The Heavenly Vision* canonical master (and separately resolve *By Water And Blood* if it belongs in the corpus), then rerun `SOURCE_FIRST_CANONICAL` editorial review. The raw misfile is intentionally left unchanged during editorial review.

### Issue ISS-011: L0226 Canonical Master Explicitly Ends Incomplete — *Who Is The Son Of Man*
- **Affected Entry:** `L0226` (*Who Is The Son Of Man*).
- **Description:** The registry and physical package agree on the work identity, but `[Who Is The Son Of Man]/master_text_who_is_the_son_of_man.txt` literally ends with `(this document ends incomplete)`. This conflicts with `source_manifest.md`, which labels the same object an `Authoritative Full Spoken Lecture Transcript` selected because it is a `Complete verbatim transcription`.
- **Editorial impact (2026-09-02):** All 62 physically available paragraphs were read end-to-end, including the explicit incomplete marker, but the intended lecture cannot be certified as fully reviewed. No quotation is admitted to the curated automatic pool from this incomplete source.
- **Resolution:** `L0226` receives a diagnostic four-file editorial package with `complete:false`, `blocked:true`, `status: BLOCKED_SOURCE_INCOMPLETE`, `canonical_identity_verified:true`, and `source_completeness_verified:false`. Restore or verify a complete canonical master, reconcile the manifest/date metadata as needed, then rerun `SOURCE_FIRST_CANONICAL` editorial review. The raw source is intentionally left unchanged during editorial review.

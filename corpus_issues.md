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

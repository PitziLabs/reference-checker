# Real-Article Test Runs

This directory contains reference lists extracted from real published articles used to validate that the auditor correctly classifies legitimate references as Defensible without over-flagging.

## Validated Articles

Articles with committed source files and completed audit reports.

| Article | Journal | Year | References | Score | Report |
|---|---|---|---|---|---|
| Amarnath & Sharma | IJNTR | 2026 | 20 | 0 (raw −25) | [amarnath-2026-2026-06-15.html](../../reports/amarnath-2026-2026-06-15.html) |
| Madhukar & Bano | IJNTR | 2026 | 5 | 54 | [madhukar-2026-2026-06-15.html](../../reports/madhukar-2026-2026-06-15.html) |

Source PDFs: `IJNTR12020003.pdf` (Amarnath) and `IJNTR12040012.pdf` (Madhukar) are committed in this directory.

**Note on expected scores:** Both articles were published in a low-visibility open-access journal and contain fabricated citations; neither is a clean-reference-list sanity check. See [#3](https://github.com/PitziLabs/reference-checker/issues/3) for the corpus expansion plan that will add clean-reference-list articles for false-positive rate calibration.

## Pending

These articles were planned for testing but have no committed reference-list files or audit reports yet. They are **not** "Tested."

| Article | Journal | Year | Status |
|---|---|---|---|
| Hawkins et al. | JOGNN | 2025 | Pending — no committed artifacts |
| Dziadkowiec et al. | JOGNN | 2025 | Pending — no committed artifacts |
| Cardon & Karr | MCN | 2026 | Pending — no committed artifacts |
| Phan, Bethune, & Lathrop | NWH | 2026 | Pending — no committed artifacts |

Adding these requires committing their reference lists (as `.md` files) and completed audit reports. See [#3](https://github.com/PitziLabs/reference-checker/issues/3).

## Adding a Test Article

1. Extract the reference list from the published article.
2. Save as `[first-author-year].md` (e.g., `hawkins-2025.md`).
3. Run the **v4** auditor prompt against the reference list.
4. Record the score and any false positives in the Validated Articles table above, and link the committed report under `reports/`.
5. If false positives are found, document them and evaluate whether the heuristic needs calibration.

## Success Criteria

A real article with a clean reference list should score between **75 and 90**. Scores below 75 suggest over-flagging (false positives). Scores above 90 are unlikely for reference lists of 20+ citations due to the D × 3 base cost in the scoring formula.

Any reference in a real published article that is classified as **High risk** is a false positive and must be investigated. If it indicates a heuristic calibration issue, file a GitHub Issue.

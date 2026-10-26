# GSTE V0.4 — Output Guide

Read the top-level reports first; consult `debug/` only when deeper diagnostics are needed. Some files may be absent if conversion stops early.

| File | Purpose |
|---|---|
| `GSTE_TAB.musicxml` | Final standard notation and TAB after successful conversion; use this file for playback and manual checking. |
| `CONVERSION_REPORT.md` | Completion summary, not a certification of musical quality. |
| `ERROR_REPORT.md` | Failure stage, error, and available locations and evidence. |
| `HUMAN_REVIEW_REPORT.md` | Recorded fingering, items needing inspection, and priority events not preserved; a warning does not necessarily mean a confirmed error. |
| `MEASURE_LOCATION_GUIDE.md` | Mapping between original measure labels and selection indices. |
| `PRIVACY_SAFE_DEBUG_REPORT.md` | Allowlisted diagnostic summary, recommended as the first attachment for issue reports. |
| `EVENT_LIFECYCLE_TRACE.md` | Concise event-lifecycle diagnostics; still inspect before sharing. |
| `debug/` | Full diagnostics and intermediate outputs, which may contain music, paths, and source information. |

Both successful and failed conversions may generate human review and measure location reports; unavailable evidence is marked as such. Intermediate `04_PRE_FINAL_REVIEW_TAB.musicxml` and `05_TAB.musicxml` do not replace the final top-level score. `debug/ARTIFACT_TRACE.json` records writing, rewriting, and copying sources.

## Locations and Status

Original measure labels follow the input XML; the selection index counts measure order within this input. If the source has been renumbered, reports cannot recover the original full-work numbering. Beat units depend on each diagnostic's definition; missing data is not inferred. Mappings may be incomplete for compressed files or missing measure labels.

`PASS` means only that the particular check passed; `REVIEW` requires verification; `FAIL` means that check failed; `NOT_AVAILABLE` or `UNAVAILABLE` indicates missing evidence. Zero priority events does not prove that the melody is complete. See the [Report Reading Guide](REPORT_READING_GUIDE.md).

## V0.4 beta Output and Index

`GSTE_TAB.musicxml` remains the primary score output. GAR is only a reference view and **does not produce a newly edited score**. Do not assume candidates displayed by GAR have been written to the output file. All existing V0.3 demos are V0.3 automatic conversion results and were not rearranged using GAR.

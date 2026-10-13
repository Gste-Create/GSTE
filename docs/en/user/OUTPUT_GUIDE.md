# GSTE V0.3 — Output Guide

Start with the outer reports. Open `debug/` only when detailed diagnostics are needed. Some files may be absent if conversion stops early.

| File | Purpose |
|---|---|
| `GSTE_TAB.musicxml` | Final standard notation and TAB on success; use for playback and manual review. |
| `CONVERSION_REPORT.md` | Completion summary; not musical-quality certification. |
| `ERROR_REPORT.md` | Failure stage, error, available locations and evidence. |
| `HUMAN_REVIEW_REPORT.md` | Recorded fingering, review-queue and unretained priority-event findings; these are review prompts, not confirmed errors. |
| `MEASURE_LOCATION_GUIDE.md` | Source measure labels mapped to excerpt indices. |
| `PRIVACY_SAFE_DEBUG_REPORT.md` | Allow-list diagnostic summary; preferred first issue attachment. |
| `EVENT_LIFECYCLE_TRACE.md` | Reduced event-lifecycle diagnostics; inspect before sharing. |
| `debug/` | Full diagnostics and intermediate output, potentially containing music, paths and source information. |

Success and failure packages may both contain human-review and measure-location reports. Missing evidence is marked unavailable. Intermediate `04_PRE_FINAL_REVIEW_TAB.musicxml` and `05_TAB.musicxml` do not replace the final outer score. `debug/ARTIFACT_TRACE.json` records write, rewrite and copy provenance.

## Locations and status

Source measure labels come from the input XML. An excerpt index counts measures within the submitted excerpt. Reports cannot recover full-work numbering from renumbered input. Beat units follow the relevant diagnostic; missing values are not inferred. Mappings may be incomplete for compressed files or missing measure labels.

`PASS` applies only to the particular check. `REVIEW` requires inspection. `FAIL` indicates a failed check. `NOT_AVAILABLE` or `UNAVAILABLE` indicates missing evidence. Zero priority events do not prove complete melody retention. See [Report Reading Guide](REPORT_READING_GUIDE.md).

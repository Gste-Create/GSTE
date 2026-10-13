# GSTE V0.3 — Report Reading Guide

Inspect the final score and outer human-review report first. Reports record observations; they do not make additional arrangement decisions.

## Integrity gates

| Gate | Check | Does not establish |
|---|---|---|
| G1 Source | Parsing and source identity structure | Complete interpretation of musical meaning |
| G2 Musical | Priority and possible-melody event retention | Musical quality or human-confirmed melody completeness |
| G3 Export | Final-event serialization, missing and ghost events | Full source-accompaniment retention or physical playability |
| G4 Playback | XML round-trip pitch, timing and string/fret consistency | Tested score-reader rendering or audio |

G3 checks export completeness; consult separate physical diagnostics such as `04_FINAL_FINGERING_REVIEW` for fingering. G4's Playback label does not mean MuseScore playback was tested.

## Reading order

1. Read `CONVERSION_REPORT.md` or `ERROR_REPORT.md` for status and direct evidence.
2. Use `HUMAN_REVIEW_REPORT.md` and `MEASURE_LOCATION_GUIDE.md` to locate review items.
3. For detailed diagnostics, inspect individual results in `debug/00_GSTE_INTEGRITY_GATE.json` and `UNIFIED_RUNTIME_MONITOR.json`; these may also be under `debug/pipeline_output/`.
4. Compare source accompaniment analysis, arrangement candidates, Joint selection, Final Review and final TAB to find the first reduction or change.

`pattern_type` and triplet labels describe locally recognized structures, not guaranteed complete preservation. Source notes, candidates, selected events and final notes are different populations; their counts are not interchangeable retention-ratio denominators. Compare source identities, attacks, chosen octave shifts and final sounding notes.

Even with passing checks, review melody, accompaniment rhythm, harmony, transitions, sustain, rests, fingering and notation. Start issue reports with a shareable reduced summary. Musical-quality problems may still require an authorized minimal score excerpt.

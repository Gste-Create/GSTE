# GSTE V0.4 — Report Reading Guide

Inspect the final score and top-level human review report first. Reports record observations; they do not make new arrangement decisions.

## Integrity Gates

| Gate | What It Checks | What It Does Not Mean |
|---|---|---|
| G1 Source | Parsing and source identification structure | Complete and correct understanding of musical semantics |
| G2 Music | Preservation of priority events and possible melody events | Musical quality or a complete melody confirmed by a person |
| G3 Export | Serialization, loss, and ghost events in the final event sequence | Preservation of all source accompaniment or actual performability |
| G4 Playback | Consistency of pitch, time, string, and fret when XML is read back | Actual visual or audio testing in notation software |

G3 checks export integrity; fingering must be checked separately in physical diagnostics such as `04_FINAL_FINGERING_REVIEW`. The word “Playback” in G4 does not mean the score has been auditioned in MuseScore.

## Reading Order

1. Read `GSTE_TAB` to assess the converted score's musicality and playability.
2. Read `CONVERSION_REPORT.md` or `ERROR_REPORT.md` to confirm status and direct evidence.
3. Use `HUMAN_REVIEW_REPORT.md` and `MEASURE_LOCATION_GUIDE.md` to identify locations requiring verification.
4. For detailed diagnostics, inspect individual results in `debug/00_GSTE_INTEGRITY_GATE.json` and `UNIFIED_RUNTIME_MONITOR.json`; these files may also be under `debug/pipeline_output/`.
5. Compare source accompaniment analysis, arrangement candidates, joint selection, final checks, and final TAB to identify where material was first removed or changed.

`pattern_type` and triplet labels indicate local recognition, not guaranteed preservation of the whole group. Source notes, candidates, selected events, and final notes are different populations; counts from different stages must not be treated as interchangeable denominators for retention rates. Compare source identities, onsets, selected octaves, and notes actually sounding in the final output.

Even when checks pass, verify melody, accompaniment rhythm, harmony, transitions, sustains, rests, fingering, and notation. An issue report may initially include only a privacy-checked summary that you are permitted to share; musical quality issues may still require a minimal authorized score excerpt.

## General Arrangement vs. Developer Debugging

For ordinary arranging, prioritize score playback, comparison with original audio tracks, and the GAR fingering index. Diagnostics/mapping data such as `EVENT_LIFECYCLE_TRACE`, `GSTE_NOTATION_MAP`, and `GSTE_EDITOR_CONTEXT` mainly assist development and issue investigation; ordinary users are not expected to inspect every entry. For bug reports, provide the smallest reproducible data that has passed privacy review when appropriate.

## Candidate Failure Locations vs. Root Causes

Rejection locations from global transposition or octave searches are not necessarily the single true error measure; different candidates may fail in different locations. First compare original measure labels with selection indices, then manually verify range and fingering constraints. A report's PASS status is not musical validation.

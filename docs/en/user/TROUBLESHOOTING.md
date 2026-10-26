# GSTE V0.4 — Troubleshooting

## Installation or Launch Problems

Confirm that you downloaded the GSTE V0.4 EXE installer and completed installation. Launch the program using the installed shortcut. If the problem persists, record your Windows version, GSTE version, whether it occurred during installation or launch, and any error messages or screenshots.

## Conversion Failure

Check the `.musicxml` / `.xml` format, required inputs, and output path. Piano requires separate left- and right-hand files. Ensemble requires a melody and at least one accompaniment; ensure all tracks share the same timeline. `.mxl` and MIDI file formats are not currently supported.

Read `ERROR_REPORT.md` for the cause and failure stage. `NO_VALID_GLOBAL_TRANSFORM` does not necessarily mean that the notes exceed the playable range. For ensemble conversion failures, also record the selected roles, input files, and error messages in the report. Retain the reports and version information for investigation.

## Abnormal Notation After Successful Conversion

Check the top-level `GSTE_TAB.musicxml` first. Use `MEASURE_LOCATION_GUIDE.md` to record the original measure label and selection index, then identify differences in melody, accompaniment, rhythm, or fingering. If there is a problem in notation software, provide its version and distinguish between XML note content and display issues.

Missing locations or `NOT_AVAILABLE` indicate insufficient evidence, not confirmed correctness. See the [Issue Reporting Guide](ISSUE_REPORT_GUIDE.md).

## GAR Not Found / Changes Cannot Be Applied

The GAR index must read `GSTE_EDITOR_CONTEXT` from conversion results produced by the GSTE V0.4 program. Results converted by V0.3 do not contain this file.
GAR is currently read-only. Therefore, changing a chord only changes the index pane, and melody double-stop positions are suggestions shown only within that pane.

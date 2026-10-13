# GSTE V0.3 — Troubleshooting

## Installation or startup problems

Confirm that you downloaded the GSTE V0.3 EXE installer and completed installation. Launch the installed application using its shortcut. If the problem persists, record the Windows version, GSTE version, whether failure occurred during installation or startup, and the error message or screenshot.

## Conversion failure

Check the `.musicxml` / `.xml` format, required inputs and output path. Piano requires two files; Ensemble requires a melody and at least one accompaniment. Align track timelines. Renaming a `.mxl` or MIDI extension does not convert the format.

Read the cause and stage in `ERROR_REPORT.md`. `NO_VALID_GLOBAL_TRANSFORM` does not necessarily indicate a range error. If an Ensemble conversion fails, record the selected roles and inputs along with the reported error. Keep the reports and version information for investigation.

## Unexpected score after successful conversion

Inspect the outer `GSTE_TAB.musicxml`, not only intermediate scores. Record source measure labels and excerpt indices using `MEASURE_LOCATION_GUIDE.md`. Identify whether melody, accompaniment, rhythm or fingering differs. For score-reader problems, include its version and distinguish XML note content from rendering.

Missing locations or `NOT_AVAILABLE` mean insufficient evidence, not confirmed correctness. See [Issue Reporting Guide](ISSUE_REPORT_GUIDE.md).

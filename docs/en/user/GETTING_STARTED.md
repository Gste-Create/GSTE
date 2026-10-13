# GSTE V0.3 — Getting Started

## Install and launch

1. Download the GSTE V0.3 EXE installer from the release download page.
2. Run the downloaded installer and follow its instructions to complete installation.
3. Launch GSTE from the installed application shortcut.

No separate Python installation is required. The application title is GSTE V0.3. The EXE download is an installer; complete installation before using GSTE.

## Prepare inputs

Use uncompressed `.musicxml` or `.xml` files. Open them in a score editor first to confirm they are readable. Export compressed `.mxl` files as uncompressed MusicXML. MIDI is not supported as an end-to-end GUI input in this release.

For Piano and Ensemble, prepare separate files with matching start times, measure positions and time signatures.

## Select a mode

1. **Melody only:** select one melody file, then choose automatic accompaniment or no accompaniment. If the melody moves between piano hands, prepare a separate melody input first. Choosing no accompaniment does not automatically extract all cross-hand melody notes.
2. **Two-hand piano:** select separate melody/right-hand and accompaniment/left-hand files. Accompaniment is analyzed from the source. There is no GUI option to require retention of every accompaniment attack.
3. **Ensemble (experimental):** select one melody and one to four accompaniment files. Assign GUITAR or BASS to each accompaniment. Multiple guitar tracks can use GUITAR, separate lead/rhythm roles are unnecessary. Earlier accompaniment slots have higher fixed fusion weights. This is not a note-retention percentage or a guarantee that every note in an earlier track will be preserved.See [Input Modes](INPUT_MODES.md).

## Convert and review

Select the interface language and output folder, then click Convert. Each GUI conversion creates a result folder. On success, use Open finished score or Open output folder.

Review the melody, rhythm and notation, then inspect fingering and accompaniment using the human-review report. On failure, read `ERROR_REPORT.md`. See [Output Guide](OUTPUT_GUIDE.md).

The language setting changes GUI text. New outer review reports are mainly in Chinese; engineering reports retain English field names.

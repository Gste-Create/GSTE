# GSTE V0.4 beta — Installation and Operation

## Installation and Launch

1. Download the GSTE V0.4 beta EXE installer from the release download page.
2. Run the downloaded installer and follow the on-screen instructions.
3. Launch GSTE using the installed application shortcut.

Python does not need to be installed separately. The downloaded EXE is an installer; complete installation before using the program.

## Preparing Input

Use uncompressed `.musicxml` or `.xml` files and first confirm that your notation software can open them. Save compressed `.mxl` files as uncompressed MusicXML before importing. This GUI release does not provide full MIDI input conversion.

Piano and ensemble modes require separate input files. Ensure that their starting times, measure positions, and time signatures align.

## Selecting a Mode

1. **Melody only:** Select a melody file, then choose automatic accompaniment or no accompaniment. If the melody crosses between the piano hands, prepare it as a separate melody input first; choosing no accompaniment does not mean that all cross-hand melody notes are automatically identified.
2. **Two-hand piano:** Select the melody/right-hand file and the left-hand/accompaniment file separately. Accompaniment is analyzed from the source; there is no GUI option to force preservation of every accompaniment onset.
3. **Ensemble (experimental):** Select the melody and one to four accompaniment files. Assign GUITAR or BASS to each accompaniment. Multiple guitar tracks can share the same role; there is no need to distinguish lead and rhythm guitars. Earlier accompaniment fields have higher fixed fusion weights. These are not note-retention percentages and do not guarantee note-for-note preservation of earlier tracks. See [Input Modes](INPUT_MODES.md).

## Conversion and Inspection

Select the interface language and output directory, then click “Start Conversion.” Each conversion creates a results folder. On success, use “Open Completed Score” or “Open Output Folder.”

Inspect the melody, rhythm, and notation first, then consult the human review report to check fingering and accompaniment. On failure, read `ERROR_REPORT.md`; see the [Output Guide](OUTPUT_GUIDE.md).

Switching languages changes only the interface text. Newly added outer-layer human-readable reports are currently mainly in Chinese; engineering reports still retain English field names.

## V0.4 beta: GAR Arrangement Reference Index (Experimental)

After GSTE conversion, open the arrangement reference index and choose a measure. The integrated “Chord Fingering / Accompaniment Arrangement” index shows candidates near the melody position and on unoccupied strings, with six-line TAB diagrams. These serve as references for available accompaniment strings and positions, including those available after a chord change. Suggested melody double-stop fingerings are also provided.

*Important:* GAR in this release is a read-only reference interface. The index does not directly modify the score or invoke GSTE recalculation, Joint, or the exporter. It must not be treated as a completed semi-automatic score editor. Use a notation editor you are comfortable with for actual changes. GAR provides simplified static fingering references that have not undergone full GSTE Joint validation; its rhythmic onset templates are not reconstructions of the source rhythm.

First-time users can begin with `GSTE_TAB.musicxml` and the GAR index; `debug/` is primarily for investigating software problems. Although ensemble mode has four accompaniment fields, start with one or two tracks and adjust based on what you hear.

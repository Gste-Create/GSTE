# GAR Arrangement Reference — V0.4 beta (Experimental)

## Purpose
GSTE converts MusicXML into fingerstyle guitar notation and TAB for review. GAR provides reference suggestions for fretboard positions, chord fingerings, and accompaniment arrangements, helping users make their own musical decisions based on the original style, listening impressions, and playing ability.

GAR is an arrangement reference tool, not a replacement for score editors such as MuseScore.

## How to Use
1. Convert a MusicXML score with GSTE V0.4 beta and review the generated `GSTE_TAB.musicxml`.
2. Open GAR and choose which conversion result to view:
   - **Most recent conversion:** Open GAR directly to view the score from the conversion you just completed.
   - **Previous conversion:** In GAR, select the `GSTE_EDITOR_CONTEXT` file from an earlier conversion result to load and review that score. You do not need to convert the original score again just to review a previous result.
3. Select a measure to inspect. GAR primarily displays the currently selected measure.
4. Click a melody note in the TAB to view suggested double-stop options.
5. Use the combined **Chord Fingering / Accompaniment Arrangement Reference** to examine candidate placements near the melody's fretboard position, using unoccupied strings, along with six-line TAB illustrations.
6. Evaluate the suggestions according to the musical style, how they sound, and their playability. To make actual changes to the score, use a separate notation editor.

## Important Limitations
**GAR V0.4 beta is a read-only arrangement reference.** Viewing or selecting candidates in GAR does not write changes back to GSTE, run the Joint arrangement process, recalculate the arrangement, or export an edited score.

Candidates are simplified, static references. They are not guaranteed to be physically playable or to match the original score's rhythm exactly. Users should review and adjust them as needed.

## Feedback
Feedback is welcome on voices you would like to preserve, arrangement workflows that could be easier to use, and unsuitable candidate suggestions. When possible, include the software version, measure number, number of source tracks, and expected result. A complete Debug package is not required. Please check the applicable permissions before publicly sharing scores.

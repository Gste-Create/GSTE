# GSTE Beta V0.1 — Current Limitations

The public focus of GSTE Beta V0.1 is to validate the two input paths, core correctness, stability, debuggability, and the basic fingerstyle-guitar arrangement workflow.

Current limitations include:

- The primary input format is MusicXML (`.musicxml` / `.xml`).
- The GUI currently provides **two-hand piano** and **melody-only** input paths.
- The ensemble-score entry is reserved but is not available in Beta V0.1.
- The two-hand piano GUI currently takes two MusicXML files: melody/right hand and left hand/accompaniment.
- The melody-only path uses the current fixed Auto arrangement workflow; general users do not need to configure internal engineering parameters.
- **Input pitch-range limitation:** If the overall interval between the highest and lowest notes in the input score exceeds the range that GSTE can currently map to the guitar, conversion may fail. Scores with a pitch span substantially wider than the range GSTE can accommodate on guitar are not currently guaranteed to convert successfully.
- Automatic arrangements may still contain issues involving musical quality, rhythm, harmony, accompaniment density, position, fingering, or notation layout.
- A successful output does not mean that the result is ready for publication or performance; manual review is still required.
- The Beta `debug/` folder retains more complete engineering diagnostic data and is intended mainly for issue investigation.

# GSTE V0.4 — Current Limitations

- **Input:** The GUI uses uncompressed MusicXML; full MIDI input conversion is not supported. Multitrack input requires separately prepared, aligned files.
- **Ensemble scores:** The experimental mode provides up to four guitar/bass accompaniment fields; the ensemble piano option is hidden. Multitrack fusion needs further testing across more pieces, and quality may vary with accompaniment configuration and source material.
- **Piano source material:** Source-note constraints and per-measure octave shifts do not guarantee preservation of every onset or sustain. Octave selection is not yet globally optimized for hand positions.
- **Rhythm and patterns:** Recognition does not guarantee full understanding or preservation of irregular meters, syncopation, pickups, long-period phrases, or phrases spanning analysis segments.
- **Key and harmony:** Relative major and minor keys may receive similar assessments. Full local modulation, cadence, and harmonic reasoning are not yet optimized.
- **Musical quality:** Material may be omitted. Accompaniment density, fingering, positions, and transitions still require human listening and performance checks.
- **Language:** The GUI supports Traditional Chinese, English, and Japanese. Report summaries may follow the interface language, while raw technical diagnostics may still contain English codes or untranslated content.

Play the converted score in notation software and verify it through human performance.

## Additional V0.4 beta / GAR Limitations

- GAR is currently a **read-only** arrangement reference index, not a mature editor capable of directly applying fingerings, locally recalculating arrangements, or providing full notation editing.
- Fingering and accompaniment templates are references only and have not undergone full GSTE Joint validation. Performability, rhythm, and musicality must be checked manually.
- Ensemble mode provides up to four accompaniment fields; starting with one or two tracks is recommended. Even two tracks may cause substantial compression of musical information.
- This release does not claim across-the-board improvements over V0.3 in automatic arrangement algorithms, musicality, or demo quality.

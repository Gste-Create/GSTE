# GSTE V0.4 — Input Modes and Roles

| Mode | Required Files | Accompaniment Method |
|---|---|---|
| Melody + automatic accompaniment | One melody file | Generated accompaniment |
| Melody + no accompaniment | One melody file | No accompaniment added |
| Piano | Melody/right hand and left hand/accompaniment | Source analysis |
| Ensemble | Melody and one to four accompaniment tracks | Role analysis and fusion |

## Ensemble Guitar

GUITAR is a guitar accompaniment role; multiple guitar tracks may be provided. Strumming, arpeggios, and other patterns are analyzed from musical content, not determined by a lead/rhythm guitar label. The melody must still be provided in a separate file.

Each track receives fixed Harmony/Bass/Texture/Rhythm weights according to its instrument role before accompaniment analysis and fusion. Weights are not note-retention percentages and do not guarantee preservation of an entire track. Source identification distinguishes tracks, but fusion may remove conflicting material. Assigning GUITAR does not guarantee that every strum, arpeggio, or flourish is preserved unchanged.

## Piano Source-Note Policy

Piano defaults to `SOURCE_AT_ATTACK`: accompaniment onset candidates are constrained to source notes at their onset, and the same physical measure uses a common octave shift. Onsets and notes may be omitted, and sustains shortened. Octave selection is based on range, not yet on globally optimized hand positions.

There is currently no mechanism that forces at least one note to be retained at every source accompaniment onset, nor octave shifting for an entire phrase or beat group. This must not be interpreted as a guarantee of equivalent source preservation for every ensemble track.

## V0.4 beta Ensemble Recommendations

Ensemble conversion remains experimental; preservation of musicality must be checked manually.

The ensemble interface accepts up to four GUITAR/BASS accompaniment tracks, but **starting with one or two tracks is recommended**. Prioritize the melody, essential bass notes, and the most important harmonic/rhythmic part. Even two tracks may cause substantial musical compression due to the range, polyphony, and hand-position constraints of a single guitar. Four tracks is an experimental input limit, **not a promise that all four parts will be preserved**. If results are unsatisfactory, adjust the source track separation and compare separate conversions rather than simply adding more tracks.

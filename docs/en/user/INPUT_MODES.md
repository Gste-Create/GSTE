# GSTE V0.3 — Input Modes and Roles

| Mode | Required files | Accompaniment |
|---|---|---|
| Melody + Auto | One melody | Generated |
| Melody + None | One melody | None added |
| Piano | Melody/right hand and accompaniment/left hand | Source analysis |
| Ensemble | One melody and one to four accompaniment tracks | Role analysis and fusion |

## Ensemble guitar

GUITAR is the guitar accompaniment role. Multiple guitar tracks are supported. The program analyzes strumming, arpeggios and other patterns from musical content rather than lead/rhythm labels. The melody remains a separate input.

Place important accompaniment in earlier slots. The program applies a fixed weight to each slot, then combines it with role weights and analysis confidence during fusion. These weights are not note-retention percentages or guarantees of complete track preservation. Tracks retain distinct source identities, but fusion may reduce conflicting material. Selecting GUITAR does not guarantee literal preservation of every strum, arpeggio or flourish.

## Piano source-pitch policy

Piano uses `SOURCE_AT_ATTACK` by default: accompaniment pitch candidates are constrained by source pitches at that attack, with a shared octave shift per physical measure. Attacks and notes may be reduced, and durations may be shortened. Octave selection is based on range rather than global fingering optimization.

Mandatory retention of at least one note at every source accompaniment attack, and phrase-wide or metric-group octave shifting, are unavailable. This Piano policy does not establish identical source-retention guarantees for every Ensemble track.

# GSTE Beta V0.1 — Output Guide

## Successful Conversion

Normal GUI output is intentionally simplified:

```text
Score_Name_GSTE/
├─ GSTE_TAB.musicxml
├─ CONVERSION_REPORT.md
├─ PRIVACY_SAFE_DEBUG_REPORT.md
└─ debug/
```

- **`GSTE_TAB.musicxml`**: Main completed score. This is the first file general users should open.
- **`CONVERSION_REPORT.md`**: Confirms that conversion completed, records the input mode and completed-score location, and reminds the user to review the result manually.
- **`PRIVACY_SAFE_DEBUG_REPORT.md`**: Privacy-safe diagnostic summary intended for issue reporting. It uses an explicit allow-list and excludes score title, source filename/path, pitch, chord, note/rhythm sequences, lyrics, part/track names, raw event/window IDs, musical candidate content, and parameter values.
- **`debug/`**: Stores full engineering diagnostics and intermediate pipeline output. It may contain more detailed score or local-system information. Normal users do not need to inspect every file. **For confidential, commercial, or unpublished works, do not share the entire `debug/` folder by default.**

`CONVERSION_REPORT.md` does not add judgments that GSTE does not directly generate, such as “musical quality passed,” “specific measures must be changed,” or AI-inferred conclusions. Such information should only be added in the future if supported by reliable local algorithms.

> A successful conversion means GSTE completed processing and generated output. It does not guarantee musical, harmonic, fingering, or notation quality. Review the score before performance, publication, or redistribution.

## Failed Conversion

```text
Score_Name_GSTE/
├─ ERROR_REPORT.md
├─ PRIVACY_SAFE_DEBUG_REPORT.md
└─ debug/
   ├─ ERROR_TRACEBACK.txt
   └─ pipeline_output/
```

Read `ERROR_REPORT.md` first. When reporting an issue, **share `PRIVACY_SAFE_DEBUG_REPORT.md` first**. The failed-conversion Privacy-Safe report does not contain traceback, source paths, filenames, exception messages, or score content. Full traceback remains only under `debug/` for local engineering diagnosis.

The Privacy-Safe report reduces data exposure but does not replace NDA, employer, customer, or organizational data-handling requirements. If confidentiality obligations apply, follow those requirements when deciding what can be shared.

## Batch / Development-Test Output

Batch testing and development tools may generate additional summaries, diagnostic files, and intermediate scores. These are development/regression outputs and are not part of the normal GUI user workflow.

## Optional: AI-Assisted Review

GSTE itself does not require AI to convert scores or generate local reports. If you independently use AI to compare source and converted scores or interpret reports, confirm that you have the necessary rights or permission before uploading any score or potentially copyrighted material, and review the selected service's privacy and data-use terms.

Not using AI does not affect normal GSTE conversion, `CONVERSION_REPORT.md`, `ERROR_REPORT.md`, or issue reporting.

See [`../../AI_POLICY.md`](../../AI_POLICY.md) for details.

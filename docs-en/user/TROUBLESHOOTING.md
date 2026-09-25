# GSTE Beta V0.1 — Troubleshooting

## GSTE Does Not Start

1. Launch GSTE from the official Beta installation.
2. Try opening GSTE from the Windows Start menu.
3. If it still does not start, record your Windows version, installation method, and what happened, then report the issue.

## Conversion Fails After Clicking Convert

1. Confirm that the input file is `.musicxml` or `.xml`.
2. Two-hand piano mode requires both the melody/right-hand file and the left-hand/accompaniment file.
3. Melody-only mode requires only the melody file.
4. Check whether `ERROR_REPORT.md` was created in the output folder.
5. When reporting the issue, share `PRIVACY_SAFE_DEBUG_REPORT.md` and a description first. Include `ERROR_REPORT.md` if available. The full `debug/` folder may contain more detailed information; share it only when you have confirmed that it can be shared and the maintainer specifically needs it.

If the input score has an unusually wide pitch span, also check [`CURRENT_LIMITATIONS.md`](CURRENT_LIMITATIONS.md). A score whose overall highest-to-lowest pitch range exceeds what GSTE can currently map to guitar may fail to convert.

## Conversion Succeeds but the Score Is Unsatisfactory

This does not necessarily mean that the program crashed. Record:

- The measure or section where the issue occurs
- Whether the issue involves melody, rhythm, harmony, accompaniment, fingering, position, or notation layout
- If the files can be shared, follow [`ISSUE_REPORT_GUIDE.md`](ISSUE_REPORT_GUIDE.md)

If you submit the original score, make sure you have the right to share it. Consent for AI-assisted debugging of a submitted score is handled separately as described in the issue-reporting guide.

## GUI Language

Traditional Chinese and English change only the GUI text and should not change conversion results. If changing the language affects conversion behavior, report it as a Beta bug.

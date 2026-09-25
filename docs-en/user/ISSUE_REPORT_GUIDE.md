# GSTE Beta V0.1 — Issue Reporting Guide

Thank you for helping test GSTE Beta.

If GSTE fails to convert a score, produces abnormal output, or encounters another problem, provide the information below. You do not need to diagnose the cause yourself; report what actually happened.

## 1. Recommended Information

When reporting an issue, include when possible:

- GSTE Beta version
- Input mode (Piano / Melody)
- Brief problem description
- Whether output was generated successfully
- `PRIVACY_SAFE_DEBUG_REPORT.md` (**recommended first**)
- `ERROR_REPORT.md` (if available)
- Other GSTE-generated diagnostic data only when you have confirmed that it can be shared
- The location of the problem, such as a measure number, when known

If the Privacy-Safe report or error report is sufficient to reproduce or identify the issue, **you do not need to provide the original score or the complete `debug/` folder.**

## 1.1 Two Types of Diagnostic Output

GSTE Beta separates diagnostics into two purposes:

1. **Privacy-Safe Debug Report (default for issue reporting):** Uses an allow-list and retains only version, status, stage/diagnosis, engineering-health counts, candidate counts, diagnostic flags/areas, and anonymized window IDs. It intentionally excludes score title, source filename/path, pitch, chord, note/rhythm sequences, lyrics, part/track names, raw event/window IDs, musical candidate content, and parameter values.
2. **Full Engineer Debug:** Retained under `debug/` and pipeline output for deeper local diagnosis. It may contain more detailed musical content, paths, candidates, or parameter information. **Do not treat it as data that can automatically be published or submitted to a third-party AI service.**

For commercial, NDA-protected, internal-company, or unpublished scores, provide only `PRIVACY_SAFE_DEBUG_REPORT.md` first. Even Privacy-Safe reports remain subject to your contracts, employer/customer requirements, and organizational data policies.

## 2. Describe What You Observed

Examples:

- Conversion stopped before completion
- No output file was generated
- Rhythm is incorrect in a measure
- Melody pitch differs from the source score
- TAB fingering is abnormal
- Playback contains a sound not shown in the score
- The application does not start
- The GUI does not respond

You do not need to determine which module, algorithm, or error category caused the issue. Diagnosis is handled during debugging.

## 3. Do You Need to Submit the Score?

**Not necessarily.**

Start with GSTE-generated error reports and diagnostic data. If they are sufficient to locate the problem, the original score is not required.

Some issues may require comparing:

`Original MusicXML → GSTE internal processing → Final output`

In that case, the maintainer may request:

- Original input MusicXML
- GSTE-generated MusicXML / TAB
- Other output files related to the issue

**Only submit scores that you have the right to share.**

## 4. AI-Assisted Debugging and Scores

Normal GSTE score conversion **does not require AI**.

During normal use, input MusicXML scores are not automatically submitted to AI as part of the conversion process.

AI may be used during GSTE development and issue debugging.

Submitting a score to reproduce an issue **does not automatically mean that you consent to AI analysis of that score.**

If AI assistance is needed to analyze the submitted score, your choice must be obtained separately.

### If your report includes a score, select one:

- [ ] **I agree that the submitted score may be used for AI-assisted debugging.**
- [ ] **I do not agree that the submitted score may be used for AI-assisted debugging.**

If you do not explicitly select “I agree,” the submitted score **should not be used for AI-assisted analysis**.

Declining AI-assisted analysis **does not affect normal GSTE use or your ability to report an issue**.

You may still submit:

- `PRIVACY_SAFE_DEBUG_REPORT.md` (preferred)
- `ERROR_REPORT.md`
- Other GSTE diagnostic data that you have confirmed can be shared
- Problem description
- Screenshots
- Other information you choose to provide

See [`../../AI_POLICY.md`](../../AI_POLICY.md) for details.

## 5. Copyright and Privacy

Do not submit:

- Scores that you do not have the right to share
- Passwords
- API keys
- Authentication tokens
- Sensitive personal information
- Confidential company information
- Other content that you do not want to make public or provide to the maintainer

If the issue can be reproduced using a public-domain or otherwise appropriately licensed test score, prefer that material.

## 6. Suggested Report Format

**GSTE Version:**  
Beta V0.1

**Input Mode:**  
Piano / Melody

**Problem:**  
Briefly describe what actually happened.

**Problem Location:**  
For example: Measure 24 (if known)

**Output Generated:**  
Yes / No

**Attached Files:**  
For example: `PRIVACY_SAFE_DEBUG_REPORT.md`, `ERROR_REPORT.md`

**Score Attached:**  
Yes / No

**AI-assisted score debugging consent (only if a score is attached):**

- [ ] I agree
- [ ] I do not agree

**Additional Information:**  
Any other information that may be useful.

## 7. Reporting Principle

GSTE Beta issue reports focus on **actual results**.

Users do not need to understand GSTE's internal algorithms or classify the error themselves.

Tell us:

**“What you provided → What happened → What you actually received”**

The debugging process handles the remaining diagnosis and analysis.

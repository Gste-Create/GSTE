# GSTE V0.4 — Issue Reporting Guide

Thank you for helping test GSTE beta. Describe what actually happened; you do not need to determine the responsible module, algorithm, or error category yourself.

## Recommended Information

- GSTE version and input mode: piano, melody + automatic accompaniment, melody + no accompaniment, or ensemble.
- Brief description of the problem and whether output was generated.
- Preferably provide `PRIVACY_SAFE_DEBUG_REPORT.md` first.
- If `ERROR_REPORT.md` is available, review its contents before sharing it.
- Provide other diagnostic files only after confirming they may be shared.
- Known problem locations, such as measure numbers.

If concise diagnostics are sufficient, there is no need to submit the original score or the entire `debug/` directory.

## Two Types of Diagnostic Output

**Privacy-safe debug report:** Uses allowlisted fields, including version, status, stages and diagnostics, engineering health counts, candidate counts, diagnostic flags and regions, and anonymized analysis-segment identifiers. It excludes titles, source filenames and paths, pitches, chords, note and rhythm sequences, lyrics, voice and track names, raw event and segment identifiers, musical candidate contents, and parameter values.

**Full engineering diagnostics:** Stored in `debug/` and pipeline outputs for in-depth local debugging. They may include musical content, paths, candidates, and parameters, and must not be considered safe to publish or submit directly to third-party AI systems.

For commercial collaborations, nondisclosure agreements, internal works, or unreleased works, provide the privacy-safe report first. Even concise reports must comply with contractual, organizational, employer, and client data policies.

## Describe the Actual Symptoms

For example: conversion stops midway, no output, incorrect measure rhythm, changed melody pitch, abnormal TAB fingering, playback sounds not present in the score, failure to launch, or an unresponsive interface.

## Is a Score Required?

Not necessarily. Start with the error report and concise diagnostics. Some problems require comparing the original MusicXML, intermediate processing, and final output to locate the first discrepancy; maintainers may then request the input MusicXML, converted score, or other relevant outputs.

Submit only scores you have permission to share. If a problem can be reproduced, prefer public-domain or appropriately licensed test material.

## AI-Assisted Debugging

Normal GSTE conversion does not require AI and does not automatically submit input MusicXML to AI. AI may be used in software development and debugging.

Submitting a score does not constitute consent to AI analysis. When a report includes a score, choose one:

- [ ] I consent to AI-assisted debugging using the score submitted with this report.
- [ ] I do not consent to AI-assisted debugging using the score submitted with this report.

Without explicit consent, submitted scores must not be used for AI-assisted analysis. Declining does not affect normal use or issue reporting. You may still provide concise reports, reviewed error reports, other shareable diagnostics, descriptions, screenshots, and any information you choose to share. See `AI_POLICY.md` in the release package for the full policy.

## Copyright and Privacy

Do not submit scores you lack permission to share, passwords, API keys, authentication credentials, sensitive personal data, company secrets, or content you do not wish to disclose to maintainers or the public.

## Issue Report Template

**GSTE version:** V0.3  
**Input mode:** Piano / Melody + automatic accompaniment / Melody + no accompaniment / Ensemble  
**Problem:** Describe the observed behavior.  
**Problem location:** Original measure label and selection index (if known).  
**Output generated:** Yes / No  
**Attachments:** List filenames.  
**Score attached:** Yes / No  
**Consent to AI-assisted debugging (complete when attaching a score):**

- [ ] Consent.
- [ ] Do not consent.

**Additional information:** Include useful context.

## V0.4 Reporting Details

Record the accompaniment mode and the role and order of each ensemble field. Provide the original measure label and selection index. For notation display or playback problems, include the notation software version.

`HUMAN_REVIEW_REPORT.md` and `MEASURE_LOCATION_GUIDE.md` can help locate problems but are not privacy summaries. `ERROR_REPORT.md` may include source paths, error text, and locations. Read the [Sharing Guide](SHARING_GUIDE.md) before attaching files.

Explain what you entered, what happened, and what you actually obtained; leave root-cause location and error classification to the debugging process.

## V0.4 beta: Feedback on Musicality and the Interface Is Welcome

In addition to software bugs, we welcome feedback on: (1) which measure/source track was insufficiently preserved; (2) which bass notes, chord colors, or rhythms you wanted to preserve; (3) which GAR candidates are unintuitive; and (4) how you would like to make manual changes. Please include version, input mode, number of accompaniment tracks, problem measure, actual and expected results. You may attach screenshots or short score excerpts that you are authorized to share. **A full debug package or unauthorized work is not required.** Feedback does not guarantee inclusion in the next release.

# GSTE V0.3 — Issue Reporting Guide

Thank you for testing GSTE Beta. Describe the result you observed; you do not need to identify the responsible module, algorithm or error category.

## Recommended information

- GSTE version and input mode: Piano, Melody + Auto, Melody + None or Ensemble.
- A short problem description and whether output was generated.
- `PRIVACY_SAFE_DEBUG_REPORT.md` as the preferred first attachment.
- `ERROR_REPORT.md`, if available, after checking its contents.
- Other diagnostic files only after confirming they can be shared.
- The problem location, such as a measure number, when known.

If reduced diagnostics are sufficient, there is no need to submit the source score or the complete `debug/` folder.

## Two diagnostic outputs

**Privacy-Safe Debug Report:** an allow-list summary containing version, status, stage/diagnosis, engineering-health counts, candidate counts, diagnostic flags/areas and anonymized window IDs. It excludes titles, source filenames and paths, pitches, chords, note/rhythm sequences, lyrics, part/track names, original event/window IDs, musical candidate content and parameter values.

**Full Engineer Debug:** detailed local diagnostics in `debug/` and pipeline output. These may contain musical content, paths, candidates and parameters. Do not treat them as automatically suitable for public sharing or third-party AI.

For commercial, confidential, NDA-covered or unpublished scores, start with the privacy-safe report. Even reduced reports must comply with your contracts and organization, employer and client data policies.

## Describe what happened

Examples include conversion stopping, no output, incorrect rhythm in a measure, a changed melody pitch, unusual TAB fingering, playback sounds absent from the notation, failure to launch or an unresponsive interface.

## Are scores required?

Not always. Begin with error reports and reduced diagnostics. Some problems require comparison of the source MusicXML, internal processing and final output to locate the first difference. Maintainers may then request the input MusicXML, converted MusicXML/TAB or relevant output files.

Submit only scores you have the right to share. Prefer public-domain or appropriately licensed test material when it reproduces the problem.

## AI-assisted debugging

Normal GSTE conversion does not require AI and does not automatically submit input MusicXML to AI. AI may be used for software development and debugging.

Submitting a score does not itself authorize AI analysis. If a report includes a score, state your choice:

- [ ] I consent to use of the scores submitted with this report for AI-assisted debugging.
- [ ] I do not consent to use of the scores submitted with this report for AI-assisted debugging.

Without explicit consent, submitted scores must not be used for AI-assisted analysis. Declining does not affect normal GSTE use or issue reporting. You may still submit reduced reports, inspected error reports, other shareable diagnostics, descriptions, screenshots and other information you choose to provide. See `AI_POLICY.md` in the release package for the full policy.

## Copyright and privacy

Do not submit scores you cannot share, passwords, API keys, authentication tokens, sensitive personal information, company secrets or anything you do not want disclosed to maintainers or the public.

## Report template

**GSTE version:** V0.3  
**Input mode:** Piano / Melody + Auto / Melody + None / Ensemble  
**Problem:** Describe the observed behavior.  
**Problem location:** Source measure label and excerpt index, if known.  
**Output generated:** Yes / No  
**Attached files:** List the files.  
**Score attached:** Yes / No  
**AI consent, if scores are attached:**

- [ ] I consent.
- [ ] I do not consent.

**Additional information:** Include any useful context.

## V0.3 details

Record the accompaniment mode and each Ensemble slot's role and order. Give both source measure labels and excerpt indices. Include the score-reader version for rendering or playback problems.

`HUMAN_REVIEW_REPORT.md` and `MEASURE_LOCATION_GUIDE.md` can help locate problems but are not privacy-safe summaries. `ERROR_REPORT.md` may contain source paths, error text and locations. See [Sharing Guide](SHARING_GUIDE.md) before attaching files.

Explain what you entered, what happened and what result you received. Leave diagnosis and error classification to the debugging process.

# GSTE Beta V0.2 — 問題回報指南

[繁體中文](#繁體中文) · [English](#english)

## 繁體中文
若不希望提供音高、和弦或逐音節奏，預設只上傳檢查過的 `PRIVACY_SAFE_DEBUG_REPORT.md`；必要時加 `CONVERSION_REPORT.md`。JSON 版可取代 MD，不需整個 debug。

**EVENT_LIFECYCLE_TRACE 沒有音高，但有逐音節奏與延音資訊，不屬於這個預設回報範圍。**
逐項檔案分類、連統計也不提供時的做法，請閱讀 [AI_SHARING_GUIDE.md](AI_SHARING_GUIDE.md)。

描述版本、模式、操作與實際結果即可，不需要猜測是哪一層出錯。只有在你願意提供該類內容時，才補充來源或轉換譜、事件追蹤、音檔或畫面。
`ERROR_REPORT.md`、traceback 與錯誤截圖可能含檔名、路徑與例外內容，請先遮蔽。完整 debug 不是預設附件。
只分享有權分享的素材；提供樂譜不自動同意維護者轉交第三方 AI，見 [AI_POLICY.md](../../AI_POLICY.md)。

## English

If you do not wish to disclose pitches, chords or per-note timing, share only the inspected PRIVACY_SAFE_DEBUG_REPORT.md by default; add an inspected CONVERSION_REPORT.md if needed. The JSON counterpart can replace the MD. Do not include the entire debug folder.

**EVENT_LIFECYCLE_TRACE has no pitches but contains per-note timing and sustain information. It is outside this default reporting scope.**

Read [AI_SHARING_GUIDE.md](AI_SHARING_GUIDE.md) for the file-by-file classification and options when even statistics must remain private.

Describe the version, mode, actions and actual result; you do not need to guess the failing layer. Add source / output scores, event traces, audio or screenshots only when you choose to disclose that content.

ERROR_REPORT.md, tracebacks and error screenshots may contain filenames, paths and exception text. Redact them first. Full debug data is not a default attachment.

Share only material you have permission to share. Supplying a score does not automatically authorize the maintainer to send it to third-party AI; see [AI_POLICY.md](../../AI_POLICY.md).

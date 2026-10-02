# GSTE Beta V0.2 — 輸出結果指南

[繁體中文](#繁體中文) · [English](#english)

## 繁體中文
本次樣本根目錄包含 `GSTE_TAB.musicxml`、`CONVERSION_REPORT.md`、`PRIVACY_SAFE_DEBUG_REPORT.md`、`EVENT_LIFECYCLE_TRACE.md` 與 `debug/`。成功／失敗或其他模式的檔案仍可能不同。

- MusicXML：主要樂譜，含音樂資訊，必須人工核對顯示、播放、節奏、延音與指法。
- CONVERSION_REPORT：流程摘要；本次沒有逐音內容。
- PRIVACY_SAFE_DEBUG_REPORT：精簡診斷，保留統計但不輸出逐音音高／時間。
- EVENT_LIFECYCLE_TRACE：逐音流程追蹤，含開始／結束與延音資訊；沒有音高不代表沒有音樂資訊。
- debug：完整工程資料，多個檔案包含音高、和弦、節奏或譜面。

分享前請依 [AI_SHARING_GUIDE.md](AI_SHARING_GUIDE.md) 選擇檔案。成功輸出不代表已通過全部音樂性與閱讀器驗證。

## English

The inspected sample's result root contains GSTE_TAB.musicxml, CONVERSION_REPORT.md, PRIVACY_SAFE_DEBUG_REPORT.md, EVENT_LIFECYCLE_TRACE.md and debug/. Other modes and successful / failed runs may produce different files.

| File | Purpose and content |
|---|---|
| MusicXML | Main score containing musical content. Manually check display, playback, rhythm, sustain and fingering. |
| CONVERSION_REPORT | Workflow summary; the inspected sample has no per-note content. |
| PRIVACY_SAFE_DEBUG_REPORT | Reduced diagnostics retaining statistics without per-note pitch/time in the inspected sample. |
| EVENT_LIFECYCLE_TRACE | Per-note workflow trace with start/end and sustain information. Absence of pitch does not mean absence of music information. |
| debug/ | Full engineering data; many files contain pitches, chords, rhythm or notation. |

Use the [AI sharing guide](AI_SHARING_GUIDE.md) to choose files before sharing. A successful export is not a complete musical-quality or reader-validation pass.

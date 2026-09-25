# GSTE Beta V0.1 — 輸出結果指南 / Output Guide

## 成功轉換 / Successful conversion

一般 GUI 使用者的輸出已刻意簡化：

```text
歌曲名稱_GSTE/
├─ GSTE_TAB.musicxml
├─ CONVERSION_REPORT.md
├─ PRIVACY_SAFE_DEBUG_REPORT.md
└─ debug/
```

- **`GSTE_TAB.musicxml`**：主要完成樂譜。一般使用者優先開啟此檔。
- **`CONVERSION_REPORT.md`**：確認轉換已完成、輸入模式與完成樂譜位置，並提醒人工確認結果。
- **`PRIVACY_SAFE_DEBUG_REPORT.md`**：預設問題回報用的隱私安全診斷摘要。使用白名單欄位，不輸出曲名、來源檔名/路徑、pitch、chord、note/rhythm sequence、lyrics、part/track 名稱、原始 event/window ID、音樂候選內容或參數值。
- **`debug/`**：保存完整工程診斷與 pipeline 中間輸出，可能包含較詳細的樂譜或本機資訊。正常使用不需要逐一閱讀；**保密、商業合作或未公開作品請勿直接分享整個 `debug/` 資料夾。**

`CONVERSION_REPORT.md` 不會列出程式目前沒有直接產生的判定，例如「音樂性通過」、「特定小節必須修改」或 AI 推測結果。這些內容若未來有可靠的本機演算法支援，再另行加入。

> 轉換成功代表 GSTE 已完成處理並產生輸出，不代表所有音樂性、和聲、指法或排版均已保證正確。演奏、公開或再散布前仍請人工確認。

## 轉換失敗 / Failed conversion

```text
歌曲名稱_GSTE/
├─ ERROR_REPORT.md
├─ PRIVACY_SAFE_DEBUG_REPORT.md
└─ debug/
   ├─ ERROR_TRACEBACK.txt
   └─ pipeline_output/
```

請先閱讀 `ERROR_REPORT.md`。回報問題時，**優先提供 `PRIVACY_SAFE_DEBUG_REPORT.md`**。失敗版 Privacy-Safe report 不包含 traceback、來源路徑、檔名、例外訊息或樂譜內容。完整 traceback 仍只保存在 `debug/` 供本機工程除錯。

Privacy-Safe report 是降低資料暴露的技術措施，不取代 NDA、雇主、客戶或組織的資料處理規範；有保密義務時仍應依相關規範決定是否可分享。

## Batch / 開發測試輸出

批次測試與開發工具可能產生額外 summary、診斷檔與中間樂譜。這些是開發／Regression 用輸出，不代表一般 GUI 使用者需要閱讀的檔案。

## 選用：AI 輔助判讀 / Optional AI-assisted review

GSTE 本身不需要 AI 才能完成轉換或產生本機報告。使用者若自行使用 AI 協助比較原譜、轉換譜或解讀報告，在上傳任何樂譜或可能受著作權保護的內容前，請先確認自己具有提供該資料給所選服務所需的權利或許可，並閱讀該服務的隱私與資料使用條款。

不使用 AI 不影響 GSTE 的正常轉換、`CONVERSION_REPORT.md`、`ERROR_REPORT.md` 或問題回報。

詳細規則請參閱 [`../../AI_POLICY.md`](../../AI_POLICY.md)。

---

## English summary

For normal GUI use, open `GSTE_TAB.musicxml` and read `CONVERSION_REPORT.md`. For issue reporting, share `PRIVACY_SAFE_DEBUG_REPORT.md` first. It is generated from an explicit allow-list and excludes score title, source filename/path, pitches, chords, note/rhythm sequences, lyrics, part/track names, raw event/window IDs, musical candidate content, and parameter values. The full `debug/` folder may contain more detailed score or local-system information and should not be shared for confidential projects unless permitted.

A successful conversion means GSTE completed processing and generated the output. It does not guarantee musical, harmonic, fingering, or notation quality. Please review the score before performance, publication, or redistribution.

Batch/development tools may create additional diagnostic files. They are not part of the normal user-facing workflow.

AI-assisted interpretation is optional. Before uploading scores or copyrighted material to a third-party AI service, confirm that you have the necessary rights or permission and review that service's privacy and data-use terms.

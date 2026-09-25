# GSTE Beta V0.1 — 問題回報指南

感謝協助測試 GSTE Beta。

如果 GSTE 發生轉換失敗、輸出異常或其他問題，請依照本文件提供相關資訊。你不需要自行判斷問題原因，只要提供實際發生的結果即可。

## 1. 建議提供的資料

回報問題時，建議提供：

- GSTE Beta 版本
- 使用的輸入模式（Piano / Melody）
- 問題簡述
- 是否成功產生輸出
- `PRIVACY_SAFE_DEBUG_REPORT.md`（**建議優先提供**）
- `ERROR_REPORT.md`（若有）
- 其他 GSTE 自動產生的相關診斷資料（僅在你確認可以分享時）
- 必要時提供問題發生位置，例如小節編號

若問題可以只靠 Privacy-Safe report 或錯誤報告重現或判斷，**不需要提供原始樂譜，也不需要提供完整 `debug/` 資料夾。**


## 1.1 兩種診斷輸出

GSTE Beta 會區分兩種診斷用途：

1. **Privacy-Safe Debug Report（預設回報用）**：使用白名單欄位，只保留版本、狀態、stage/diagnosis、工程健康計數、candidate count、診斷 flags/areas 與匿名化 window ID。刻意排除曲名、來源檔名/路徑、pitch、chord、note/rhythm sequence、lyrics、part/track 名稱、原始 event/window ID、音樂候選內容與參數值。
2. **Full Engineer Debug（完整工程診斷）**：保留於 `debug/` 與 pipeline output，供本機深入除錯。它可能包含較詳細的音樂內容、路徑、候選或參數資訊，**不要把它視為可直接公開或可直接交給第三方 AI 的資料。**

若樂譜來自商業合作、NDA、公司內部或未公開作品，請先只提供 `PRIVACY_SAFE_DEBUG_REPORT.md`。即使是 Privacy-Safe report，也應遵守你的合約、雇主、客戶與組織資料政策。

## 2. 建議的問題描述方式

請盡量描述實際看到的現象，例如：

- 轉換中途停止
- 沒有產生輸出檔案
- 某一小節節奏錯誤
- 主旋律音高與原譜不同
- TAB 指法異常
- 出現譜面上不存在的播放聲音
- 程式無法開啟
- GUI 沒有反應

不需要自行判斷問題屬於哪個程式模組、哪個演算法或哪種錯誤分類，這些工作會在除錯階段處理。

## 3. 是否需要提供樂譜？

**不一定。**

建議先提供 GSTE 產生的錯誤報告與診斷資料。如果這些資訊已足以定位問題，就不需要提供原始樂譜。

某些問題可能必須比較：

`原始 MusicXML → GSTE 內部處理 → 最終輸出`

才能確認第一個發生差異的位置。

這種情況下，維護者可能會請你另外提供：

- 原始輸入 MusicXML
- GSTE 產生的 MusicXML / TAB
- 與問題相關的其他輸出檔案

**請只提交你有權分享的樂譜。**

## 4. AI 輔助除錯與樂譜

GSTE 的正常樂譜轉換流程**不需要 AI**。

一般使用 GSTE 時，輸入的 MusicXML 樂譜不會因為正常轉換流程而自動提交給 AI。

AI 可能被用於 GSTE 的程式開發與問題除錯。

如果你主動提交樂譜協助重現問題，**提交樂譜本身不代表同意將樂譜提供給 AI 分析。**

只有在需要使用 AI 協助分析該樂譜時，才需要另外取得你的選擇。

### 如果此次回報包含樂譜，請選擇：

- [ ] **同意將此次提交的樂譜用於 AI 輔助除錯**
- [ ] **不同意將此次提交的樂譜用於 AI 輔助除錯**

若未明確選擇「同意」，提交的樂譜**不應用於 AI 輔助分析**。

不同意 AI 輔助分析**不影響 GSTE 的正常使用，也不影響問題回報**。

你仍然可以提交：

- `PRIVACY_SAFE_DEBUG_REPORT.md`（優先）
- `ERROR_REPORT.md`
- 你確認可以分享的其他 GSTE 診斷資料
- 問題描述
- 截圖
- 其他你願意提供的資訊

詳細說明請參閱 [`../../AI_POLICY.md`](../../AI_POLICY.md)。

## 5. 著作權與隱私

請不要提交：

- 你沒有權利分享的樂譜
- 密碼
- API keys
- Authentication tokens
- 個人敏感資訊
- 公司機密資料
- 其他不希望公開或提供給維護者的內容

如果可以使用公共領域（Public Domain）或其他具有適當授權的測試樂譜重現問題，建議優先使用這類樂譜。

## 6. 建議回報格式

**GSTE Version:**  
Beta V0.1

**Input Mode:**  
Piano / Melody

**Problem:**  
請簡單描述實際發生的問題。

**Problem Location:**  
例如：Measure 24（若知道）

**Output Generated:**  
Yes / No

**Attached Files:**  
例如：`PRIVACY_SAFE_DEBUG_REPORT.md`、`ERROR_REPORT.md`

**Score Attached:**  
Yes / No

**AI 輔助樂譜除錯同意（只有附上樂譜時需要選擇）：**

- [ ] 同意
- [ ] 不同意

**Additional Information:**  
其他你認為有幫助的資訊。

## 7. 回報原則

GSTE Beta 的問題回報以**實際結果**為主。

使用者不需要理解 GSTE 的內部演算法，也不需要自行分類錯誤。

請告訴我們：

**「輸入了什麼 → 發生了什麼 → 實際得到什麼」**

其餘的問題定位與分析交由除錯流程處理。

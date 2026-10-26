# GSTE V0.4 — 輸出指南

先閱讀外層報告，需要深入診斷時再查看 `debug/`。若轉換過早停止，部分檔案可能不存在。

| 檔案 | 用途 |
|---|---|
| `GSTE_TAB.musicxml` | 成功後的最終五線譜與六線譜，播放及人工核對應使用此檔。 |
| `CONVERSION_REPORT.md` | 完成摘要，不是音樂品質認證。 |
| `ERROR_REPORT.md` | 失敗階段、錯誤、可取得的位置與證據。 |
| `HUMAN_REVIEW_REPORT.md` | 已記錄的指法、待檢查項目與未保留的優先事件；提醒不代表確定錯誤。 |
| `MEASURE_LOCATION_GUIDE.md` | 原譜小節標籤與選段序號對照。 |
| `PRIVACY_SAFE_DEBUG_REPORT.md` | 白名單診斷摘要，建議優先作為問題回報附件。 |
| `EVENT_LIFECYCLE_TRACE.md` | 精簡事件生命週期診斷，分享前仍須檢查。 |
| `debug/` | 完整診斷與中間輸出，可能包含音樂、路徑與來源資訊。 |

成功與失敗結果皆可能產生人工檢查及小節定位報告；缺少證據時標示未提供。中間的 `04_PRE_FINAL_REVIEW_TAB.musicxml` 與 `05_TAB.musicxml` 不取代外層最終樂譜。`debug/ARTIFACT_TRACE.json` 記錄寫入、改寫與複製來源。

## 定位與狀態

原譜小節沿用輸入 XML 的標籤；選段序號計算本次輸入內的小節順序。來源若已重新編號，報告無法恢復原全曲編號。拍點單位依各診斷定義，缺少資料不推測。壓縮檔或缺少小節標籤時，對照可能不完整。

`PASS` 僅表示該項檢查通過；`REVIEW` 需要核對；`FAIL` 表示該項檢查失敗；`NOT_AVAILABLE` 或 `UNAVAILABLE` 表示缺少證據。優先事件為零不代表已證明旋律完整，詳見[報告判讀](REPORT_READING_GUIDE.md)。

## V0.4 beta 的輸出與索引

`GSTE_TAB.musicxml` 仍是主要樂譜輸出；GAR 索引只是參考畫面，**不會生成經人工修改的新譜**。不要將 GAR 顯示的候選視為已寫入輸出檔。既有 V0.3 Demo 均為 V0.3 自動轉換結果，未使用 GAR 重新編曲。

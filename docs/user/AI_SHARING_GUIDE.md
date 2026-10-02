# GSTE Beta V0.2 — 提供 AI／公開回報的檔案選擇
本表已核對本次原始碼與 Chopin 診斷樣本。相同檔名在其他版本不保證內容相同。

## 不希望 AI 讀取音高、和弦或逐音節奏時
預設只單獨提供 `PRIVACY_SAFE_DEBUG_REPORT.md`，必要時加上 `CONVERSION_REPORT.md`。若工程除錯需要結構化資料，可用 `debug/PRIVACY_SAFE_DEBUG_REPORT.json` 取代 MD；不必兩者都提供。
將檔案複製到中性名稱的資料夾後單獨上傳，不要上傳以曲名命名的整包 ZIP。先打開檢查內容，不在附言或截圖補上不想提供的樂譜資料。

|檔案／資料|本次內容與風險|不提供音符／節奏時是否可上傳|
|---|---|---|
|`PRIVACY_SAFE_DEBUG_REPORT.md`|沒有曲名、來源路徑、音高、和弦、逐音 onset/release 或歌詞；有診斷狀態、匿名窗口順序、候選數、問題統計|優先提供；仍需檢查|
|`debug/PRIVACY_SAFE_DEBUG_REPORT.json`|與上述 MD 相同的精簡診斷，另有結構化欄位|可單獨提供；不要連同整個 debug|
|`CONVERSION_REPORT.md`|本次只有版本、成功狀態、模式及固定輸出檔名|本次可提供；其他回報先檢查是否含錯誤或路徑|
|`EVENT_LIFECYCLE_TRACE.md`|逐音開始／結束、角色、選取狀態、延音段數；MD 本次可呈現局部事件，不能因為沒音高就視為沒音樂資訊|不提供|
|`debug/EVENT_LIFECYCLE_TRACE.json`|完整事件生命週期，含逐音開始／結束與實際輸出時間|不提供|
|`GSTE_TAB.musicxml`、其他 MusicXML／MIDI／音檔／譜面截圖|實際樂譜或可聽／可見音樂內容|不提供|
|`ERROR_REPORT.md`、`debug/ERROR_TRACEBACK.txt`、錯誤視窗截圖|可能含來源路徑、檔名、例外文字及音樂內容|不直接提供；先手動遮蔽，優先改用精簡失敗報告|
|`debug/ARTIFACT_TRACE.json`|本次僅固定輸出名與 writer/postprocessor，未見逐音內容；原始碼 source 欄位會取 final.name|非預設回報；這份樣本可在檢查後補充，其他版本須核對來源檔名|
|完整 `debug/`、`debug/pipeline_output/`、整個輸出 ZIP|混有音高、和弦、節奏、指法、樂譜及細部解析|不提供|
|其他未列為可提供的 JSON／MD／TXT|未因副檔名或名稱自動去識別化|預設不提供|

本次含音樂內容的例子：`14_event_dump.json`、`10_joint_candidates.json`、`21_SERIALIZER_MELODY_MANIFEST.json`、`22_GPT_HUMAN_REVIEW_PACKET.json`、`ENGINEER_DEBUG_SUMMARY.json`、`melody_path_candidates.json`，以及 pipeline_output 中的角色、Bass/Harmony/Rhythm/Texture 意圖與譜面檔案。`GPT_HUMAN_REVIEW_PACKET` 的用途就是協助讀取音樂問題，不是無音樂內容包。`PUBLIC_EXPORT_SANITIZER` 清理中繼資料，也不代表樂譜音符被移除。

## 連音樂推導統計也不想提供時
精簡報告仍含 108 個匿名診斷窗口（本次樣本）、候選數、問題類型等由樂譜推導的資料。若連這些統計也不願分享，就不要提供 PRIVACY_SAFE_DEBUG_REPORT；只提供本次已檢查的 CONVERSION_REPORT，或手動描述版本、Windows 版本、模式、是否成功與不涉及樂譜的現象。若連模式都不能透露，只手動提供必要的操作環境與軟體錯誤現象。

## 能除錯到什麼程度
精簡報告適合確認工程狀態、失敗類型與大致問題區段；無法完整確認旋律、節奏、和聲或逐音正確性。若需要追逐音 release mutation，EVENT_LIFECYCLE_TRACE 就有幫助，但那表示你選擇提供節奏時間資訊。
提交問題不等於同意維護者把另行提供的樂譜交給第三方 AI。若你直接上傳檔案到 AI 服務，該服務就會接收你選擇提供的內容。

## 程式防護的限制
精簡報告產生器採欄位白名單，但 status、flags、diagnostic_areas 等字串沒有嚴格值白名單。人工將敏感字串放入上游 summary 時，實測會被帶入報告；這不是此次樣本已洩漏的證據，而是目前不能保證任意來源或未來改動都安全的原因。分享前仍須檢查。

## English
For reporting without note pitches, harmony or per-note timing, share the inspected `PRIVACY_SAFE_DEBUG_REPORT.md` (or its JSON counterpart) and, if needed, the inspected `CONVERSION_REPORT.md`. Do not share event lifecycle traces, complete debug folders, MusicXML, MIDI, audio or score screenshots. Reduced reports still reveal diagnostic statistics. If those are also confidential, provide only a manually reviewed general description of the software issue. Review content and filenames before sharing.

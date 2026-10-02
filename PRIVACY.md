# GSTE Beta V0.2 隱私說明

## 本機轉換
本次檢查 src 原始碼的 imports 與相關呼叫，未發現 requests、urllib、socket 等網路傳輸匯入或桌面流程的自動上傳。這是原始碼靜態檢查，未完成 EXE 與 source 的 build 一致性驗證、Windows 網路監測或防毒掃描，因此不是二進位永不連網的保證。建置腳本需要下載 pip／Nuitka 依賴，與使用者桌面轉換是不同流程。

## 診斷與音樂資訊
**沒有音高，不代表沒有音樂資訊。** EVENT_LIFECYCLE_TRACE 包含逐音 onset/release 與延音段數，不能在不提供節奏資訊時分享。
本次 PRIVACY_SAFE_DEBUG_REPORT 的 JSON 已由原始碼重新產生，與附件完全一致；本次內容沒有曲名、來源路徑、音高、和弦、歌詞或逐音時間，但含匿名診斷窗口、候選數與問題統計。若連音樂推導統計也不能提供，就不要分享此報告。
欄位白名單不是所有字串值的白名單；目前產生器會傳遞 status、flags 與 area 字串，未來或非標準輸入仍可能帶入敏感文字。使用者分享前須檢查內容與檔名。
完整 debug、錯誤文字、MusicXML、音檔、截圖與輸出 ZIP 可能含樂譜或個資，不能預設公開。

完整選檔表與最少回報方式見 [docs/user/AI_SHARING_GUIDE.md](docs/user/AI_SHARING_GUIDE.md)。

## AI 與公開提交
GSTE 桌面轉換不需要提交樂譜給 AI。公開 GitHub 回報可被他人取得，請只提供有權公開的內容。提供問題或樂譜，不自動授權維護者把另行提供的樂譜轉交第三方 AI；需另外取得該次同意，見 AI_POLICY.md。直接將檔案上傳 AI 則該服務會接收該檔案。

## English
The reviewed source did not show desktop network-upload imports/calls, but the executable was not proven to match this source and was not dynamically monitored. Reduced debug reports omit per-note pitch and timing in the inspected sample, while retaining diagnostic statistics. Event lifecycle traces include musical timing. Always inspect contents and filenames; full debug files are not public by default. See the AI sharing guide for the exact file selection policy.

# GSTE Beta V0.1 隱私說明 / Privacy Notice

## 中文
### 本機處理
GSTE Beta V0.1 的正常樂譜轉換流程在使用者電腦本機執行，不需要將輸入樂譜提交給 AI。此版本不提供帳號、telemetry、analytics、crash upload 或雲端樂譜處理功能。

### 問題回報與診斷
公開 GitHub Issues、Discussions 或 Pull Requests 應視為公開內容。請勿提交個人敏感資訊、登入憑證、公司機密、無權公開的原始碼或樂譜。

`PRIVACY_SAFE_DEBUG_REPORT.md` 是預設問題回報檔，採白名單輸出並排除曲名、來源檔名/路徑、pitch、chord、note/rhythm sequence、lyrics、part/track 名稱、原始 event/window ID、音樂候選內容與參數值。完整 `debug/` 供本機工程除錯，可能包含較詳細資訊，不應預設公開。

Privacy-Safe report 是降低資料暴露的技術措施，不是法律或 NDA 保密認證。

### AI 協作
GSTE 執行轉換本身不依賴 AI。專案開發、程式 review、除錯、測試與文件整理可能使用 AI 輔助，但由人類決定需求、版本與發布。使用者提交樂譜並不自動同意 AI 分析；若維護者需要把該樂譜交由第三方 AI 服務協助除錯，應取得該次提交的明確同意。詳見 `AI_POLICY.md`。

若未來加入網路傳輸、帳號、telemetry、analytics 或雲端處理，本文件必須在該功能發布前更新。

## English
### Local processing
Normal score conversion in GSTE Beta V0.1 runs locally on the user's computer and does not require submitting the input score to AI. This release does not provide accounts, telemetry, analytics, crash upload, or cloud score processing.

### Issue reports and diagnostics
Information posted to public GitHub Issues, Discussions, or Pull Requests should be treated as public. Do not submit sensitive personal information, credentials, confidential company data, proprietary source code, or scores you are not authorized to share.

`PRIVACY_SAFE_DEBUG_REPORT.md` is the default issue-report file. It uses an allow-list and excludes score title, source filename/path, pitch, chord, note/rhythm sequences, lyrics, part/track names, raw event/window IDs, musical candidate content, and parameter values. The full `debug/` folder is intended for local engineering diagnostics and may contain more detailed information; it should not be treated as public by default.

The Privacy-Safe report is a data-minimization measure, not a legal or NDA confidentiality certification.

### AI collaboration
GSTE does not depend on AI to perform score conversion. AI tools may assist project development, code review, debugging, testing, and documentation, while requirements, validation, version decisions, and releases remain human-reviewed. Submitting a score does not automatically authorize AI analysis. If the maintainer needs to provide that score to a third-party AI service for debugging, explicit consent for that submission should be obtained. See `AI_POLICY.md`.

If future releases add network transmission, accounts, telemetry, analytics, or cloud processing, this notice must be updated before those features are released.

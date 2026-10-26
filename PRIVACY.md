# GSTE V0.4 beta 隱私說明 / Privacy Notice

## 中文
### 本機處理
GSTE V0.4 beta 的正常樂譜轉換流程在使用者電腦本機執行，不需要將輸入樂譜提交給 AI。此版本不提供帳號、telemetry、analytics、crash upload 或雲端樂譜處理功能。

### 問題回報與診斷
公開 GitHub Issues、Discussions 或 Pull Requests 應視為公開內容。請勿提交個人敏感資訊、登入憑證、公司機密、無權公開的原始碼或樂譜。

`PRIVACY_SAFE_DEBUG_REPORT.md` 是預設問題回報檔，採白名單輸出並排除曲名、來源檔名/路徑、pitch、chord、note/rhythm sequence、lyrics、part/track 名稱、原始 event/window ID、音樂候選內容與參數值。完整 `debug/` 供本機工程除錯，可能包含較詳細資訊，不應預設公開。

Privacy-Safe report 是降低資料暴露的技術措施，不是法律或 NDA 保密認證。

### AI 協作
GSTE 執行轉換本身不依賴 AI。專案開發、程式 review、除錯、測試與文件整理可能使用 AI 輔助，但由人類決定需求、版本與發布。使用者提交樂譜並不自動同意 AI 分析；若維護者需要把該樂譜交由第三方 AI 服務協助除錯，應取得該次提交的明確同意。詳見 `AI_POLICY.md`。

若未來加入網路傳輸、帳號、telemetry、analytics 或雲端處理，本文件必須在該功能發布前更新。

## English
### Local processing
Normal score conversion in GSTE V0.4 beta runs locally on the user's computer and does not require submitting the input score to AI. This release does not provide accounts, telemetry, analytics, crash upload, or cloud score processing.

### Issue reports and diagnostics
Information posted to public GitHub Issues, Discussions, or Pull Requests should be treated as public. Do not submit sensitive personal information, credentials, confidential company data, proprietary source code, or scores you are not authorized to share.

`PRIVACY_SAFE_DEBUG_REPORT.md` is the default issue-report file. It uses an allow-list and excludes score title, source filename/path, pitch, chord, note/rhythm sequences, lyrics, part/track names, raw event/window IDs, musical candidate content, and parameter values. The full `debug/` folder is intended for local engineering diagnostics and may contain more detailed information; it should not be treated as public by default.

The Privacy-Safe report is a data-minimization measure, not a legal or NDA confidentiality certification.

### AI collaboration
GSTE does not depend on AI to perform score conversion. AI tools may assist project development, code review, debugging, testing, and documentation, while requirements, validation, version decisions, and releases remain human-reviewed. Submitting a score does not automatically authorize AI analysis. If the maintainer needs to provide that score to a third-party AI service for debugging, explicit consent for that submission should be obtained. See `AI_POLICY.md`.

If future releases add network transmission, accounts, telemetry, analytics, or cloud processing, this notice must be updated before those features are released.


## 新增報告 / New reports

`HUMAN_REVIEW_REPORT.md`、`MEASURE_LOCATION_GUIDE.md`、`ERROR_REPORT.md`、最終／中間樂譜與完整 `debug/` 不列為預設可分享的精簡檔。原始錯誤文字可能含路徑；位置對照可能揭露來源小節。精簡檔仍須由使用者確認。詳見 [分享指南](docs/user/SHARING_GUIDE.md)。

Human-review, measure-location, error reports, scores and full diagnostics are not reduced safe-sharing attachments by default. Error strings can contain paths and location maps can expose source numbering. Review reduced reports too.


---

## 日本語

### ローカル処理
GSTE V0.4 beta の通常の変換は利用者の PC 内で実行されます。この版はアカウント、テレメトリー、利用解析、クラッシュの自動アップロード、クラウドでの楽譜処理を提供しません。

### 診断情報の共有
GitHub の公開 Issue 等は公開情報として扱ってください。`PRIVACY_SAFE_DEBUG_REPORT.md` は共有向けに情報を制限したレポートで、曲名、ファイル名・パス、音高、和音、音符・リズム列、歌詞、トラック名、元のイベント ID、音楽候補とパラメータ値などを除外する設計です。ただし共有前の確認が必要で、法的な秘密保持認証ではありません。`debug/` 全体には詳細な情報が含まれる場合があります。

### AI
通常の変換は AI を必要としません。提出した楽譜を第三者 AI に提供するには、その都度明示的な同意が必要です。今後ネットワーク送信やクラウド機能を追加する場合、公開前にこの文書を更新する必要があります。

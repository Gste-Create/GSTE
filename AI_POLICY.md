# GSTE AI 協作與使用政策 / AI Collaboration & Use Policy

## 中文
GSTE V0.4 beta 的正常樂譜轉換為本機程式流程，**不需要 AI，也不會因正常轉換自動把輸入樂譜提交給 AI**。

本專案在開發過程中會使用 AI 作為協作工具，例如程式分析、除錯、測試設計、文件整理與報告閱讀。AI 的輸出不視為自動正確；功能需求、架構方向、音樂目標、Regression、發布內容與最終判斷仍由人類審查。

使用者也可以自行選擇 AI 協助閱讀 GSTE 報告或比較樂譜，但這不是 GSTE 必要流程。將樂譜或其他內容提供給第三方 AI 服務前，使用者應確認自己有權分享，並自行閱讀該服務的隱私與資料使用條款。

提交問題給 GSTE 維護者時，**提交樂譜不代表自動同意 AI 分析**。若維護者需要將該樂譜提供給第三方 AI 服務協助除錯，應另外取得使用者對該次提交的明確同意。不同意時仍可使用 `PRIVACY_SAFE_DEBUG_REPORT.md` 與問題描述；錯誤報告及截圖需先檢查是否含可分享內容回報。

公開提交到 repository 的 Issues、Pull Requests、一般 logs、測試結果與文件可能由 AI 協助 review。請勿提交密碼、API keys、tokens、個人敏感資訊、公司機密、無權公開的原始碼或無權分享的樂譜。

## English
Normal score conversion in GSTE V0.4 beta is a local software workflow. **It does not require AI and does not automatically submit input scores to AI.**

AI tools may assist project development, including code analysis, debugging, test design, documentation, and report interpretation. AI output is not treated as automatically correct; requirements, architecture, musical goals, regression validation, release contents, and final decisions remain human-reviewed.

Users may independently choose an AI service to help read GSTE reports or compare scores, but this is optional. Before providing scores or other content to a third-party AI service, users should confirm that they have the right to share the material and review that service's privacy and data-use terms.

When reporting an issue to the GSTE maintainer, **submitting a score does not automatically authorize AI analysis**. If the maintainer needs to provide that score to a third-party AI service for debugging, explicit consent for that submission should be obtained separately. Users who decline can still report issues using `PRIVACY_SAFE_DEBUG_REPORT.md` and written descriptions; inspect error reports and screenshots for shareable content first.

Public repository Issues, Pull Requests, general logs, test results, and documentation may be reviewed with AI assistance. Do not submit passwords, API keys, tokens, sensitive personal information, confidential company data, proprietary source code, or scores you are not authorized to share.


---

## 日本語

GSTE V0.4 beta の通常の楽譜変換はローカルで実行され、AI を必要とせず、入力楽譜を自動的に AI サービスへ送信しません。

開発ではコード解析、デバッグ、テスト設計、文書整備などに AI を補助的に利用する場合があります。ただし要件、音楽的な判断、回帰テスト、公開の最終判断は人が行います。利用者が外部 AI へ楽譜やレポートを共有する場合は、自身の権利と当該サービスのデータ利用条件を確認してください。

維持管理者へ楽譜を提出しても、第三者 AI での分析への自動同意にはなりません。そのような利用には別途明示的な同意が必要です。公開 Issue や Pull Request に機密情報、認証情報、許諾のない楽譜を添付しないでください。

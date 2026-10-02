# GSTE — Guitar Score Transcription Engine

**GSTE Beta V0.2** 是一套將 MusicXML 樂譜轉換為可供人工檢查與後續編修的 **指彈吉他（fingerstyle guitar）TAB / MusicXML** 的桌面軟體。

> Beta 版本以功能驗證與回報實際結果為主。轉換成功代表程式完成處理並產生輸出，不代表編曲、節奏、指法或樂譜格式在所有作品上皆已保證正確。

## 目前支援範圍

- **雙手鋼琴模式**：分別輸入右手／主旋律與左手／伴奏 MusicXML，重新配置為指彈吉他樂譜。
- **Melody 模式**：輸入主旋律 MusicXML，可依目前 GUI 提供的選項進行轉換。
- **僅主旋律轉換**：可不加入 GSTE 自動伴奏，適合希望保留輸入音符、進行吉他指板配置的用途。
- 輸出 MusicXML / TAB，桌面版設計為本機轉換；本次未動態驗證網路行為。
- 團譜路徑目前尚未公開。

## 重要使用注意事項

GSTE 目前仍有適用範圍。雙手鋼琴模式主要針對「主旋律主要位於右手、左手主要提供 Bass／和聲／伴奏」的樂譜。若作品的主要旋律頻繁跨越左右手、兩手皆包含不可省略的旋律材料，或原譜織度高度依賴鋼琴延音與多聲部關係，目前版本可能無法得到理想結果。

例如《月光奏鳴曲第一樂章》這類旋律與織度跨越雙手、且大量音符關係需要共同保留的作品，目前不列為 Piano 模式的成功示範曲目。這類作品可視需求嘗試整理成單一路徑後使用「僅主旋律／不加自動伴奏」方式，但仍需人工確認結果。

請勿把「成功產生 MusicXML」視為樂譜已通過音樂性或可演奏性審核。演奏、發布或再散布前，請以 MuseScore 或其他 MusicXML 閱讀器開啟並人工檢查。

## 快速開始

第一次使用請閱讀 [`docs/user/GETTING_STARTED.md`](docs/user/GETTING_STARTED.md)。

基本流程：

`MusicXML → GSTE → GSTE_TAB.musicxml → 人工檢查`

## Demo 政策

Repository 的 `demo/` 收錄經來源權利核對的 **9 組成功轉換結果（Melody 8、Piano 1）**，並附對應 Input 與來源材料。詳見 [Demo 清單](demo/README.md)及[權利索引](demo/DEMO_LICENSE_INDEX.md)。這些案例尚未宣稱音樂性全部人工通過；不適合目前演算法或來源權利不明的作品已移出公開包。

原作已進入 Public Domain，**不代表網路取得的特定數位樂譜檔一定可以重新散布**。只有在來源檔本身具有可確認的 Public Domain、CC0 或其他允許再散布的授權時，才建議連同 Input 一起公開。來源授權不明時，不應把該 Input 檔放入公開 Demo。

GSTE 產生的樂譜應標示為 **GSTE-generated output / GSTE 轉換結果**，不可表示為原作曲家的原始吉他編曲。

## 問題回報

發生失敗或結果異常時，請先檢查敏感內容，再提供 `PRIVACY_SAFE_DEBUG_REPORT.md` 與實際現象。不要自行猜測是哪一層演算法造成問題。詳見 [`docs/user/ISSUE_REPORT_GUIDE.md`](docs/user/ISSUE_REPORT_GUIDE.md)。

## Music Rights

使用者有責任確認自己對輸入、修改、演奏、公開與散布的樂曲及特定樂譜版本具有必要權利。網路可下載不等於可自由再散布。

---

## English summary

GSTE Beta V0.2 converts MusicXML into fingerstyle-guitar TAB/MusicXML for review and further editing. Piano mode is currently best suited to scores where the principal melody is mainly in the right hand and the left hand primarily supplies bass, harmony, or accompaniment. Scores with essential melodic material distributed across both hands may not convert reliably with the current Piano workflow.

A successful conversion only means that GSTE completed processing and produced output. Always review the generated score before performance, publication, or redistribution.

For public demos, the public-domain status of the underlying composition does not by itself establish redistribution rights for a particular digital score file. Publish source/input files only when the rights of that specific edition/file are sufficiently clear.

## 本次檢查與發布狀態
請閱讀 SECURITY_REVIEW.md。尚不能宣稱此二進位已獲無惡意程式、零個資風險或不侵權認證。MIDI 未確認為公開功能，團譜仍未開放。

## 不提供音樂內容的回報
預設只提供檢查後的 PRIVACY_SAFE_DEBUG_REPORT.md，必要時加 CONVERSION_REPORT.md。EVENT_LIFECYCLE_TRACE 含逐音節奏，不在這個範圍。完整分類見 [docs/user/AI_SHARING_GUIDE.md](docs/user/AI_SHARING_GUIDE.md)。

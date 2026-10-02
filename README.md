# GSTE — Guitar Score Transcription Engine

[繁體中文](#繁體中文) · [English](#english)

## 繁體中文
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


## 本次檢查與發布狀態
請閱讀 SECURITY_REVIEW.md。尚不能宣稱此二進位已獲無惡意程式、零個資風險或不侵權認證。MIDI 未確認為公開功能，團譜仍未開放。

## 不提供音樂內容的回報
預設只提供檢查後的 PRIVACY_SAFE_DEBUG_REPORT.md，必要時加 CONVERSION_REPORT.md。EVENT_LIFECYCLE_TRACE 含逐音節奏，不在這個範圍。完整分類見 [docs/user/AI_SHARING_GUIDE.md](docs/user/AI_SHARING_GUIDE.md)。

## English

GSTE Beta V0.2 is a desktop application that converts MusicXML scores into fingerstyle-guitar TAB / MusicXML for manual review and further editing.

> This Beta focuses on validating features and collecting real conversion results. A successful conversion means processing completed and an output was generated; it does not guarantee arrangement, rhythm, fingering or notation correctness for every work.

### Supported workflows

- **Two-hand Piano mode:** supply separate right-hand / melody and left-hand / accompaniment MusicXML files, then rearrange them for fingerstyle guitar.
- **Melody mode:** supply a melody MusicXML file and select the options available in the GUI.
- **Melody-only conversion:** convert without GSTE-generated accompaniment, for preserving input notes and assigning them to guitar positions.
- MusicXML / TAB output. The desktop workflow is designed for local conversion; network behavior has not been dynamically verified in the recorded review.
- Group-score processing is not available in the public release.

### Important limitations

Piano mode is intended primarily for scores where the melody is mainly in the right hand and the left hand supplies bass, harmony or accompaniment. Results may be unsuitable when essential melody frequently crosses hands, both hands contain indispensable melodic material, or the texture depends heavily on piano sustain and multiple voices.

Moonlight Sonata, first movement, is therefore not included as a successful Piano demo. Where appropriate, reorganize such material into a single input and try melody-only conversion without automatic accompaniment, then review the result manually.

Generating a MusicXML file successfully is not a musical-quality or playability approval. Open the output in MuseScore or another MusicXML reader before performance, publication or redistribution.

### Quick start

Read the bilingual [installation and GUI guide](docs/user/GETTING_STARTED.md). Workflow: MusicXML → GSTE → GSTE_TAB.musicxml → manual review.

### Demo policy

The repository includes **9 successful conversions (8 Melody, 1 Piano)** with matching inputs and source materials selected after source-rights review. See the [demo list](demo/README.md) and [rights index](demo/DEMO_LICENSE_INDEX.md). These cases have not all passed a manual musical-quality review. Works unsuitable for the current algorithm or with unclear source rights were excluded.

A public-domain composition does not automatically make a particular downloaded digital edition redistributable. Publish inputs only when that edition has an identifiable public-domain declaration, CC0 dedication or another applicable permission to redistribute. Do not publish inputs with unclear source rights.

Label generated scores **GSTE-generated output**, not the composer's original guitar arrangement.

### Reporting problems

Inspect and redact sensitive information, then provide PRIVACY_SAFE_DEBUG_REPORT.md and describe what happened. You do not need to guess which algorithm layer failed. See the [issue reporting guide](docs/user/ISSUE_REPORT_GUIDE.md).

### Music rights

Users must have the rights required to input, modify, perform, publish and distribute the work and its particular score edition. Availability for download is not permission to redistribute.

### Recorded review and release status

Read [SECURITY_REVIEW.md](SECURITY_REVIEW.md). The reviewed binaries have not been certified malware-free, free of personal-data risks or non-infringing. MIDI is not confirmed as a public feature; group-score processing remains unavailable.

### Reporting without musical content

Share only the inspected PRIVACY_SAFE_DEBUG_REPORT.md by default, and add an inspected CONVERSION_REPORT.md if needed. EVENT_LIFECYCLE_TRACE contains per-note timing and is outside that scope. See the [AI sharing guide](docs/user/AI_SHARING_GUIDE.md) for the full classification.

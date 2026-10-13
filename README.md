# GSTE — Guitar Score Transcription Engine

**GSTE V0.3（程式版本 0.3.0）**將 MusicXML 樂譜轉換為五線譜與指彈吉他 TAB。正常轉換在本機執行，不依賴 AI。

**GSTE V0.3 (version 0.3.0)** converts MusicXML scores to fingerstyle guitar notation and TAB. Normal conversion runs locally without AI.

## 下載與啟動 / Download and launch

從版本下載頁下載 Windows EXE 安裝檔，執行並完成安裝後，透過程式捷徑啟動 GSTE。不需另外安裝 Python。本包提供文件與 Demo，EXE 安裝檔另行下載。

Download the Windows EXE installer from the release page, complete installation, then launch GSTE using its installed shortcut. No separate Python installation is needed. This package contains documentation and demos; the EXE installer is downloaded separately.

## 功能 / Features

| 模式 / Mode | 輸入與行為 / Input and behavior |
|---|---|
| Melody + Auto | 一份主旋律 MusicXML，自動生成伴奏。 / One melody file with generated accompaniment. |
| Melody + None | 一份主旋律 MusicXML，不添加伴奏。 / One melody file without added accompaniment. |
| Piano | 主旋律／右手與左手／伴奏兩份 MusicXML，分析來源伴奏後重新配置。 / Separate melody/right-hand and accompaniment/left-hand files. |
| Ensemble（實驗 / experimental） | 主旋律加 1–4 個伴奏檔，指定 GUITAR 或 BASS。 / Melody plus one to four GUITAR/BASS accompaniment files. |

團譜可同時輸入多軌吉他，最後融合為一把指彈吉他，不保證逐軌保留所有音符。

Ensemble mode combines multiple tracks into one guitar arrangement and does not guarantee complete track retention.
## Demo

`demo/` 全部採用 **V0.3 的實際轉換結果**：4 個主旋律、1 個鋼琴、1 個團譜案例。各曲保留輸入、最終 TAB、轉換報告及來源授權；未人工修改轉換結果的音符及指法。公開授權確認與演奏品質審查是不同事項，輸出仍需人工核對。

All six demo cases contain actual **V0.3 output**: four melody, one piano and one ensemble case. Each includes inputs, final TAB, conversion reports and source-license information. Converted notes and fingerings are unchanged. Permission to publish does not establish musical quality or playability.

請見 [Demo 清單](demo/README.md)。來源授權以各曲 `SOURCE_LICENSE.md` 為準；GSTE 軟體使用條款不取代樂譜授權。

See the [demo list](demo/README.md). Each score's source license is separate from GSTE's software terms.

## 文件與政策 / Documentation and policies

- [操作指南 / Getting Started](docs/zh-TW/user/GETTING_STARTED.md)
- [中文文件索引](docs/zh-TW/README.md) · [English documentation](docs/en/README.md)
- [目前限制 / Limitations](docs/zh-TW/user/CURRENT_LIMITATIONS.md)
- [V0.3 版本說明 / Release notes](RELEASE_NOTES_V0.3.md)
- [問題回報 / Issue reporting](docs/zh-TW/user/ISSUE_REPORT_GUIDE.md)
- [使用條款 / Terms](BETA_TERMS.md) · [隱私 / Privacy](PRIVACY.md) · [AI 政策 / AI policy](AI_POLICY.md)
- [第三方元件 / Third-party notices](THIRD_PARTY_NOTICES.md)

GSTE 可執行版本依隨附使用條款提供；本包不授予 GSTE 原始碼的開源授權。成功轉換不保證音樂性、指法或讀譜軟體排版正確。

The executable is provided under the included terms; this package grants no open-source license to GSTE source code. Successful conversion does not guarantee musical quality, fingering or reader rendering.

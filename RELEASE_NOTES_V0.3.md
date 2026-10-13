# GSTE V0.3 — 版本說明 / Release Notes

程式版本：**0.3.0**；介面名稱：**GSTE V0.3**。下載並執行 Windows EXE 安裝檔，完成安裝後啟動 GSTE。

Runtime version: **0.3.0**; application title: **GSTE V0.3**. Download and run the Windows EXE installer, then launch GSTE after installation.

## 主要更新 / Main changes

- 主旋律可選擇自動生成伴奏或不添加伴奏。 / Melody input offers automatic accompaniment or no accompaniment.
- 開放實驗性團譜輸入：主旋律與最多四軌 GUITAR／BASS 伴奏，多軌融合為一把指彈吉他。 / Experimental ensemble input combines a melody and up to four GUITAR/BASS tracks into one guitar arrangement.
- 改善來源伴奏、拍群與伴奏型態的解析和配置。Piano 伴奏使用同起音來源音約束及同小節共同八度策略，但不保證全部起音保留。 / Improved source accompaniment and pattern handling; Piano uses source-at-attack pitches and a shared measure-octave policy without complete attack-retention guarantees.
- 統一各模式的輸出整理，提供人工檢查與小節位置報告。 / Unified output folders include human-review and measure-location reports.
- Demo 更新為 V0.3: 4 個主旋律、1 個鋼琴、1 個團譜案例。 / Demos updated to V0.3: four melody, one piano and one ensemble case.

## 使用前須知 / Before use

輸入以未壓縮 `.musicxml`／`.xml` 為主；MIDI 不列為本版 GUI 支援格式。團譜仍屬實驗功能。旋律、節奏、伴奏、指法與排版均需人工檢查；報告 PASS 只適用於該項檢查，並非全曲品質認證。

Use uncompressed MusicXML. MIDI is not advertised as a supported GUI input in this release. Ensemble remains experimental. Review melody, rhythm, accompaniment, fingering and layout; a PASS applies only to its particular check.

目前限制見 [中文限制說明](docs/zh-TW/user/CURRENT_LIMITATIONS.md) / [Current limitations](docs/en/user/CURRENT_LIMITATIONS.md)。本包未聲稱已通過所有 Windows、讀譜軟體或演奏情境的驗證。

See the current limitations. This package does not claim validation across all Windows, score-reader or performance scenarios.

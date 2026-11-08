# GSTE — Demo Collection (V0.3 / V0.4 Beta)

本資料夾包含 **7 個實際轉換案例**：4 個主旋律（Melody）、1 個雙手鋼琴（Piano）、2 個團譜（Ensemble）。原有五個 Melody／Piano 案例維持 **GSTE V0.3**；兩個 Ensemble 案例為 **GSTE V0.4 Beta**，包含人工前處理、自動轉換及人工後處理。

This collection contains **7 conversion cases**: 4 melody, 1 piano, and 2 ensemble. The five existing melody/piano cases remain **GSTE V0.3** demonstrations. The two ensemble cases use **GSTE V0.4 Beta** and include manual preparation, automatic conversion, and manual post-editing.

## 案例清單 / Demo index

| 模式 / Mode | 案例 / Case | 版本 / Version | 展示成果 / Final score | 說明與授權 / Documentation |
|---|---|---|---|---|
| ensemble | 魔王 / *Erlkönig*, original measures 57–148 | V0.4 Beta | [MusicXML](ensemble/Erlkonig/Erlkonig_GSTE_final.musicxml) · [MP4](ensemble/Erlkonig/Erlkonig_GSTE_final.mp4) | [README](ensemble/Erlkonig/Erlkonig_README.md) · [Attribution](ensemble/Erlkonig/Erlkonig_ATTRIBUTION.md) |
| ensemble | 骷髏之舞 / *Danse macabre*, original measures 26–85 (ending after first note of m. 85) | V0.4 Beta | [MusicXML](ensemble/Danse_Macabre/Danse_Macabre_Final.musicxml) · [MP4](ensemble/Danse_Macabre/Danse_Macabre_Final.mp4) | [README](ensemble/Danse_Macabre/Danse_Macabre_README.md) · [Attribution](ensemble/Danse_Macabre/Danse_Macabre_ATTRIBUTION.md) |
| melody | 巴哈 BWV1007 / Bach BWV1007 | V0.3 | [MusicXML](melody/Bach_Cello_Suite_No.1_BWV1007_MELODY_Cello_R100/GSTE_TAB.musicxml) | [Source license](melody/Bach_Cello_Suite_No.1_BWV1007_MELODY_Cello_R100/SOURCE_LICENSE.md) |
| melody | 給愛麗絲：主旋律，第 1–80 小節 / *Für Elise*: melody, mm. 1–80 | V0.3 | [MusicXML](melody/Beethoven_FurElise_RH_Measure_1-80/GSTE_TAB.musicxml) | [Source license](melody/Beethoven_FurElise_RH_Measure_1-80/SOURCE_LICENSE.md) |
| melody | 巴哈 BWV1002 / Bach BWV1002 | V0.3 | [MusicXML](melody/bach_bwv1002/GSTE_TAB.musicxml) | [Source license](melody/bach_bwv1002/SOURCE_LICENSE.md) |
| melody | 韋瓦第 Op.3 / Vivaldi Op.3 | V0.3 | [MusicXML](melody/vivaldi_op3/GSTE_TAB.musicxml) | [Source license](melody/vivaldi_op3/SOURCE_LICENSE.md) |
| piano | 給愛麗絲：雙手鋼琴，第 1–80 小節 / *Für Elise*: piano, mm. 1–80 | V0.3 | [MusicXML](piano/Beethoven_FurElise_M1-80/Beethoven_FurElise_M1-80.musicxml) | [Source license](piano/Beethoven_FurElise_M1-80/SOURCE_LICENSE.md) |

## 如何閱讀 / How to use

- **V0.3 Melody／Piano**：各案例的 `input/` 保存輸入，`GSTE_TAB.musicxml` 或案例主檔為轉換結果。這五個案例的轉換音符與指法未經人工修改，仍需播放及實際演奏驗證。*Für Elise* 的 Melody 與 Piano 是兩個不同輸入模式案例。
- **V0.4 Beta Ensemble**：`Original/` 或 `original/` 為原始／來源整理資料，`Prepared/` 為人工前處理輸入；`*RawGSTE.musicxml` 為自動轉換結果，`*Final.musicxml` 或 `*final.musicxml` 為人工修訂展示版，MP4 為展示影片。詳細修改與限制見各曲 README。
- **授權 / Licensing**：各案例來源、改編聲明與授權條件請見其 `SOURCE_LICENSE.md` 或 `*_ATTRIBUTION.md`，並參閱 [授權索引](DEMO_LICENSE_INDEX.md)。影片及改編樂譜的授權範圍應依個別文件確認；不代表 GSTE 軟體程式碼採用相同授權。

## 展示注意事項 / Notes

Ensemble 的 Final 樂譜並非完全自動產物，請勿將其人工修訂部分歸因於 GSTE 自動編曲。部分 MusicXML 匯入 MuseScore 4 後可能出現多聲部休止符擁擠、等音異名記譜或播放聲部異常；詳細情況與暫行處理請參考各曲 README。

The ensemble final scores include manual edits and should not be presented as unmodified automatic outputs. Some imported MusicXML scores may require layout or playback review in MuseScore 4; see the individual READMEs.

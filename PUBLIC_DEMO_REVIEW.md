# 公開 Demo 定稿紀錄

[繁體中文](#繁體中文) · [English](#english)

## 繁體中文
日期：2026-10-03。由 14 組精簡為 9 組；不修改保留樂譜的音符、不重新轉換。

## 本次移除（Input 與 Output 同時移出）

| 舊目錄 | 原因 |
|---|---|
| melody/danse-macabre-op-40-saint-saens-camille | 來源檔對應與個別譜授權仍未核實 |
| piano/01_bach_bwv846 | 僅找到曲庫整體公版聲明，缺少足夠的個別數位版本權利證據 |
| piano/02_chopin_prelude_op28_no4 | 僅找到曲庫整體公版聲明，缺少足夠的個別數位版本權利證據 |
| piano/04_Chopin_-_Nocturne_Op_9_No_2_E_Flat_Major | 僅找到曲庫整體公版聲明，缺少足夠的個別數位版本權利證據 |
| piano/Waltz_in_A_MinorChopin | 僅找到曲庫整體公版聲明，缺少足夠的個別數位版本權利證據 |

所有保留的 MusicXML/MXL/MIDI/LilyPond ZIP 均與所提供公開包的原附件位元組相同；權利說明與索引為本次更新。給愛麗絲原檔的字節差異來自 XML 格式空白，正規化後與批次下載原檔相同。

Mutopia 來源鏈核對包括原稿權利欄位、來源頁、原始 MIDI 和輸入音符／起音位置。BWV1007 與 BWV1011 分別有 2 音與 1 音的起音位置相差 1/192 四分音符，其餘一致；完整比對方法與結果保存在權利 JSON，不將其表述為檔案完全相同。

本文件只記錄 Demo 篩選。安裝檔、Portable 二進位與其第三方依賴仍按原 SECURITY_REVIEW.md / THIRD_PARTY_NOTICES.md 的檢查範圍描述。CHECKSUMS.json 是原二進位雜湊，未改成文件包雜湊。

本次雙語修訂翻譯公開說明並更新文件校驗碼；上游授權原文及音樂檔保持不變，歷史引擎標記保留。

## English

Review date: 2026-10-03. The demo set was reduced from 14 to 9 cases. Retained score notes were not changed and conversions were not rerun.

### Cases excluded, including both input and output

| Previous directory | Reason |
|---|---|
| melody/danse-macabre-op-40-saint-saens-camille | Source-file identity and the individual edition's rights were not verified. |
| piano/01_bach_bwv846 | Only a collection-level public-domain statement was found; evidence for the individual digital edition was insufficient. |
| piano/02_chopin_prelude_op28_no4 | Same collection-level evidence limitation. |
| piano/04_Chopin_-_Nocturne_Op_9_No_2_E_Flat_Major | Same collection-level evidence limitation. |
| piano/Waltz_in_A_MinorChopin | Same collection-level evidence limitation. |

Retained MusicXML/MXL and MIDI/LilyPond ZIPs remain byte-identical to the supplied public-ready package. Rights notices and indexes were updated. The supplied Für Elise original differs from the batch download in XML formatting whitespace only; canonicalized XML matches.

The Mutopia provenance review checks original rights fields, source pages, original MIDI and input pitches/onsets. BWV1007 has two onsets and BWV1011 has one onset differing by 1/192 of a quarter note; all other checked pitch/onset pairs agree. Results and method limitations are recorded in the rights JSON. This is not a claim of byte-identical MIDI or full duration equivalence.

This record concerns demo selection. Installer, Portable binaries and third-party dependencies remain subject to the recorded scope in SECURITY_REVIEW.md and THIRD_PARTY_NOTICES.md. CHECKSUMS.json retains binary hashes, not documentation hashes.

The bilingual revision translates public explanatory text and updates document checksums. Upstream license originals and music files remain unchanged; historical engine labels are retained.

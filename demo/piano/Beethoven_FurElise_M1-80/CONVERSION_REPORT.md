# GSTE 0.3.0 — Für Elise（給愛麗絲） 轉換紀錄 / Conversion Record

- Batch status: **PASS**
- Runtime version: **0.3.0**
- Input mode: Piano / two-hand
- Elapsed seconds: 65.18
- Finished at (as recorded; timezone not provided): 2026-10-09T01:40:10
- Final score: [Beethoven_FurElise_M1-80.musicxml](Beethoven_FurElise_M1-80.musicxml)
- Public-source status: **PUBLIC_DEMO_SOURCE_CLEARED**

| 診斷 / Gate | 原報告狀態 / Recorded status |
|---|---|
| G1 | PASS |
| G2 | REVIEW |
| G3 | PASS |
| G4 | PASS |

G2 priority events: 44/54 retained; 10 dropped by Joint.

`PASS` 批次狀態代表成功輸出，不能代替 G2 REVIEW、人工音樂性檢查或授權確認。上列 priority 計數不是全曲旋律保留百分比。G3/G4 是資料輸出與重讀核對，不是 MuseScore 畫面驗證。

Batch PASS means output completion, not resolution of G2 REVIEW, musical quality or rights. Priority counts are not full-melody retention percentages. G3/G4 are data checks, not reader-render verification.

轉換樂譜位元組與附件最終 TAB 相同，未經人工改譜。本次僅核對 XML 可解析及檔案配對，未試聽、演奏或重跑。本公開示範格式不附完整 debug；人工報告已記錄的提醒概述如下，不附失效證據連結：

Final TAB bytes are unchanged. This task checks parsing and pairing only; no listening, performance or rerun. Full debug is omitted from the demo layout.

## 原人工提醒（僅摘要）

僅列診斷已記錄的位置與代碼；提醒不等於確認錯誤。

| 定位 | 記錄 | 證據檔案 |
|---|---|---|
| 原譜小節 未提供／選段第 未提供 小節／拍點 未提供 | `SERIALIZER_BACKBONE_EMISSION`／診斷標記 | `22_GPT_HUMAN_REVIEW_PACKET.json`（完整附件診斷，不含於此 Demo） |
| 原譜小節 未提供／選段第 未提供 小節／拍點 未提供 | `RHYTHM`／診斷標記 | `22_GPT_HUMAN_REVIEW_PACKET.json`（完整附件診斷，不含於此 Demo） |
| 原譜小節 15／選段第 16 小節／拍點 0.25 | `DISSONANCE`／診斷標記 | `22_GPT_HUMAN_REVIEW_PACKET.json`（完整附件診斷，不含於此 Demo） |
| 原譜小節 26／選段第 27 小節／拍點 0.0 | `DISSONANCE`／診斷標記 | `22_GPT_HUMAN_REVIEW_PACKET.json`（完整附件診斷，不含於此 Demo） |
| 原譜小節 34／選段第 35 小節／拍點 0.75 | `DISSONANCE`／診斷標記 | `22_GPT_HUMAN_REVIEW_PACKET.json`（完整附件診斷，不含於此 Demo） |
| 原譜小節 76／選段第 77 小節／拍點 0.0 | `DISSONANCE`／診斷標記 | `22_GPT_HUMAN_REVIEW_PACKET.json`（完整附件診斷，不含於此 Demo） |
| 原譜小節 64／選段第 65 小節／拍點 0.0 | `DISSONANCE`／診斷標記 | `22_GPT_HUMAN_REVIEW_PACKET.json`（完整附件診斷，不含於此 Demo） |
| 原譜小節 71／選段第 72 小節／拍點 0.0 | `DISSONANCE`／診斷標記 | `22_GPT_HUMAN_REVIEW_PACKET.json`（完整附件診斷，不含於此 Demo） |
| 原譜小節 78／選段第 79 小節／拍點 0.0 | `DISSONANCE`／診斷標記 | `22_GPT_HUMAN_REVIEW_PACKET.json`（完整附件診斷，不含於此 Demo） |
| 原譜小節 24／選段第 25 小節／拍點 0.75 | `DISSONANCE`／診斷標記 | `22_GPT_HUMAN_REVIEW_PACKET.json`（完整附件診斷，不含於此 Demo） |
| 原譜小節 33／選段第 34 小節／拍點 0.5 | `DISSONANCE`／診斷標記 | `22_GPT_HUMAN_REVIEW_PACKET.json`（完整附件診斷，不含於此 Demo） |
| 原譜小節 36／選段第 37 小節／拍點 0.0 | `DISSONANCE`／診斷標記 | `22_GPT_HUMAN_REVIEW_PACKET.json`（完整附件診斷，不含於此 Demo） |
| 原譜小節 62／選段第 63 小節／拍點 未提供 | `DROPPED_BY_JOINT`／DROPPED_BY_JOINT | `25_MELODY_IDENTITY_LIFECYCLE.json`（完整附件診斷，不含於此 Demo） |
| 原譜小節 70／選段第 71 小節／拍點 未提供 | `DROPPED_BY_JOINT`／DROPPED_BY_JOINT | `25_MELODY_IDENTITY_LIFECYCLE.json`（完整附件診斷，不含於此 Demo） |
| 原譜小節 75／選段第 76 小節／拍點 未提供 | `DROPPED_BY_JOINT`／DROPPED_BY_JOINT | `25_MELODY_IDENTITY_LIFECYCLE.json`（完整附件診斷，不含於此 Demo） |
| 原譜小節 76／選段第 77 小節／拍點 未提供 | `DROPPED_BY_JOINT`／DROPPED_BY_JOINT | `25_MELODY_IDENTITY_LIFECYCLE.json`（完整附件診斷，不含於此 Demo） |

拍點沿用診斷檔的計數單位；缺少欄位時顯示未提供，不從音樂內容推測。

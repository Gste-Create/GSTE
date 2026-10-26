# GSTE V0.4 beta — Public Release Notes / 公開說明

## 中文
本次主要增加 **GAR 編曲索引（V0.4 實驗功能）**：當前小節 TAB 顯示、主旋律事件選取與雙音建議、合併和弦指法與伴奏編排索引，以及六線 TAB 指法示意。GAR 目前**唯讀**，不會直接改譜、呼叫 Joint、重新生成或輸出修改後的樂譜。候選為靜態簡化指法參考，不代表原曲節奏重建或完整演奏驗證。

GSTE 仍提供主旋律、鋼琴及團譜 MusicXML 轉指彈吉他五線譜與 TAB。團譜介面最多四條伴奏輸入，但建議從一至兩軌開始；即使兩軌也可能嚴重壓縮原有聲部。請依聽感比較、調整來源音軌並人工確認。

**Demo 未變動**：沿用 V0.3 自動轉換成果，未重新生成、未用 GAR 修改，不能當成 V0.4 beta 的新演算法品質比較。歡迎回饋音樂性、來源保留、候選指法及操作體驗。一般使用者不需要閱讀完整工程 Debug。



## English
This beta introduces the experimental **GAR arrangement reference index** (V0.4): measure-focused TAB, melody-event selection and double-stop suggestions, a combined chord/accompaniment fingering index, and six-string TAB diagrams. **GAR is read-only**; it does not edit notation, invoke Joint, regenerate, or export modified scores. Candidates are simplified static references, not a full playability check or source-rhythm reconstruction.

GSTE still supports melody, piano, and experimental ensemble MusicXML-to-fingerstyle staff/TAB conversion. Although ensemble offers up to four accompaniment slots, start with one or two. Even two tracks may undergo significant musical compression. Compare results and review by ear.

**Demos are unchanged V0.3 automatic conversions**—not regenerated or GAR-edited. Feedback on musicality, voice retention, fingering references, and usability is welcome; full debug logs are not required.



## 目前 V0.4 介面與報告 / Current V0.4 GUI and reports

- GUI 提供繁體中文、English、日本語切換；轉換報告的易讀摘要可依介面語言顯示，原始診斷代碼保留。 / GUI offers Traditional Chinese, English and Japanese; report summaries may follow the UI language while diagnostic codes remain stable.
- 團譜每軌依樂器角色套用固定 Harmony/Bass/Texture/Rhythm 權重；此功能仍屬實驗性，音樂性保留度須人工確認。 / Ensemble tracks use fixed role-based Harmony/Bass/Texture/Rhythm weights. Musical preservation must be checked manually.
- 錯誤報告所列位置可能是特定全域搜尋候選的失敗位置，**不一定是所有候選共同的唯一根因**。 / A reported location may belong to a rejected search candidate and is not necessarily the unique cause of overall failure.
- 本包只更新文件，不改動 GSTE 程式或重新產生 Demo。 / This package updates documentation only; it does not change program code or regenerate demos.


---

## 日本語

GSTE V0.4 beta は、**GAR 編曲リファレンス（実験的）**を導入します。現在の小節を中心とした TAB 表示、旋律音符の選択と重音候補、和音運指と伴奏配置の統合リファレンス、六線 TAB 図を提供します。GAR は**読み取り専用**で、直接編集、Joint 再実行、再生成、修正楽譜の書き出しは行いません。

旋律、ピアノ、実験的なアンサンブルの MusicXML 変換は引き続き利用できます。アンサンブルは最大 4 本の伴奏トラックを受け付け、各トラックに楽器役割ごとの固定 Harmony/Bass/Texture/Rhythm ウェイトを適用します。ただし一本のギターへの統合で音楽情報が大きく省略される場合があるため、1～2 本からの試用と人による確認を推奨します。

GUI は繁体字中国語・英語・日本語に対応します。付属デモは変更していない V0.3 の変換結果で、V0.4 による再生成ではありません。

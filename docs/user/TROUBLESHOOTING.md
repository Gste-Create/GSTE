# GSTE Beta V0.2 — 常見問題

[繁體中文](#繁體中文) · [English](#english)

## 繁體中文
## 程式無法啟動

重新啟動電腦可以排除暫時性的程序鎖定，但不是標準修復方式。若持續無法啟動，請記錄 Windows 版本、GSTE 版本與發生情況後回報。

## 轉換失敗

確認 MusicXML 可由一般樂譜閱讀器正常開啟，再確認輸入模式與檔案選擇正確。查看是否產生 `ERROR_REPORT.md` 與 `PRIVACY_SAFE_DEBUG_REPORT.md`。

## 轉換成功但結果不理想

請先判斷輸入是否符合目前模式：

- Piano：主旋律是否主要位於右手？
- Melody：是否已整理出希望保留的主要音符？
- Melody-only：是否希望不產生自動伴奏？

若作品旋律頻繁跨左右手，不要把 Piano 模式輸出不理想直接視為單一小 bug；這可能超出目前路徑的設計假設。

## 輸出 MusicXML 無法正常顯示

如果 GSTE 顯示完成，但 MuseScore／Soundslice 開啟後只有休止符、缺音、延音錯誤或無法載入，請保留該輸出並回報。這類問題屬於輸出格式／重新解析驗證的一部分，不應靠逐曲特殊修補取代共同根因修正。

## English

### Application does not start

Restarting the computer may clear a temporary process lock but is not a standard fix. If the issue continues, report the Windows version, GSTE version and circumstances.

### Conversion fails

Check that a normal score reader can open the MusicXML, and that the input mode and files are correct. Look for ERROR_REPORT.md and PRIVACY_SAFE_DEBUG_REPORT.md.

### Conversion succeeds but the result is unsuitable

Check whether the score fits the selected mode:

- Piano: is the melody mainly in the right hand?
- Melody: have you prepared the principal notes you want to retain?
- Melody-only: do you want no generated accompaniment?

When melody frequently crosses hands, unsuitable Piano output may reflect the workflow's design assumptions rather than a single minor bug.

### Exported MusicXML does not display correctly

If GSTE completes but MuseScore / Soundslice shows only rests, missing notes, tie errors or a loading failure, retain the output and report it. This concerns export-format and reparse validation. Per-song patches should not replace investigation of the shared root cause.

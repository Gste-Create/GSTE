# GSTE Beta V0.1 — 安裝與 GUI 使用指南

這份文件將「安裝」與「GUI 操作」合併在同一個流程。一般使用者第一次使用 GSTE，只需要先閱讀這一份。

## 1. 安裝／啟動

### 建議：安裝版

1. 取得 `GSTE_Beta_V0.1_Setup.exe`。
2. 雙擊安裝程式並依畫面完成安裝。
3. 安裝完成後，從 Windows 開始功能表開啟 **GSTE**。若安裝時建立了桌面捷徑，也可以直接從桌面啟動。

一般使用者不需要另外安裝 Python；正式 Beta 安裝包已包含執行所需 runtime。

> 若程式無法啟動，請參閱 [`TROUBLESHOOTING.md`](TROUBLESHOOTING.md)。

## 2. 選擇語言

GUI 可在 **繁體中文**與 **English** 之間切換。語言切換只影響使用者介面文字，不會改變編曲結果。

## 3. 選擇輸入模式

### 雙手鋼琴

目前 GUI 需要分別指定：

- **主旋律／右手 MusicXML**
- **左手／伴奏 MusicXML**

兩個檔案會共同進入 GSTE 的鋼琴編曲流程。

### 僅主旋律

選擇一份單旋律 MusicXML。GSTE 會使用目前 Beta 的 Auto 編曲流程，自動決定和弦與伴奏。

### 團譜

入口目前保留，但 **Beta V0.1 暫不開放**。

## 4. 選擇輸出資料夾

按 **「選擇」** 指定輸出位置。每次轉換會建立獨立的結果資料夾，避免直接覆蓋前一次轉換。

## 5. 開始轉換

確認輸入檔案與輸出位置後，按 **「開始轉換 / Convert」**。

成功後 GUI 會顯示完成訊息，並提供：

- **開啟完成樂譜 / Open finished score**
- **開啟輸出資料夾 / Open output folder**

一般使用者最主要的結果是：

`GSTE_TAB.musicxml`

可使用支援 MusicXML 的樂譜軟體開啟並人工檢查結果。

## 6. 轉換完成後

成功轉換的外層資料夾主要包含：

```text
歌曲名稱_GSTE/
├─ GSTE_TAB.musicxml
├─ CONVERSION_REPORT.md
├─ PRIVACY_SAFE_DEBUG_REPORT.md
└─ debug/
```

一般使用時只需要先查看 `GSTE_TAB.musicxml`。若要回報問題，請優先提供 `PRIVACY_SAFE_DEBUG_REPORT.md`。`debug/` 保存較完整的工程診斷資料，可能含較詳細的樂譜或本機資訊；除非確認內容可以分享且維護者確實需要，否則不要直接上傳整個 `debug/` 資料夾。

詳細說明請閱讀 [`OUTPUT_GUIDE.md`](OUTPUT_GUIDE.md)。

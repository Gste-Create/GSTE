# GSTE Beta V0.2 — 安裝與 GUI 使用指南

## 1. 安裝與啟動

1. 從 GSTE 官方 GitHub Release 取得目前版本的 Windows 安裝檔。
2. 執行安裝程式並依畫面完成安裝。
3. 開啟安裝後的 GSTE；捷徑是否建立依安裝選項而定，本次未實際執行安裝驗證。安裝腳本設定 PrivilegesRequired=admin，Setup 會要求系統管理員權限。

安裝檔：`GSTE_Beta_V0.2_Setup.exe`。Portable：將 `GSTE_Beta_V0.2_Portable.zip` 完整解壓到獨立資料夾，再開啟 `GSTE.exe`；不要只移動 EXE，其他 DLL、Tcl/Tk 檔也需要保留。此包為 Windows x64 程式。

轉換前備份輸入，輸出請使用專用空白資料夾，不要選取存放其他重要檔案的資料夾。

一般使用者不需要另外安裝 Python。更新版本時，請以 GitHub Release 顯示的版本號與檔名為準，不要從舊貼文或舊 Demo 包判斷目前版本。

## 2. 準備輸入 MusicXML

GSTE 主要使用 `.musicxml` / `.xml`。

### 雙手鋼琴模式

分別準備：
- 右手／主旋律 MusicXML
- 左手／伴奏 MusicXML

此模式目前最適合主旋律主要位於右手、左手主要負責 Bass／和聲／伴奏的作品。

**不建議直接把旋律頻繁跨越左右手、兩手音符皆高度不可省略的作品視為標準 Piano 輸入。** 這類作品即使成功輸出，也可能出現旋律遺失、織度破壞或不符合原曲結構的結果。

### Melody 模式

選擇一份主要旋律 MusicXML。依 GUI 目前提供的選項，可使用自動編曲流程，或選擇**僅主旋律轉換、不加入自動伴奏**。

「僅主旋律」功能主要用途是保留輸入音符並將其配置到吉他演奏位置，也可作為未來其他撥弦樂器樂譜移植與跨手旋律整理的基礎工具。它不代表所有複雜鋼琴譜可以不經整理直接輸入。

### 團譜

目前公開 Beta 尚未開放。

## 3. 開始轉換

指定輸出位置後按「開始轉換 / Convert」。以下為常見名稱示意，實際內容依轉換結果而定：

```text
歌曲名稱_GSTE/
├─ GSTE_TAB.musicxml
├─ CONVERSION_REPORT.md
├─ PRIVACY_SAFE_DEBUG_REPORT.md
└─ debug/
```

## 4. 轉換後一定要做的事

請使用 MuseScore 或其他支援 MusicXML 的閱讀器開啟 `GSTE_TAB.musicxml`，至少確認：

- 主旋律是否完整
- 節奏與延音是否正確
- 是否出現多餘或消失的音符
- TAB 與五線譜是否對應
- 指法／把位是否實際可演奏
- 檔案能否正常開啟與播放

**GSTE 顯示成功 ≠ 樂譜已人工驗證通過。**

## 5. 樂譜與著作權

請只輸入、分享或公開你具有相應權利的樂譜。

「作品本身是 Public Domain」與「你下載的那一份 MusicXML 可以自由再散布」是不同問題。若無法確認特定來源檔的授權，請不要把該來源 MusicXML 隨 GSTE Demo 或問題回報公開散布。

# GSTE Beta V0.2 — 安裝與 GUI 使用指南

[繁體中文](#繁體中文) · [English](#english)

## 繁體中文
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

常見結果包含 `GSTE_TAB.musicxml`、`CONVERSION_REPORT.md`、`PRIVACY_SAFE_DEBUG_REPORT.md` 與 `debug/`，存放於該次結果資料夾；詳見 [輸出指南](OUTPUT_GUIDE.md)。

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

## English

### 1. Installation and launch

1. Obtain the current Windows installer from the official GSTE GitHub Release.
2. Run the installer and follow its prompts.
3. Launch GSTE after installation. Shortcut creation depends on installation options; the recorded review did not execute the installer. The reviewed script sets PrivilegesRequired=admin, so Setup requests administrator privileges.

Installer: GSTE_Beta_V0.2_Setup.exe. Portable: fully extract GSTE_Beta_V0.2_Portable.zip into a dedicated folder, then launch GSTE.exe. Keep the other DLL and Tcl/Tk files alongside it; do not move only the EXE. The reviewed package is Windows x64.

Back up inputs before conversion. Use a dedicated empty output folder rather than a folder containing other important files.

End users do not need to install Python separately. When updating, use the version and filenames displayed in the GitHub Release, rather than an old post or demo package.

### 2. Preparing MusicXML input

The main supported extensions are .musicxml / .xml.

**Two-hand Piano mode:** prepare separate right-hand / melody and left-hand / accompaniment files. This mode works best when melody is mainly in the right hand and bass, harmony or accompaniment mainly in the left.

Do not treat scores with melody frequently crossing hands or indispensable notes in both hands as standard Piano input. Even successful output may lose melodic material, damage texture or misrepresent the original structure.

**Melody mode:** select one principal-melody MusicXML file. According to GUI options, use automatic arrangement or **melody-only conversion without generated accompaniment**.

Melody-only conversion aims to retain input notes while assigning guitar positions. It can also provide a foundation for future transfers from other plucked instruments and for reorganizing cross-hand melody. It does not mean complex piano scores can be entered without preparation.

**Group scores:** unavailable in the public Beta.

### 3. Starting conversion

Choose an output location and click Convert. Typical output files include GSTE_TAB.musicxml, CONVERSION_REPORT.md, PRIVACY_SAFE_DEBUG_REPORT.md and a debug/ folder inside the result directory. Actual contents depend on the result. See the [output guide](OUTPUT_GUIDE.md).

### 4. Reviewing the output

Open GSTE_TAB.musicxml in MuseScore or another MusicXML reader. Check:

- Whether the principal melody is retained.
- Rhythm and sustain / ties.
- Extra or missing notes.
- Agreement between TAB and staff notation.
- Playable fingering and positions.
- Successful loading and playback.

**GSTE success is not a manual score-validation pass.**

### 5. Scores and copyright

Input, share or publish only scores for which you have the required rights.

A public-domain composition and a freely redistributable downloaded MusicXML edition are separate issues. If the edition's rights cannot be confirmed, do not distribute that source file publicly with a GSTE demo or issue report.

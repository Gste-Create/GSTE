# GSTE Beta V0.2 安全、隱私與授權檢查
檢查日期：2026-10-02。對象：本次附件的 Setup.exe、Portable.zip、其中 GSTE.exe 及 V0.1.1 文件包。

## 結論
本次未在可讀程式字串及封裝清單中辨識出明確的 GSTE 惡意指令、開發者個人使用者路徑或明顯服務金鑰，但這是有限的二進位靜態觀察，不足以排除隱藏、編碼、動態組合或執行時行為。不能對外宣稱「不會傷害任何電腦」「完全不侵權」「沒有個資風險」。
現階段判定為：文件已修正，二進位安全與發布授權尚未完整驗證。

## 已觀察與待確認
|項目|本次證據|判定與下一步|
|---|---|---|
|封裝型態|GSTE.exe 為 Windows x64 PE，具有 Nuitka module loader 字串；不是可直接閱讀的 Python 原始碼|須取得對應 build 原始碼、依賴清單及安裝腳本|
|執行權限|GSTE.exe manifest 為 asInvoker|主程式 manifest 未要求提升權限；安裝程式權限與實際行為另需測試|
|檔案清理|GUI 與 output_packaging 鄰近常數含 rmtree、unlink、move、copy2|疑似輸出整理；無法確認路徑保護、符號連結、同路徑或例外時是否會誤刪。應驗證只能清理本次建立的工作目錄|
|外部程序|GUI 區段有 subprocess、startfile 字串|可能用於開啟結果；須核對是否 shell=True、命令拼接或未受信輸入可觸發命令|
|網路|有 Python socket/SSL；內部 demo_service 描述 CLI/web caller|不能由元件存在推定有上傳，也不能由未發現目標網址保證不連網。須離線轉換及網路監測|
|報告隱私|有 privacy_safe_debug、public_musicxml_sanitizer 與 event lifecycle 相關元件|未取得生成器或真實輸出，未確認例外訊息、檔名路徑、metadata 全部遮蔽|
|個資字串|ASCII／UTF-16 可讀內容搜尋未見明顯開發者 C:\Users 路徑、常見 GitHub/OpenAI 金鑰前綴|只涵蓋有限樣式；上游作者署名、email 與著作權通知屬授權資訊，應保留|
|音樂素材|Portable 清單未見獨立 MusicXML/MIDI demo 檔|不能因此排除內嵌資料、未授權程式碼或未提供的 Repository demo|
|第三方通知|原包只找到 tk/license.terms；Python 3.11.9、OpenSSL 3.0.13 版本字串|授權材料尚未完整隨二進位附帶；本次補入文件可取得部分，Tcl、VC runtime、Nuitka build 版本仍需核實|
|版本一致性|APP_NAME=GSTE Beta V0.2，VERSION=group_V0.1，提示仍含 Beta V0.1、report 含 V0.1.3|下次 build 統一 title、report、terms、installer 版本；文件更新不能修補 EXE 內部文字|

## 本次未執行
未執行 Windows 安裝／卸載、GUI 轉換、網路／登錄／檔案系統監測、Defender 或其他防毒掃描；未進行來源逐行審查、惡意輸入測試、依賴 CVE 完整比對或來源與二進位一致性驗證。舊版本 Python/OpenSSL 可讀字串不等於已確認漏洞可利用，也不能視為目前已更新。
Setup.exe 與 GSTE.exe 的 PE certificate table 欄位皆為 0，本次沒有看到內嵌 Authenticode 簽章；未確認外部 catalog 簽署。結果見 CHECKSUMS.json。未簽署不等於惡意程式，但不能以發行者簽章核對來源。

## 完成確認需要的資料與測試
1. 提供本次 V0.2 對應的完整 source project、requirements/lock/build report、安裝腳本與實際 build 指令，先核對雜湊或 build 身分。
2. 審查所有刪除、覆蓋、解壓、subprocess、XML/MXL 輸入、診斷文字與 metadata sanitization 的呼叫路徑；設定輸入大小／展開量限制，驗證失敗不影響來源與其他檔案。
3. 在乾淨 Windows VM 測試一般權限安裝／Portable／卸載，監測網路、登錄與工作目錄外檔案變動；加入含人名、使用者路徑、歌詞、來源 metadata 的隱私測試。
4. 由 Windows Defender 掃描實際最終包，驗證重新封裝後的 SHA-256；不要為了通過啟動而要求使用者關閉防毒或整體安全功能。
5. 依實際 build 的全部依賴補齊授權通知與可散布來源，將通知隨 Setup 安裝及 Portable 附帶。現有文件不能證明來源程式碼沒有抄用第三方。

## 音樂權利
原曲公版不代表特定編曲、數位樂譜、演奏音檔或其新增內容可任意再散布。只發布轉換結果也不會自動消除來源編曲的權利問題。未查證來源的示範需另行審核，不能以轉換格式當作授權。
原二進位安全檢查未涵蓋 Demo。2026-10-03 已另對公開 Demo 完成來源聲明與附件來源鏈核對，範圍見 demo/DEMO_LICENSE_INDEX.json；這不改變本文件的二進位安全檢查結論。

## 參考
- Python 3.11 授權：https://docs.python.org/3.11/license.html；隨文件附入 v3.11.9 來源 LICENSE 與 incorporated-software 文件。
- OpenSSL：https://openssl-library.org/source/license/index.html；實際取得狀況見 licenses/SOURCES.json。
- Nuitka：https://nuitka.net/user-documentation/user-manual.html。
- 美國著作權局衍生作品說明：https://www.copyright.gov/circs/circ14.pdf（一般原則參考，非台灣個案法律結論）。

本次僅更新文件，不修改 EXE、DLL 或演算法，不表示安裝包已重新建立或安全認證完成。

## 原始碼與實際診斷包補充檢查（2026-10-02）
此節補充上述僅二進位檢查的限制，新增附件為 GSTE_group_V0.2_GUI_InstallerName_Fixed(1).zip、licenses.zip 與 Chopin 診斷包。尚未證明原始碼能逐位元重建既有 EXE。

- src 匯入靜態掃描未發現 requests／urllib／socket／http／ftplib／smtplib／winreg／pickle；桌面外部開啟使用 os.startfile 或參數陣列的 Popen，未看到 shell=True。不能以有限掃描代替動態安全測試。
- GUI _new_run_dir 建立以輸入 stem 命名的獨立目錄，已有目錄則加序號；清理呼叫集中在工作輸出與 debug/pipeline_output。API/CLI 可傳既有 output_dir，packaging 會移動非 ROOT_KEEP 檔案並刪除同名舊 target，且未見完整路徑／連結防護。因此 GUI 一般使用的目錄隔離較清楚，仍不能保證任意 API 輸入安全；專用輸出目錄建議保留。
- Inno 腳本明示 PrivilegesRequired=admin；註冊表讀取是檢查相同版本是否已安裝。程式 main manifest 的 asInvoker 與安裝程式要求管理員是不同事項。
- build_windows.bat 使用 pip 與 Nuitka 下載建置工具，清空專案 dist／release；這是開發建置行為，不應要求一般使用者執行。建置依賴未精確鎖版本，不可宣稱可重現 build。
- 未看到建立 Portable 前複製 licenses 的步驟，因此原附件授權缺口仍需重建包才能補入。附來的 licenses.zip 與上輪文件包授權材料完全一致。
- 專案原始碼附件內有 8 個獨立 XML／MusicXML 音樂檔；其來源／授權未逐曲查核，不宜把整個 source ZIP 當作不含音樂的公開包。此次未修改或公開該 source ZIP。
- 本次精簡 JSON 以 build_privacy_safe_debug_report 從同包 ENGINEER_DEBUG_SUMMARY 重新產生，結果完全相同。沒有逐音音高／時間欄位，但有 108 個匿名區段的診斷與候選統計。
- EVENT_LIFECYCLE_TRACE 雖名為 privacy-safe，實際匯出 onset/release、角色、延音與事件順序，包含節奏資訊。文件已明確排除它作為不提供音樂內容的預設回報。
- 產生器只限制欄位，未嚴格限定所有字串值。以純合成敏感 sentinel 放進 status／flags／area，輸出仍包含 sentinel，證實存在字串透傳；這不是本次樣本洩漏個資的證據。需後續程式值白名單與相關測試改善。

### 驗證紀錄
直接執行既有三個 output/package/privacy trace contract 測試函式均通過；本環境無 pytest，未執行完整 pytest suite。另做實際精簡 JSON 生成一致性比對與合成字串透傳檢查。這三個既有測試本身只驗證介面／原始碼文字，不能當作去識別化或程式安全認證。
新增文件 AI_SHARING_GUIDE.md，清楚區分「不提供音高／和弦／逐音節奏」與「連推導統計都不提供」。本次僅更新文件，未修改 source／EXE／安裝腳本。

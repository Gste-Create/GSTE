# GSTE Beta V0.2 — Third-Party Notices
第三方授權不受 GSTE Beta 條款覆蓋或限制。以下是本次 Portable 包靜態盤點，並非完整法律合規認證。

|元件|觀察結果|文件與待確認事項|
|---|---|---|
|Python|python311.dll 可讀版本為 3.11.9|licenses/PYTHON-3.11.9-LICENSE.txt 與 incorporated-software 文件|
|Tcl/Tk|tcl86t.dll、tk86t.dll；8.6 系列，patch 未核實|保留原包 tk/license.terms；Tcl 的精確版本授權需由 build 核實|
|OpenSSL|libcrypto 可讀版本為 3.0.13|licenses/OPENSSL-3.0.13-LICENSE.txt|
|Microsoft VC runtime|vcruntime140.dll|須確認 build 使用的 Visual Studio / VC Redistributable 授權及可散布來源|
|Nuitka|編譯器識別字串，版本未核實|licenses/NUITKA-LICENSE.txt 僅供索引；實際 build 版本及其隨附通知需核實|
|Python incorporated software|_bz2、_lzma、_decimal、pyexpat 等|依 Python 文件檢查 Expat、libmpdec、bzip2、xz 等實際內建版本通知；不得以主授權取代|

原 Portable 包只有找到 tk/license.terms，未找到本表其餘完整文件。此次文件包補入可取得的上游文件；尚未改動 Setup.exe 或原 Portable。公開發布時需把授權文件放入實際安裝目錄與 Portable，並核實實際版本，不是只放 GitHub 索引。

官方來源與取得日期見 licenses/SOURCES.json。上游主分支文件不代表已匹配特定 Nuitka build。未發現 music21 獨立封裝檔，不代表可證明沒有改寫或內嵌其程式碼。

## 附件 licenses 與建置核對（2026-10-02）
使用者提供的 licenses.zip 與本文件包 licenses 逐檔一致，確實包含前述上游授權材料；仍缺 Tcl 精確 build 的核對與 VC runtime 可散布來源資料，Nuitka 文件來自主分支而非已鎖定 build 版本。這不是完整依賴合規認證。
原始碼 build_windows.bat 未把 licenses 或本套文件複製進 dist/GSTE；Inno Setup 只收集 dist/GSTE。應在建立 Portable ZIP／呼叫 Inno Setup 之前，把核實過的 licenses 與必要使用條款／notice 複製進 dist/GSTE，再重建發布包。單獨上傳 licenses.zip 不會改動既有 Setup.exe。

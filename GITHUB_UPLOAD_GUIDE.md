# GitHub 更新方式

[繁體中文](#繁體中文) · [English](#english)

## 繁體中文
1. 解壓縮本包；README.md、demo/、docs/、licenses/ 位於 ZIP 根目錄。上傳這些內容，不要再包進一層 GSTE 資料夾。
2. 先刪除 GitHub 舊 demo/ 內容，再上傳本版完整 demo/。網頁 Upload files 的同名覆蓋不會刪除本版已移除的曲目；只補新檔會讓舊譜繼續公開。移除清單見 PUBLIC_DEMO_REVIEW.md。若已上傳精簡後的 9 組 Demo，只需同路徑覆蓋本次雙語文件，不必再刪除這 9 組。
3. 同步更新根目錄 README.md、SECURITY_REVIEW.md 與本包其他文件。
4. 本包不含安裝檔；Release 安裝檔仍需另外更新。
5. 舊曲目若曾公開，刪除目前檔案不會自動清除 Git 歷史、舊 Release 或外部副本。另檢查你曾上傳的舊 Demo ZIP 與 Release 附件。

6. 網頁單次最多上傳 100 個檔案。本包可分 demo/ 與其餘根目錄內容兩批上傳。若剛完成 9 組 Demo 上傳，本次直接覆蓋雙語文件，不需重做刪除流程。docs/ 使用原路徑，避免 docs/docs/。

建議提交標題：更新 Beta V0.2 中英對照文件。
建議說明：補齊公開指南與 Demo 來源說明的中英對照，保留 9 組 Demo 並更新文件校驗碼。

## English

1. Extract the package. README.md, demo/, docs/ and licenses/ are at the ZIP root. Upload these contents without wrapping them in an extra GSTE folder.
2. When replacing the older 14-case demo set, delete the old demo/ contents first, then upload the complete selected 9-case demo/. Web uploads do not delete cases absent from the new package. The removal list is in [PUBLIC_DEMO_REVIEW.md](PUBLIC_DEMO_REVIEW.md). If you have already uploaded the selected 9-case set, upload the bilingual files to the same paths; there is no need to delete those nine cases again.
3. Update the root README.md, SECURITY_REVIEW.md and other supplied documents together. Update docs/ at its existing path; do not create docs/docs/ or an extra release-folder wrapper.
4. This package contains no installer. Update installer assets separately in Releases.
5. Deleting current files does not erase Git history, old Release assets or external copies. Also review previously uploaded demo ZIPs and Release attachments.
6. A browser upload accepts up to 100 files per batch. This bilingual package can be uploaded in two batches: the demo/ folder first, then all remaining root files and folders. Inspect the listed paths before committing.

Suggested commit title: Update Beta V0.2 bilingual documentation.
Suggested description: Add complete Chinese and English public guides and demo source notices; keep the nine selected demos and update document checksums.

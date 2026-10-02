# GitHub 更新方式

1. 解壓縮本包；README.md、demo/、docs/、licenses/ 位於 ZIP 根目錄。上傳這些內容，不要再包進一層 GSTE 資料夾。
2. 先刪除 GitHub 舊 demo/ 內容，再上傳本版完整 demo/。網頁 Upload files 的同名覆蓋不會刪除本版已移除的曲目；只補新檔會讓舊譜繼續公開。移除清單見 PUBLIC_DEMO_REVIEW.md。
3. 同步更新根目錄 README.md、SECURITY_REVIEW.md 與本包其他文件。
4. 本包不含安裝檔；Release 安裝檔仍需另外更新。
5. 舊曲目若曾公開，刪除目前檔案不會自動清除 Git 歷史、舊 Release 或外部副本。另檢查你曾上傳的舊 Demo ZIP 與 Release 附件。

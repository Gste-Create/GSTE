# GSTE Beta V0.1 — 第三方元件聲明 / Third-Party Notices

GSTE Beta V0.1 的 Windows 發布包包含第三方執行階段元件。這些元件不因 GSTE 自身的 Beta 使用條款而改變授權；各元件仍依其原始授權條款提供。

The GSTE Beta V0.1 Windows package includes third-party runtime components. Their licenses are not replaced by the GSTE Beta terms; each component remains available under its upstream license.

本清單依 Beta V0.1 Release Candidate 的實際 Windows runtime 封裝內容整理；公開下載目前以 `GSTE_Beta_V0.1_Setup.exe` 為主。版本資訊由同一 Release Candidate 的 runtime 檔案與 binary version strings 核對。

| Component | Version observed in package | Purpose | Upstream license / notice |
|---|---:|---|---|
| Python | 3.11.9 | GSTE runtime | Python Software Foundation License Agreement; Python distribution also contains incorporated software under additional notices |
| Tcl/Tk | 8.6.12 | Tk GUI runtime | Tcl/Tk License Terms |
| OpenSSL | 3.0.13 | Cryptographic/SSL runtime libraries used by the packaged Python runtime | Apache License 2.0 |
| Microsoft Visual C++ Runtime | packaged runtime DLL | Windows C/C++ runtime required by the executable/runtime | Microsoft redistributable terms |
| bzip2 / libbzip2-derived Python module support | included through Python `_bz2` runtime module | Compression support | bzip2/libbzip2 license; see Python incorporated-software acknowledgements |

## Important

- GSTE does not claim ownership of these third-party components.
- Third-party copyright notices and license terms remain in effect.
- The GSTE Beta license applies to GSTE's own distributable portions only and does not override rights granted by third-party licenses.
- Python itself contains additional incorporated software with separate notices. For the authoritative list, consult the license/acknowledgement materials corresponding to the packaged Python 3.11.9 distribution.
- When preparing the final downloadable release, retain the upstream license files/notices required by the corresponding runtime distributions. This notice is a project index and is not a substitute for any full license text that an upstream license requires to accompany binary redistribution.

## License files and official upstream references

公開 Repository 另提供 [`licenses/`](licenses/) 目錄，集中保存隨封裝取得的授權文字與官方授權來源索引。

## Official upstream references

- Python 3.11 license and incorporated-software acknowledgements: https://docs.python.org/3.11/license.html
- Tcl/Tk licensing terms: https://www.tcl-lang.org/software/tcltk/license.html
- OpenSSL licensing information: https://www.openssl.org/source/license.html
- bzip2/libbzip2: https://sourceware.org/bzip2/

If a future GSTE build changes its packaged runtime or adds dependencies, this file must be reviewed again before that build is released.

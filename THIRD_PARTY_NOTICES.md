# GSTE V0.3 — Third-Party Notices

This inventory describes the components included in the supplied Windows portable distribution. Third-party components remain subject to their respective licenses. GSTE's terms of use do not replace or restrict the rights granted by those licenses. Source licenses for demo scores are documented separately in each piece's `SOURCE_LICENSE.md`.

| Component | Version | Purpose | License |
|---|---|---|---|
| CPython | 3.11.9 | Python runtime and standard library | Python Software Foundation License Agreement and incorporated third-party notices |
| Tcl / Tk | 8.6.12 | Graphical user interface | Tcl/Tk License Terms |
| OpenSSL | 3.0.13 | Cryptographic and SSL support bundled with Python | Apache License 2.0 |
| Microsoft Visual C++ Runtime | 14.38.33126.1 | Windows runtime support | Applicable Microsoft redistribution terms |
| Incorporated libraries, including Expat, bzip2, liblzma and libmpdec | Individual component versions not separately identified | XML parsing, compression and decimal arithmetic | Component-specific licenses; see the Python incorporated-software acknowledgements |
| Nuitka compiled runtime support | 2.8.10 | Compilation support embedded in `GSTE.exe` | Apache License 2.0 |

The Python version was identified from version strings in `python311.dll`. Tcl/Tk versions were identified from the bundled initialization scripts. OpenSSL and Visual C++ Runtime versions were identified from their DLL version strings. Nuitka 2.8.10 was identified from the user-supplied query of the same project's `.venv-build` environment on 2026-10-10. Its license text is retained from the official 2.8.10 release tag.

## Included Licenses

- [Python License](licenses/PYTHON_LICENSE.txt)
- [Python Incorporated-Software Acknowledgements](licenses/PYTHON_ACKNOWLEDGEMENTS.rst)
- [Tcl/Tk License](licenses/TCL_TK_LICENSE.txt)
- [Apache License 2.0](licenses/APACHE-2.0.txt)
- [Nuitka 2.8.10 License](licenses/NUITKA_2.8.10_LICENSE.txt)
- [Official License Sources](licenses/OFFICIAL_LICENSE_SOURCES.md)

The presence of bundled OpenSSL, socket or other runtime support does not imply that normal GSTE conversion uploads scores. See [PRIVACY.md](PRIVACY.md) for the data-processing and issue-report policies.

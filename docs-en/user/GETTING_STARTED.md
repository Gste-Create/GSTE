# GSTE Beta V0.1 — Installation and GUI Guide

This document combines installation and GUI operation into one workflow. First-time GSTE users only need to start here.

## 1. Install / Launch

### Recommended: Installer version

1. Obtain `GSTE_Beta_V0.1_Setup.exe`.
2. Run the installer and follow the on-screen instructions.
3. After installation, open **GSTE** from the Windows Start menu. If a desktop shortcut was created during installation, you can use it instead.

General users do not need to install Python separately; the official Beta installer includes the runtime required to run GSTE.

> If GSTE does not start, see [`TROUBLESHOOTING.md`](TROUBLESHOOTING.md).

## 2. Select Language

The GUI can switch between **Traditional Chinese** and **English**. Changing the interface language does not change the arrangement result.

## 3. Select Input Mode

### Two-hand Piano

The current GUI requires two files:

- **Melody / Right-hand MusicXML**
- **Left-hand / Accompaniment MusicXML**

Both files are processed together by the GSTE piano-arrangement workflow.

### Melody Only

Select one melody MusicXML file. GSTE uses the current Beta Auto arrangement workflow to determine harmony and accompaniment automatically.

### Ensemble Score

The entry is reserved, but **it is not available in Beta V0.1**.

## 4. Select Output Folder

Click **Select** to choose the output location. Each conversion creates a separate result folder so that the previous conversion is not overwritten directly.

## 5. Start Conversion

After confirming the input files and output location, click **Start Conversion / Convert**.

When conversion succeeds, the GUI displays a completion message and provides:

- **Open finished score**
- **Open output folder**

The main result for general users is:

`GSTE_TAB.musicxml`

Open it with software that supports MusicXML and review the result manually.

## 6. After Conversion

A successful conversion folder mainly contains:

```text
Score_Name_GSTE/
├─ GSTE_TAB.musicxml
├─ CONVERSION_REPORT.md
├─ PRIVACY_SAFE_DEBUG_REPORT.md
└─ debug/
```

For normal use, start with `GSTE_TAB.musicxml`. When reporting an issue, share `PRIVACY_SAFE_DEBUG_REPORT.md` first. The `debug/` folder retains more complete engineering diagnostics and may contain more detailed score or local-system information. Do not upload the entire `debug/` folder unless you have confirmed that its contents can be shared and the maintainer specifically needs it.

See [`OUTPUT_GUIDE.md`](OUTPUT_GUIDE.md) for details.

# GSTE — Guitar Score Transcription Engine

**語言 / Language / 言語：** [繁體中文](#zh-tw) · [English](#en) · [日本語](#ja)

---

<a id="zh-tw"></a>

## 繁體中文

**GSTE V0.4 beta（GAR 編曲索引實驗版）**可將 MusicXML 樂譜轉換為指彈吉他五線譜與 TAB。一般轉換在本機執行，不依賴 AI。


## 下載

請至 **Releases** 下載 `GSTE Beta V0.4.exe`。可執行檔是否隨文件包附帶，請以實際發布內容為準。

## 功能

| 模式 | 輸入與行為 |
|---|---|
| Melody + Auto | 輸入一份主旋律 MusicXML，自動生成伴奏。 |
| Melody + None | 輸入一份主旋律 MusicXML，不添加伴奏。 |
| Piano | 分別輸入主旋律／右手與伴奏／左手 MusicXML，分析來源伴奏後重新配置。 |
| Ensemble（實驗） | 輸入主旋律與 1–4 份伴奏 MusicXML，伴奏軌指定為 GUITAR 或 BASS。 |

團譜建議先使用 1–2 條伴奏軌（介面最多支援四條）。多軌會整合為單把指彈吉他的編曲，不保證完整保留每條來源音軌。各軌依樂器角色使用固定的 Harmony/Bass/Texture/Rhythm 權重。Piano 模式仍可獨立使用。

## GAR 編曲索引（V0.4 beta）

GAR 可顯示當前小節的 TAB、選取主旋律音符、提供雙音建議，以及顯示和弦指法與伴奏配置的 TAB 示意。除了直接查看剛完成的轉換結果，也可選擇先前轉換結果中的 `GSTE_EDITOR_CONTEXT`，重新載入對應樂譜供參考。

**GAR 目前為唯讀工具。** 不會直接修改樂譜、重新執行 Joint 編曲或輸出修改版。建議候選為簡化的靜態參考，不保證手型與節奏完全符合原譜。

詳見 [GAR 使用指南](docs/zh-TW/user/GAR_GUIDE.md)。

## Demo

`demo/` 收錄六份 **V0.3 實際自動轉換結果**：四份主旋律、一份鋼琴及一份團譜案例。每份保留輸入、最終 TAB、轉換報告與來源授權資訊；轉換後的音符與指法未經人工修改，也未使用 V0.4 beta 或 GAR 重新生成。

請見 [Demo 清單](demo/README.md)。公開授權不代表演奏品質已通過審查；仍須人工確認音樂性、指法與排版。樂譜授權以各案例的 `SOURCE_LICENSE.md` 為準。

## 文件與政策

- [繁體中文文件索引](docs/zh-TW/README.md)
- [操作指南](docs/zh-TW/user/GETTING_STARTED.md)
- [目前限制](docs/zh-TW/user/CURRENT_LIMITATIONS.md)
- [問題回報](docs/zh-TW/user/ISSUE_REPORT_GUIDE.md)
- [V0.4 beta 發行說明](RELEASE_NOTES_V0.4_beta.md) · [V0.3 發行說明](RELEASE_NOTES_V0.3.md)
- [使用條款](BETA_TERMS.md) · [隱私政策](PRIVACY.md) · [AI 政策](AI_POLICY.md) · [第三方元件聲明](THIRD_PARTY_NOTICES.md)

GUI 支援繁體中文、英文及日文。GSTE 可執行版本依隨附條款提供；本文件包不授予 GSTE 原始碼的開源授權。歡迎回饋音樂性、音軌保留及操作體驗。

---

<a id="en"></a>

## English

**GSTE V0.4 beta (experimental GAR arrangement reference)** converts MusicXML scores into fingerstyle guitar staff notation and TAB. Standard conversion runs locally without AI.


## Download

Go to **Releases** to download `GSTE Beta V0.4.exe`. Check the actual release contents to see whether the executable is included in a particular package.

## Features

| Mode | Input and behavior |
|---|---|
| Melody + Auto | One melody MusicXML file; accompaniment is generated automatically. |
| Melody + None | One melody MusicXML file; no accompaniment is added. |
| Piano | Separate melody/right-hand and accompaniment/left-hand MusicXML files; the source accompaniment is analyzed and rearranged. |
| Ensemble (experimental) | A melody plus 1–4 accompaniment MusicXML files, each assigned a GUITAR or BASS role. |

For ensemble conversion, start with one or two accompaniment tracks (the interface supports up to four). Multiple tracks are combined into a single fingerstyle guitar arrangement; full preservation of every source track is not guaranteed. Each track uses fixed Harmony/Bass/Texture/Rhythm weights based on its instrument role. Piano mode is also available independently.

## GAR Arrangement Reference (V0.4 beta)

GAR displays TAB for the selected measure, lets you select melody notes, and provides double-stop suggestions and TAB diagrams for chord fingerings and accompaniment arrangements. You can inspect the most recently converted score or load a previously converted score by selecting its `GSTE_EDITOR_CONTEXT` file.

**GAR is currently read-only.** It does not edit scores, rerun the Joint arrangement process, or export modified scores. Suggestions are simplified static references and are not guaranteed to match the original rhythm or form playable fingerings.

See the [GAR guide](docs/en/user/GAR_GUIDE.md).

## Demos

The `demo/` directory contains six **actual V0.3 automatic conversion results**: four melody, one piano, and one ensemble example. Each includes source inputs, final TAB, conversion reports, and source-license information. The converted notes and fingerings have not been manually edited, and the demos have not been regenerated using V0.4 beta or GAR.

See the [demo list](demo/README.md). Permission to distribute a score does not establish musical quality or playability; musical content, fingering, and rendering still require human review. Each example's `SOURCE_LICENSE.md` governs its score licensing.

## Documentation and policies

- [English documentation index](docs/en/README.md)
- [Getting started](docs/en/user/GETTING_STARTED.md)
- [Current limitations](docs/en/user/CURRENT_LIMITATIONS.md)
- [Issue reporting](docs/en/user/ISSUE_REPORT_GUIDE.md)
- [V0.4 beta release notes](RELEASE_NOTES_V0.4_beta.md) · [V0.3 release notes](RELEASE_NOTES_V0.3.md)
- [Terms](BETA_TERMS.md) · [Privacy](PRIVACY.md) · [AI policy](AI_POLICY.md) · [Third-party notices](THIRD_PARTY_NOTICES.md)

The GUI supports Traditional Chinese, English, and Japanese. The executable is distributed under the included terms; this documentation package does not grant an open-source license to GSTE source code. Feedback on musical quality, track preservation, and usability is welcome.

---

<a id="ja"></a>

## 日本語

**GSTE V0.4 beta（GAR 編曲リファレンス実験版）**は、MusicXML 形式の楽譜をフィンガースタイルギター用の五線譜と TAB 譜に変換するソフトウェアです。通常の変換処理はローカルで実行され、AI を必要としません。


## ダウンロード

**Releases** から `GSTE Beta V0.4.exe` をダウンロードしてください。実行ファイルが各配布パッケージに含まれるかどうかは、配布内容をご確認ください。

## 主な機能

| モード | 入力と動作 |
|---|---|
| Melody + Auto | 旋律の MusicXML ファイルを一つ入力し、伴奏を自動生成します。 |
| Melody + None | 旋律の MusicXML ファイルを一つ入力し、伴奏は追加しません。 |
| Piano | 旋律／右手と伴奏／左手の MusicXML ファイルを別々に入力し、元の伴奏を解析して再配置します。 |
| Ensemble（実験的機能） | 旋律と 1～4 本の伴奏 MusicXML ファイルを入力し、各伴奏トラックに GUITAR または BASS を指定します。 |

アンサンブル変換では、まず 1～2 本の伴奏トラックから試すことを推奨します（画面上は最大四本まで対応）。複数のトラックを一本のフィンガースタイルギター編曲に統合するため、各トラックの全音符が保持されるとは限りません。各トラックには楽器の役割に応じた Harmony/Bass/Texture/Rhythm の固定ウェイトが適用されます。Piano モードは単独でも利用できます。

## GAR 編曲リファレンス（V0.4 beta）

GAR では、選択した小節の TAB 譜を表示し、旋律音の選択、重音候補の確認、コード運指や伴奏配置の TAB 図による参照ができます。直前に変換した楽譜に加え、以前の変換結果に含まれる `GSTE_EDITOR_CONTEXT` を選択して、対応する楽譜を再表示することもできます。

**現在の GAR は読み取り専用です。** 楽譜の直接編集、Joint 編曲処理の再実行、編集済み楽譜の書き出しには対応していません。候補は簡略化された静的な参考情報であり、運指の実現可能性や元のリズムとの完全な一致は保証されません。

詳しくは [GAR 使用ガイド](docs/ja/user/GAR_GUIDE.md) をご覧ください。

## デモ

`demo/` には、**V0.3 で実際に自動変換した六つの結果**（旋律四件、ピアノ一件、アンサンブル一件）を収録しています。各例には入力ファイル、最終 TAB、変換レポート、原資料のライセンス情報が含まれます。変換後の音符や運指には手作業で修正を加えておらず、V0.4 beta や GAR による再生成も行っていません。

[デモ一覧](demo/README.md) をご覧ください。公開許諾と演奏品質の確認は別の問題です。音楽的な自然さ、運指、表示結果は人による確認が必要です。各楽譜の利用条件は `SOURCE_LICENSE.md` に従ってください。

## ドキュメントとポリシー

- [日本語ドキュメント一覧](docs/ja/README.md)
- [GAR 使用ガイド](docs/ja/user/GAR_GUIDE.md)
- [V0.4 beta リリースノート](RELEASE_NOTES_V0.4_beta.md) · [V0.3 リリースノート](RELEASE_NOTES_V0.3.md)
- [利用規約](BETA_TERMS.md) · [プライバシー](PRIVACY.md) · [AI ポリシー](AI_POLICY.md) · [サードパーティーに関する通知](THIRD_PARTY_NOTICES.md)

GUI は繁体字中国語、英語、日本語に対応しています。実行ファイルには同梱の利用規約が適用され、この文書パッケージは GSTE のソースコードにオープンソースライセンスを付与するものではありません。音楽的な品質、トラックの保持、操作性についてのご意見を歓迎します。

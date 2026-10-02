# GSTE Beta V0.2 — 目前限制與使用注意事項

[繁體中文](#繁體中文) · [English](#english)

## 繁體中文
GSTE 仍處於 Beta。公開版本的目標是逐步驗證轉換正確性、穩定性、可除錯性與指彈吉他配置，而不是宣稱所有 MusicXML 都能自動產生完成品。

## 目前限制

- 主要輸入格式為 MusicXML（`.musicxml` / `.xml`）。
- 公開流程以 Piano 與 Melody 路徑為主；團譜尚未開放。
- Piano 模式目前假設主旋律主要位於右手，左手主要提供 Bass、和聲或伴奏。
- **旋律跨左右手、兩手皆包含必要旋律、複雜多聲部或高度依賴鋼琴延音關係的作品，目前可能不適合直接使用 Piano 模式。**
- 《月光奏鳴曲第一樂章》目前已知不適合作為此版本 Piano 模式的成功示範，因此不應列在公開成功 Demo 中。
- Melody 路徑可依 GUI 選項進行自動伴奏，或使用「僅主旋律／不加自動伴奏」功能。
- 僅主旋律模式仍受吉他音域、同時發音、把位與實際指法限制，不代表所有輸入音符都能在完全不修改的情況下配置。
- 自動編曲仍可能出現音樂性、節奏、和聲、伴奏密度、延音、把位、指法或排版問題。
- MusicXML Export 仍需以外部閱讀器重新開啟確認。成功寫出檔案不等於 notation serialization 已完全正確。
- 成功轉換不代表作品已達可直接演出或公開的品質。

## 建議處理方式

遇到不符合目前 Piano 假設的作品時，不應持續強迫同一路徑產生結果。可先重新整理主旋律／角色資料，再評估使用 Melody 或僅主旋律路徑。

若某首作品在新版發生 regression，請保留輸入、版本號與 Privacy-Safe report，並先確認其他既有測試曲是否受到相同修改影響。

## English

GSTE Beta V0.2 aims to validate conversion accuracy, stability, diagnosability and fingerstyle-guitar placement. It does not claim to turn every MusicXML score into a finished arrangement.

### Current limitations

- MusicXML (.musicxml / .xml) is the main input format.
- Public workflows are Piano and Melody; group-score processing is not available.
- Piano mode assumes melody is mainly in the right hand and bass, harmony or accompaniment mainly in the left.
- **Melody crossing hands, indispensable material in both hands, complex polyphony or heavy dependence on piano sustain may be unsuitable for direct Piano input.**
- Moonlight Sonata, first movement, is a known unsuitable successful-demo candidate for this Piano workflow and is not included in the public successful set.
- Melody mode can use automatic accompaniment or melody-only conversion without accompaniment, according to GUI options.
- Melody-only conversion still obeys guitar range, simultaneous-note, position and fingering limits. It does not guarantee that all input notes can be placed without changes.
- Automatic arrangement may still produce musical, rhythmic, harmonic, accompaniment-density, sustain, position, fingering or layout problems.
- Reopen MusicXML exports in an external reader. Writing a file successfully does not prove correct notation serialization.
- Conversion success does not mean the work is ready for performance or publication.

### Recommended handling

Do not repeatedly force scores outside Piano mode's assumptions through that workflow. Reorganize the melody / role material and consider Melody or melody-only input.

If a score regresses in a newer version, retain its input, version identifier and privacy-safe report. Check whether the same change also affects existing test pieces.

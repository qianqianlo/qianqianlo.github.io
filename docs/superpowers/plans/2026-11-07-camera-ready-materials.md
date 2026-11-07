# Camera-Ready Materials Alignment

> Execute the user-approved factual update inline. Use executing-plans; preserve the existing decks rather than redesigning them.

**Goal:** Align the current CoRL and IROS presentations, their speaker materials, and active website downloads with the final camera-ready papers.

**Architecture:** Preserve slide order, themes, animations, and embedded media. Use Artifact Tool for editable replacement tables, then apply focused OOXML updates to the original package so unsupported media are not lost. Validate in PowerPoint and synchronize only the active copies.

**Tech Stack:** Artifact Tool JavaScript, XML/ZIP parsers, native PowerPoint rendering, GitHub Pages.

**Spec:** User approval: "全部更新到最终camera ready版本". Authorities are the 47-page RoboLineage camera-ready PDF and the 8-page Geometric Entropy camera-ready PDF already verified in the website update.

## Constraints

- Keep historical v1-v5/v8 files unchanged; produce clearly named camera-ready revisions and update the active convenience/download copies.
- Keep all 21 CoRL slides, their original layout, and every embedded video/audio byte.
- CoRL Table 1 leakage: 11.3, 9.8, 7.2, 6.2, 4.6, 2.1 for the six relevant structured-review rows.
- Effort stages: expert 10.1/40.5/59.2/20.4; RoboLineage 2.3/40.6/9.4/2.0 minutes, totals 130.2/54.3.
- Match every Table 3 value, not just RoboLineage; distinguish round diagnostics from independent final testing.
- Do not relabel digitized or illustrative data as exact measurements. Use original paper figures when raw data are unavailable.
- Preserve older homepage research entries and contribution marks.
- PPTX files are local deliverables only. Remove the previously added IROS website PPTX button and asset; do not add a CoRL slide download.

## Tasks

- [x] Extract an executable assertion set from paper Tables 1, 3 and 11; confirm the current CoRL deck fails it.
- [x] Render relevant original slides; repair native summary values, table images, chart cache/workbook, labels, and speaker notes. Use editable tables for the two replacement tables.
- [x] Independently audit the current IROS deck and script; correct only concrete differences from its final paper, preserving documented uncertainty.
- [x] Validate slide count, exact values, chart/workbook agreement, XML relationships, media hashes, PowerPoint renders, and unchanged-slide content.
- [x] Back up the active input, save clearly named final local presentation/PDF/script copies, remove website slide assets, and verify their removal online.

## Review Focus

- Numbers embedded in images are not covered by text-only replacement.
- A native chart cache and its embedded workbook must agree.
- Old numerical statements in notes/scripts can survive a correct visual slide.
- Imports can drop media, animations, fonts, or theme details; final source-package preservation must be verified.
- Updated numbers must retain denominators, trial counts, and rounding semantics.

## Execution Notes

- Spaces import rejected the 104 MB CoRL deck because its Office-input limit is 32 MB. Use a local PPTX fallback with the original package retained.
- The existing website update is deployed; no old publication rows need editing.
- Local validation found three empty relationship IDs on existing slide 12 media-click actions. Remove only the empty IDs, preserving the media actions, complete video relationships, timing and embedded bytes; all other unrelated slide XML remains byte-identical.
- Both finalizers pass package, font, native-chart/workbook and first-party import checks. CoRL has 21 slides, IROS 14. The active website PPTX asset and link were removed in Geometric Entropy commit d292168, per the user's clarification.
- Native PowerPoint rendered both complete final decks and exported 21-/14-page PDFs. Unchanged-slide render comparisons are pixel-identical; all altered slides were inspected at full size.
- The estimated CoRL table-height warning was checked against its native render: no text/footer overlap. IROS overlap warnings belong to unchanged progressive-reveal layers and remain as in the source.
- Live verification: the GE website contains no PPTX link, and the old PPTX URL returns HTTP 404.
- Independent final review found no critical or important issues; exact paper tables, 17 native charts/workbooks, notes/scripts, relationships and media preservation passed.
- Saved CoRL v6 and IROS v9 camera-ready revisions, their PDFs and scripts in the original presentation folders. Backed up both active Downloads PPTX files before replacing them. Historical versions remain unchanged.

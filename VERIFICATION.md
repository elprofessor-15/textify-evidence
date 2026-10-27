# Verification

Verified locally on October 27, 2026, with Node 24 and Google Chrome.

- `npm run build`: passed.
- `npm test`: 6 tests passed. Covers keyword/category search, percentage-point and relative calculations, zero baseline, negative deltas, quoted/CRLF CSV parsing, invalid CSV rejection, full citation exports, and curated-record provenance fields.
- Local HTTP server: returned 200 at http://127.0.0.1:5178/.
- Browser: searching “renewable” returned only the two IRENA records.
- Browser: saved two findings and verified they remained after reload.
- Browser: inspected reported values and +17 percentage points / 30.9% relative change for 55% to 72% adoption.
- Browser: citation-copy action showed successful feedback. The browser automation clipboard reader did not independently return the copied text, so system clipboard contents were not independently verified.
- Browser: CSV data and Markdown brief export controls were exercised. Brief export showed download feedback. The automation download event did not resolve, and completed files on disk were not independently verified. Export content generation is covered by automated tests and an example is included under `examples/`.
- Browser: imported a pasted CSV with required provenance; verified the resulting chart card; removed the disposable test record through the UI.
- Automated native file-picker upload was blocked by the Chrome extension's file-URL access setting. CSV paste import was verified end to end; native file selection remains unverified.
- Mobile: at 390 x 844, document width equaled viewport width (390 px), four cards rendered in a single column, and the detail dialog width was 390 px. Escape dismissed the dialog.
- Browser console: no captured errors or warnings in the final check.
- Three actual screenshots captured and visually inspected. The source-detail capture shows the upper part of a scrollable drawer.

No claims of live Textify integration, extraction quality, production scale, revenue impact, or feature absence are made.

# Transfer Study Coach Pipeline

A sanitized archival snapshot of a Google Apps Script prototype for spaced vocabulary review, problem re-review, and study-pattern summaries. This is not a production deployment.

## Files

- `Code.gs.txt` is attached to the `v0.1.0-archival-snapshot` release. It contains 41,848 Unicode characters (48,229 UTF-8 bytes), SHA-256 `96d2a1b54bb20d270e4bf040ba49de5f21c514035195985b0232447e0ecf48fe`.
- `TEST_SPREADSHEET_ID` remains `REPLACE_WITH_TEST_SPREADSHEET_ID`. Personal study data, actual source links, and spreadsheet identifiers are excluded.
- `appsscript.json` is in the repository root. It specifies the V8 runtime, `Asia/Seoul`, and only the `spreadsheets.currentonly` OAuth scope.

## Validation and limits

The published `Code.gs.txt` is an earlier archival snapshot. A separate later source of 47,110 characters was reported to pass five recovery/date-boundary cases and two overlapping concurrent-save cases in isolated Apps Script tests. The menu popup was not verified because the test environment lacked the required `script.container.ui` permission. Those results do not establish that this earlier snapshot passed those tests.

The script was not executed or deployed during publication, and the original Apps Script project and spreadsheet were not modified. No live-use safety validation is claimed.

## Safe use

Keep `TEST_SPREADSHEET_ID` as a placeholder unless using a dedicated disposable synthetic test spreadsheet. Do not substitute an original or live study spreadsheet ID. `setupPipeline()` is disabled in this snapshot. `runSyntheticIntegrationTests()` creates tabs and writes synthetic rows to the spreadsheet selected by `TEST_SPREADSHEET_ID`; never run it against an original or live spreadsheet.

# Transfer Study Coach Pipeline

This repository contains a sanitized snapshot of the latest source read from the separate Apps Script test project. It is an isolated synthetic-test project, not a production deployment.

## Files

- `Code.gs.txt`: 47325 Unicode characters, 53796 UTF-8 bytes; SHA-256 `26375ae684ad0bf9508677889a382370955a6d34489e2c560cdc149014eb907b`. An identifier altered during anonymization was normalized to `isSyntheticQuestion`. This correction was not compile-tested.
- `appsscript.json`: V8 runtime, `Asia/Seoul`, and only the `spreadsheets.currentonly` OAuth scope.
- The real spreadsheet ID is replaced with `REPLACE_WITH_TEST_SPREADSHEET_ID`. Question identifiers are replaced with synthetic labels. Study materials and their links are excluded.

## What is included

The script contains the study-coach menu and logic for spaced vocabulary review, problem re-review, recovery/idempotency, coaching summaries, and synthetic tests. `setupPipeline()` is intentionally disabled in this isolated copy.

## Validation and limits

An earlier isolated Apps Script validation reported five recovery/date-boundary checks and two overlapping concurrent-save cases passing. The menu-popup route was not verified because the test environment lacked the `script.container.ui` permission. This report does not establish live-use safety. The source in this repository was not run or deployed during publication.

## Safe use

Do not substitute an original or live study spreadsheet ID. `runSyntheticIntegrationTests()`, `runSyntheticResumeTests()`, and `showConcurrentSyntheticTest()` create or modify synthetic tabs and rows in the spreadsheet selected by `TEST_SPREADSHEET_ID`; use only a dedicated disposable synthetic sheet. The original spreadsheet and existing Apps Script project were not modified.

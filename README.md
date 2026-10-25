# family-finance-dash

Hebrew (RTL) single-page dashboard that visualizes data from a restricted Google Sheet.

## How it works

- Plain HTML/JS, no build step. Chart.js is loaded from a CDN.
- Access is restricted: the page requires sign-in with Google, and only the authorized account can read the sheet. Data is loaded through the Google Sheets API (v4) after sign-in.
- The sheet is NOT public. Keep it shared with the authorized account only - never switch it to "Anyone with the link".
- The sheet link is stored in the browser's localStorage only; no data is stored anywhere but the sheet itself.
- Evidence document links and private labels live in restricted sheet tabs and are loaded only after sign-in; they are not part of this repository.

## Sheet format

First sheet tab, header row with these Hebrew columns:
תאריך | ילד | מטפל/ספק | מספר קבלה/חשבונית | סכום קבלה | סטטוס | סכום החזר | מספר בקשה/טופס | הערות

Columns are matched by header name, so column order can change.

## Hosting

Served as a static site (e.g. GitHub Pages) from the repository root.

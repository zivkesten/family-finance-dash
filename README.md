# family-finance-dash

Hebrew (RTL) single-page dashboard that visualizes data from a shared Google Sheet.

## How it works

- Plain HTML/JS, no build step. Chart.js is loaded from a CDN.
- On first visit the page asks for a Google Sheet link. The link is stored in the browser's localStorage only - nothing is hardcoded in this repo and no data is stored anywhere but the sheet itself.
- Data is read through the sheet's public gviz JSON endpoint, so the sheet must be shared as "Anyone with the link - Viewer".

## Sheet format

First sheet tab, header row with these Hebrew columns:
תאריך | ילד | מטפל/ספק | מספר קבלה/חשבונית | סכום קבלה | סטטוס | סכום החזר | מספר בקשה/טופס | הערות

Columns are matched by header name, so column order can change.

## Hosting

Served as a static site (e.g. GitHub Pages) from the repository root.

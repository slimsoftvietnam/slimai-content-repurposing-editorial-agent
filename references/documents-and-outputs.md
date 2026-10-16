# Documents, sheets, and deliverable layout

## Preferred output options

- Use connected Google Drive/Docs/Sheets skills when the user requests native Google files and the connection is available. Create a Google Doc for the full article/editorial package and a Google Sheet for the compact 7-day calendar when useful.
- Otherwise, create local editable files: DOCX for the article/package, XLSX or CSV for the calendar, and Markdown for source analysis or QA notes. Do not claim a Google file was created when only a local file exists.
- Keep the calendar import-friendly with complete copy in each row. Do not remove or rename the current required CSV fields. The minimal field schema is in [workflow and calendar](workflow-and-calendar.md).
- When an Excel calendar is requested, keep the canonical CSV intact and create a separate, formatted `.xlsx` with the same complete content plus usable date/time, image, and status fields. Follow [workbook, visual, and Sheets delivery](workbook-and-visuals.md).
- Use an understandable folder structure when exporting multiple assets, such as `content/<campaign>/blog/`, `facebook/`, `linkedin/`, `tiktok/`, `images/`, and `qa/`. Adapt to the existing project instead of relocating prior deliverables without a request.
- Preserve source files and existing work. Do not change sharing permissions or make private materials public to simplify document embedding.

## Google Sheet status controls

When creating/updating a Google Sheet, add data validation for the machine-readable statuses in the calendar guide. Keep `approved` distinct from `ready`; only explicit user approval for that specific post may set it. If the connected Sheets interface cannot add validation, keep the values consistent and note the limitation. See [Google Sheets data-validation examples](https://developers.google.com/workspace/sheets/api/samples/data).

## Suggested package contents

For a multi-channel campaign, deliver the complete blog and social copy, a minimal 7-day calendar if requested, final visual files with source/license notes, and a concise QA/source report. Avoid separate files that merely duplicate the complete `content` cells unless they improve review or handoff.

# Workbook, visual, and Google Sheets delivery

Read this reference when the requested output includes a styled Excel calendar, generated images, or a Google Sheets copy.

## Excel calendar

- Preserve `content_calendar.csv` as the canonical tracker unless the user asks to update it. Create a separate `.xlsx` for the presentation and handoff.
- Put one post per row and include the full ready-to-publish copy in the workbook. Keep fields limited to what production needs: proposed publish date/time with timezone, channel, title, complete content, media/asset, SEO fields for blogs, and status.
- Visually distinguish the title and compact summary from the data table. Use a restrained brand palette, readable typography, wrapped content, useful column widths, frozen headers, filters, and row heights that make long copy scannable. Do not merge cells inside the data table.
- For a proposed calendar, label proposed dates and times clearly and retain `ready` unless a platform has actually confirmed scheduling. Preserve `published` and `needs_video` when supported by the source tracker.
- Add a status dropdown with the machine-readable values from the calendar guide. Keep `approved` distinct from `ready`.
- Embed image previews when the workbook format supports them and include the asset filename/path or safe link needed to retrieve the full-size asset. Never label a TikTok still or storyboard image as a finished video.
- Before handoff, reopen or render the workbook and inspect it at normal viewing size. Ensure all 32-bit or unsupported features have not broken import compatibility.

## Visual assets

- Create images only when requested or useful to a specific deliverable; do not create a generic image for every post by default.
- For social cards, use the user's visual reference for palette, type hierarchy, contrast, and conceptual imagery. For blog covers and illustrations, use a separate blog reference if supplied. A rejected direction applies immediately: stop generating that asset type and omit rejected outputs from the handoff.
- Use an image-generation skill/tool for original artwork when available. Preserve the full-resolution output in the campaign's asset folder, use clear filenames, and map each image to the exact calendar rows that use it.
- For SlimAI blog visuals, use the supplied [`blog-style-reference.png`](../assets/blog-style-reference.png) as the ongoing art direction and [`logo-slimai.png`](../assets/logo-slimai.png) as the exact brand mark. Match the reference closely in palette, composition, texture, and mood. Create a distinct cover and a sufficient set of in-article illustrations for the article's major ideas or sections; each illustration should explain a key metaphor, process, or summary rather than repeat the cover. When text is requested, generate the short title on the cover and concise, source-grounded labels on illustrations directly with the image model. Inspect Vietnamese text carefully and regenerate images with misspellings. Never overlay replacement typography unless the user asks for it. Add the exact logo asset as a separate faithful image layer after generation; do not ask the image model to redraw, approximate, or invent the logo.
- Treat the assets folder and the workbook as one deliverable: whenever an image is created, corrected, or replaced (including a logo correction), update the matching workbook preview/embedded image or asset link in the corresponding calendar row. Reopen/render the finished workbook and confirm that it displays the latest image versions, not stale embedded copies. Keep stable descriptive filenames and map each image to the exact blog and cover/section placement.
- Deliver a complete campaign folder so the workbook, website, and full-resolution media travel together. Use a structure such as `content-calendar-YYYY-MM-DD/` with `SlimAI_Content_Calendar_7_Days_YYYY-MM-DD.xlsx`, `index.html` (when a responsive presentation is requested), `data/calendar.json`, and `assets/`. Keep every generated image and the exact logo under `assets/`; do not leave references to temporary or machine-specific paths. Include an `assets/asset-manifest.json` that maps each filename to the post ID, channel, role (cover, section illustration, social visual, or TikTok storyboard), alt text, and any needed placement note. The website must resolve all media from this bundled assets folder.

## Responsive calendar presentation

- When requested, create a mobile-first, accessible, static web presentation alongside the Excel/Sheet deliverables. It should show the calendar week, publish date and timezone, channel, title, full ready-to-publish copy, image preview, and actual production status. Support practical filtering by date/channel/status and text search when the calendar has enough rows to benefit from them. Use clear links to the authoritative Google Sheet and any full-size assets.
- Generate the website from the same canonical calendar data as the workbook; do not hand-maintain a second divergent version. Keep copy and asset paths in a local JSON data file and local assets, avoid credentials or unapproved public APIs, and make the page work at narrow mobile widths without horizontal scrolling. Preserve `published`, `ready`, `approved`, and `needs_video` as distinct states.
- Before handoff, verify that the page loads, filters work, all local image paths resolve, long copy is readable, keyboard focus is visible, and the 375px mobile layout has no horizontal overflow. If hosted, retain the existing audience; new calendar pages should be private unless the user explicitly requests wider access.
- If a user supplies a newer art direction, use it for that request and update these references only when the user wants it to become the ongoing SlimAI default.
- Keep images as image assets; put post copy in spreadsheet cells. Do not bake lengthy post text or unverified claims into an image. Do not copy third-party logos, names, or distinctive brand assets from references.
- A generated asset has no external source URL/license to cite; label it as AI-generated. For sourced external assets, record the source URL, creator, license/terms, and attribution.

## Google Sheets import

- If the user asks for a Google Sheet and the connected Drive integration is available, import the completed `.xlsx` as a native Google Sheet in the account the user selected. If the user has not identified the account and multiple accounts are connected, ask before writing.
- Keep the native sheet usable: confirm the tab and populated row count, add a native table/filter and status dropdown when supported, and verify that the imported content and status values match the workbook.
- Keep image assets private by default. Embed them into the workbook/sheet or provide private Drive files with usable links; never make a folder or asset public merely to make `IMAGE()` work.
- Report the native Google Sheet link and account used. Do not claim successful upload until the native spreadsheet is confirmed.

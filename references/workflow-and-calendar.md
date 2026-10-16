# Workflow and editorial calendar

## Production statuses

Use these machine-readable values in the existing `status` column:

`draft` → `ready` → `approved` → `drafted` / `scheduled` / `submitted` → `published`

- `draft`: work has started and is incomplete.
- `ready`: copy is complete and awaiting review. It is **not** publication approval.
- `approved`: the user explicitly approved this specific row and destination for publication.
- `drafted`: a publisher/platform confirms a saved draft exists.
- `scheduled`: the platform confirms a scheduled post exists.
- `submitted`: an immediate publish request was accepted, but the public post is not yet confirmed.
- `published`: the post is visibly live or otherwise confirmed by platform evidence.
- `needs_video`: the TikTok script is complete but a rendered video is missing.
- `blocked`: progress needs a source, asset, decision, correction, login, or platform-side action.

Do not promote statuses based on intention. Record publication confirmation/permalink in the handoff or an existing notes field if one is introduced by the user; do not add columns to the minimal import schema by default. `ready` rows from earlier calendars remain unapproved until the user explicitly approves them.

## Calendar conventions

- One row represents one channel deliverable. Put the complete, channel-ready copy in `content`, including TikTok script, caption, and hashtags.
- Preserve this header, order, and existing rows:

  `publish_at,channel,title,content,media_url,seo_slug,meta_title,meta_description,focus_keyword,status`

- Keep the calendar minimal. Do not add owner, rationale, campaign, priority, or separate draft-link columns unless the user requests them.
- `publish_at` is an ISO 8601 timestamp with timezone, normally `Asia/Ho_Chi_Minh`. If timing is unknown, leave it blank. If proposing dates for a seven-day plan, label the dates/times as proposals in the handoff and do not imply user confirmation.
- Leave `media_url` blank until a final media asset exists. For TikTok, set `needs_video` until the video is rendered and attached.
- Blog rows should populate `seo_slug`, `meta_title`, `meta_description`, and `focus_keyword`; leave these blank for social posts.
- Do not store credentials, access tokens, or private personal data in the calendar.
- Correctly quote commas, quotes, and line breaks inside CSV cells. Read and preserve the current CSV before editing; do not reset/rebuild it to apply new guidance.

## Channel content requirements

### SEO blog

Capture the intended query and intent, researched primary and related terms, title/meta title, meta description, stable lowercase slug, answer-first introduction, four to six useful H2 sections where suitable, substantive examples/steps/limitations, verified internal/external link suggestions, and quality notes. Use enough depth to answer the query; do not pad to a word count. Add FAQs only for distinct, useful questions. Separate observations about search results from measured search volume. See [quality and assets](quality-and-assets.md).

### Facebook

Open with a concrete reader situation or takeaway, use short paragraphs and natural Vietnamese, make one point, and finish with one clear CTA. Use a small relevant hashtag set only when it fits the brand.

### LinkedIn

Use a professional, work-relevant observation, lesson, or framework. Explain its practical implication and finish with a specific CTA. Give it a distinct structure and argument from the Facebook post.

### TikTok

Write a recordable vertical-video plan with timecodes, spoken lines, on-screen text, and visual/action cues. Open with a visual and spoken hook, develop one idea with concrete examples or changes of shot, and close with a spoken CTA. If no duration is specified, propose 30–45 seconds. Include caption and hashtags in the same calendar cell. Never label a script as a produced video.

## SEO content safeguards

- Search current results and official/reliable sources when research tools are available. Cite any external factual additions in the article or source notes.
- Distinguish supplied-source claims from independently checked facts; flag claims that remain unverified.
- Never fabricate search volume, ranking likelihood, expertise, first-hand experience, or internal links. If the website inventory is unavailable, propose link topics without inventing URLs.
- Prioritize reader value, clear hierarchy, explanatory detail, and natural language over keyword repetition. Google documents the people-first and search fundamentals guidance in its [SEO Starter Guide](https://developers.google.com/search/docs/fundamentals/seo-starter-guide) and [helpful content guidance](https://developers.google.com/search/docs/fundamentals/creating-helpful-content).

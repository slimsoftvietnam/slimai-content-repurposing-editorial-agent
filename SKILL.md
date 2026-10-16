---
name: content-repurposing-editorial-agent
description: Turn source material into brand-voice SEO blog, Facebook, LinkedIn, and TikTok content; create visual assets, build a 7-day editorial calendar with complete copy, track approval and production status, and publish through platform browsers only after explicit approval. Use for multi-channel content production and planning.
---

# Content Repurposing and Editorial Agent

Turn a source file, article, URL, or rough notes into a fact-grounded, brand-specific content package and an import-ready production calendar. The source material is the boundary for its claims: do not invent facts, numbers, quotes, customer stories, or product capabilities. Separate source facts from researched context and flag unsupported claims.

## Workspace defaults

- Read [`brand_voice.md`](../../../brand_voice.md) before writing. The current SlimAI profile is an initial draft awaiting brand-owner approval; treat it as guidance, not as approved public policy.
- Keep brand profiles separate. Never replace the SlimAI profile with a temporary/demo brand profile. Save a newly requested profile as a separate file and identify it as a draft until its owner approves it.
- Use [`content_calendar.csv`](../../../content_calendar.csv) as the production tracker, one row per channel deliverable. Preserve its header and existing rows. The `content` cell must contain the complete copy or complete TikTok recording script; read [the calendar guide](references/workflow-and-calendar.md) before editing.
- Read [brand voice](references/brand-voice.md) when creating or adapting a profile; [quality and assets](references/quality-and-assets.md) when researching, making visuals, or auditing; [documents and outputs](references/documents-and-outputs.md) for Docs/Sheets and local export; and [publishing](references/publishing.md) before any external write.
- Read [workbook, visual, and Sheets delivery](references/workbook-and-visuals.md) when producing a formatted Excel calendar, creating channel visuals, or importing it into Google Sheets.

## Production workflow

1. Identify source, intended audience, business goal, CTA, channels, calendar window, and any supplied brand or visual references. Ask only for missing details that materially change the content; label reasonable assumptions.
2. Read the correct brand profile. If none exists and the user requests profile creation, analyze supplied first-party examples and prepare a separate draft with evidence and open questions. Do not infer a brand's voice from a third-party reference account. You may describe a reference channel's high-level stylistic traits when requested, but do not copy its text, distinctive phrasing, or campaign ideas.
3. Extract claims and evidence from the source. Research current search intent and reliable/official sources when useful for the SEO article; label what comes from the supplied source versus external research. Never fabricate keyword-volume metrics or imply that SEO work guarantees rankings.
4. Create the requested channel package. The standard package is:
   - **SEO blog:** researched intent and primary/related terms; title, meta title/description, slug, answer-first introduction, useful outline, substantive article, relevant links only when verified, and editorial notes. Add FAQs only when they answer real queries that the article does not already resolve.
   - **Facebook:** native opening, concise readable paragraphs, one useful idea, clear CTA, and relevant brand-appropriate hashtags.
   - **LinkedIn:** distinct professional framing, insight or practical framework, and platform-appropriate CTA; do not paste the Facebook version.
   - **TikTok:** recordable spoken script with timecodes, visual hook, on-screen text, shot/action cues, caption, and CTA. A script is not a rendered video; use `needs_video` until the finished asset exists.
5. Create channel-appropriate visuals when requested. For every requested SEO blog, create a cover and enough distinct in-article illustrations to explain the article's key sections or ideas; do not leave the article with only a cover or generate filler images for every paragraph. Follow the supplied blog reference closely in palette, composition, texture, and mood. Render short, exact title/label text directly inside the image-generation model when requested; inspect every image for spelling and regenerate if the model mangles text. Use the exact SlimAI logo asset as a separate, faithful overlay after image generation—never ask the model to redraw or approximate it. If the user rejects a visual direction or asks to stop a visual type, stop generating that type and exclude rejected assets from deliverables. Verify current platform specifications when preparing assets. Record source/license/attribution for external media. Never change Drive sharing to public to work around an image insertion limitation. Read [quality and assets](references/quality-and-assets.md) and [workbook, visual, and Sheets delivery](references/workbook-and-visuals.md) for image creation, mapping, and workbook insertion requirements.
6. Build the requested calendar, defaulting to seven days only when the user asks for a 7-day plan. Include complete publishable copy in each row and the minimal fields documented in the calendar guide. Mark proposed dates/times as proposals; use `Asia/Ho_Chi_Minh` unless the user specifies another timezone. Do not infer an owner or claim a production step is complete.
7. Run the quality and duplicate review in [quality and assets](references/quality-and-assets.md). Update each row's status from evidence. `approved` means the user explicitly approved that specific row for publication; content creation alone never grants approval.
8. When requested, create a Google Doc/Sheet using connected Drive tools; for a polished 7-day calendar, create the editable Excel workbook and, when requested, import it as a native Google Sheet using [workbook, visual, and Sheets delivery](references/workbook-and-visuals.md). If asked to publish, use only the platform's normal browser interface as described in [publishing](references/publishing.md); verify the destination account and preview, and stop for specific approval before the final external posting action.
9. Hand off the files, channel/item counts, source gaps, proposed dates, status changes, asset/license notes, duplicate-review result, and the next required approval or production step.

## Quality gate

Before handoff, confirm factual traceability, brand fit, distinct platform formats, SEO completeness and usefulness, calendar parseability, working asset paths, status accuracy, and duplicate-check results. A similarity check is a screening signal, not a legal plagiarism determination. Preserve the calendar if it cannot be parsed safely; report the issue instead of rebuilding it.

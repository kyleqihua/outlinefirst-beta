# OutlineFirst privacy notice

Last updated: 2026-09-03

OutlineFirst automatically processes video captions when the user opens a supported YouTube video
while the OutlineFirst panel is visible. Hiding the panel stops new caption and brief processing
until the user opens it again.

## Data flow

1. The extension reads the active video's available captions, title, and description from YouTube.
2. It sends the title, description, caption text, and timestamps to the OutlineFirst Cloudflare
   Worker.
3. The Worker sends that content to DeepSeek to correct obvious caption errors and generate a
   structured brief.
4. The extension validates the returned timestamps and stores the brief in Chrome local storage so
   the same video can reopen faster.
5. The Worker keeps aggregate operational records needed to measure service reliability and cost:
   request time, completion status, model, token counts, estimated cost, latency, extension version,
   and a random per-request identifier used to prevent duplicate records. The Web Store release does
   not send or store a persistent installation identifier.

## What OutlineFirst does not do

- It does not require an account.
- It does not collect names, email addresses, payment information, or a persistent installation
  identifier.
- It does not include advertising trackers or per-user behavior analytics.
- It does not store the developer's DeepSeek API key in the extension.
- The Worker does not intentionally log caption text or generated briefs.

## Retention and control

Cached briefs stay in Chrome local storage on the user's device. Uninstalling the extension removes
extension storage. The beta keeps at most 30 cached briefs. Aggregate operational records are kept
for up to 90 days. They do not contain captions, titles, descriptions, generated briefs, page URLs,
or a persistent installation identifier.

Cloudflare processes the request and operational records, and DeepSeek processes the video content
needed to generate the brief, under their own service and privacy terms. Information received by
OutlineFirst is used only to provide or improve its single purpose, including maintaining and
measuring the reliability of that feature, in accordance with the Chrome Web Store User Data Policy.
This notice will be updated before any account, per-user analytics, payment, or additional data
collection feature is introduced.

# watchbrief privacy notice

Last updated: 2026-08-08

watchbrief processes video captions automatically while its panel is visible
on a supported YouTube video. Hiding the panel stops new processing.

## Data flow

1. The extension reads the active video's title, description, and available
   captions from YouTube while the panel is visible.
2. It sends the title, description, caption text, and timestamps to the
   watchbrief Cloudflare Worker.
3. The Worker sends that content to DeepSeek to generate a structured brief.
4. The extension validates the returned timestamps and stores the brief in
   Chrome local storage so the same video can reopen faster.

## What watchbrief does not do

- It does not require an account.
- It does not collect names, email addresses, browsing history, or payment
  information.
- It does not include analytics or advertising trackers.
- It does not store the developer's DeepSeek API key in the extension.
- The Worker does not intentionally log caption text or generated briefs.

## Retention and control

Cached briefs stay in Chrome local storage on the user's device. Uninstalling
the extension removes extension storage. The beta keeps at most 30 cached
briefs.

Cloudflare and DeepSeek process requests under their own service and privacy
terms. This notice will be updated before any account, analytics, payment, or
additional data collection feature is introduced.

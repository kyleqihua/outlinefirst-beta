# OutlineFirst privacy notice

Last updated: 2026-08-30

OutlineFirst processes video captions automatically while its panel is visible
on a supported YouTube video. Hiding the panel stops new processing.

## Data flow

1. The extension reads the active video's title, description, and available
   captions from YouTube while the panel is visible.
2. It sends the title, description, caption text, and timestamps to the
   OutlineFirst Cloudflare Worker.
3. The Worker sends that content to DeepSeek to generate a structured brief.
4. The extension validates the returned timestamps and stores the brief in
   Chrome local storage so the same video can reopen faster.

## Service operation data

On installation or update, the extension creates a random installation ID and
a random authentication token in Chrome local storage and registers that
installation ID and extension version with the OutlineFirst Worker. They are
not a name, email address, advertising ID, or third-party account. They let
OutlineFirst count installations, measure reliability and cost, and return
feedback replies to the correct installation. The database has an empty account
field for a possible future sign-in feature, but the current extension does not
create an account.

For each brief request, the Worker stores the installation ID, extension
version, request time, completion status, latency, DeepSeek input/output token
counts, and an estimated API cost. It does not store the video's title,
description, captions, or generated brief with that usage record.

If a user sends feedback inside the extension, OutlineFirst stores the message,
its processing status, the developer's reply, and limited troubleshooting
context: the current video ID and title, page URL, and the last OutlineFirst
error category. Feedback is optional. The extension shows the status and
developer reply only to the same authenticated installation.

## What OutlineFirst does not do

- It does not require an account.
- It does not collect names, email addresses, payment information, or a
  cross-site browsing history.
- It does not include advertising trackers or share an identifier with
  advertisers.
- It does not store the developer's DeepSeek API key in the extension.
- The Worker does not intentionally log caption text or generated briefs.

## Retention and control

Cached briefs stay in Chrome local storage on the user's device. Uninstalling
the extension removes extension storage. The beta keeps at most 30 cached
briefs.

Server-side usage events are removed after 90 days. Feedback and its reply are
removed after 365 days. An inactive installation record is removed after 365
days when it has no retained feedback. Users can request earlier deletion by
sending feedback from the installation and asking for its data to be deleted.

Cloudflare and DeepSeek process requests under their own service and privacy
terms. This notice will be updated before any account, analytics, payment, or
additional data collection feature is introduced or these practices change.

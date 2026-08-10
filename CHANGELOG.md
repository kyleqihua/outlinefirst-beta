# Changelog

## 0.1.3-beta

### Fixed

- The Chrome Web Store build now takes priority when an older unpacked beta is still
  installed.
- Caption and brief work pauses while the panel or YouTube tab is hidden.
- Temporary caption, network, and service failures recover automatically.
- Stale requests are cancelled during navigation, and stalled streams no longer load
  forever.
- Caption fallback and progressive brief rendering start sooner.
- Loading, error, and panel lifecycle transitions stay visually stable.

## 0.1.2-beta.3

### Fixed

- The panel now appears immediately when watchbrief is installed while a YouTube tab is already
  open.
- The extension stays ready when YouTube navigates from its home page to a video without a full
  page reload.

## 0.1.1-beta.2

The first bundled and minified watchbrief beta.

### Included

- Automatic, streaming briefs while the panel is visible
- A stable single panel across YouTube navigation
- Clickable chapter titles and timestamped brief points
- Playback highlighting and local caching
- Metadata-assisted correction for automatic-caption errors
- No background caption or model work while the panel is hidden
- Bundled, minified browser runtime code without source maps or server code

### Known limits

- Installation uses Chrome's **Load unpacked** flow.
- Unpacked extensions do not update automatically.
- Videos without readable captions cannot be summarized.
- The browser runtime remains inspectable, as required for a locally installed
  Chrome extension; sensitive prompts and credentials remain on the server.

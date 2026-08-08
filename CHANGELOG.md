# Changelog

## 0.1.1-beta.2

The current installable watchbrief beta.

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

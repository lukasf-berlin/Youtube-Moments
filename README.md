<div align="center">
  <img src="icons/icon.svg" alt="YouTube Moments icon" width="96" height="96">

# YouTube Moments

[![Firefox Add-on](screenshots/firefox-badge.png)](https://addons.mozilla.org/en-US/firefox/addon/youtube-moments/)

</div>

A lightweight browser extension for saving exact timestamps ("moments") from YouTube videos and revisiting them later.

> [!IMPORTANT]
> This is a personal project built with the assistance of AI (Claude).

## Features

- **Save moment** — Adds a button to the action row under any YouTube video. Clicking it captures the current playback timestamp and allows you to attach an optional note.
- **Moments page** — Click the toolbar icon to open a dedicated full-page manager with:
  - Search across notes, video titles, and channel names
  - Pagination for large collections
  - Inline editing and deletion of saved moments
  - Share a moment as a formatted message (for WhatsApp, Slack, etc.) or copy the timestamped link
  - Export to a JSON file and import from a previously exported backup
- **Local-only storage** — Moments are stored safely using the browser's local extension storage.

## Screenshots

![Moments screen (empty)](screenshots/moments-no-content.png)  
_Moments screen (empty)_

![Save moments button](screenshots/save-button.png)  
_Save moments button_

![Moments screen with items](screenshots/moments-content.png)  
_Moments screen (with moments)_

## Installation

Requires Firefox 140+ on desktop, or Firefox for Android 142+.

The easiest way to install is from the official Firefox Add-ons listing: [addons.mozilla.org/firefox/addon/youtube-moments](https://addons.mozilla.org/en-US/firefox/addon/youtube-moments/).

Once installed, the extension icon appears in the toolbar. Click it at any time to open the Moments page. Pin the icon to the toolbar for quick access.

### Installing from source (development)

1. Clone this repository.
2. Open `about:debugging#/runtime/this-firefox` in Firefox.
3. Click **Load Temporary Add-on…**.
4. Select the `manifest.json` file from the cloned repository.

## Usage

1. Open any YouTube video (`youtube.com/watch?v=...`).
2. Click **Save moment** below the video at the timestamp you want to bookmark.
3. Optionally enter a note, then confirm.
4. Click the extension toolbar icon to view, search, edit, export, or delete your saved moments.

## Permissions

- `storage` — Used exclusively to persist saved moments locally within your browser.

## Building a release

```bash
npm run lint   # validates manifest.json and source code with web-ext
npm run build  # packages the extension into web-ext-artifacts/*.zip
npm run dev    # runs the extension in a temporary Firefox instance for live testing
```

## License

MIT — see [LICENSE](LICENSE).

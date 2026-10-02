# MIME Type Lookup

A fast, searchable lookup between file extensions and MIME (media) types, in both directions. Around 200 common types are built in as an inline table, so it works with no external dependencies and works offline.

**Live demo:** https://0xelitesystem.github.io/mime-type-lookup/

## Use

1. Type a file extension (`.webp` or `webp`) or a MIME type (`image/` or `application/json`) into the search box.
2. Narrow the search with **All**, **By extension** or **By MIME type**.
3. Read the matching rows. Each is marked IANA for a registered type or common for a convention.

## Why this exists

Looking up a MIME type usually means a web search for a one-line answer. This tool keeps the table in the page and filters it as you type, in either direction, offline. It is one HTML file that runs in your browser, with no tracking and no server, under the MIT license.

## Features

- Search a file extension (like `.webp` or `webp`) to find its MIME type.
- Search a MIME type (like `image/` or `application/json`) to find matching extensions.
- Free-text search across extensions, MIME types, and short descriptions.
- Filter mode toggle: All, By extension, By MIME type.
- Around 200 entries covering text, image, audio, video, application, font, archive, and model types.
- Each row is flagged as an IANA registered media type or a common convention.
- Match highlighting and a live result count.
- Light and dark themes, keyboard-friendly, responsive.

## How it works

The full dataset is embedded in the page as an inline JavaScript array. Typing filters the table in the browser using plain string matching. A leading dot on an extension is tolerated, so `.png` and `png` behave the same. Registered types are marked "IANA"; entries that are widely used but not IANA registered (or are vendor and legacy conventions) are marked "common".

## Privacy

Everything runs in your browser. There are no network requests, no analytics, and no external scripts. Open the page source or the DevTools network tab to confirm nothing leaves your machine.

The only thing written to storage is your light or dark theme choice, saved in `localStorage` under the key `theme`.

## Run locally

```bash
git clone https://github.com/0xelitesystem/mime-type-lookup
cd mime-type-lookup
```

Open `index.html` in any modern browser. Or serve the folder with `python -m http.server 8000` and visit http://localhost:8000/.

## Build

No build step. The whole tool is one `index.html` file with its CSS and JavaScript inline, and nothing to install.

## More

Part of a catalog of single-file browser tools and plain-language references, all MIT licensed and dependency-free: [0xelitesystem.github.io](https://0xelitesystem.github.io/). Built by [elitesystem.ai](https://elitesystem.ai).

## License

MIT. Copyright 0xelitesystem 2026.

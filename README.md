# MIME Type Lookup

A fast, searchable lookup between file extensions and MIME (media) types, in both directions. Around 200 common types are built in as an inline table, so it works with no external dependencies and works offline.

## Live demo

https://0xelitesystem.github.io/mime-type-lookup/

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

## More

Part of a catalog of single-file browser tools and plain-language references, all MIT licensed and dependency-free: [0xelitesystem.github.io](https://0xelitesystem.github.io/). Built by [elitesystem.ai](https://elitesystem.ai).

## License

MIT. Copyright 0xelitesystem 2026.

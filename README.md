# HomeOS 0.7.0 — International TV directory

Replace index.html, style.css, app.js and manifest.webmanifest in the existing GitHub Pages repository. No local storage keys are changed.

## What changed
- Live TV mobile screen hides the redundant marketing hero to prioritise playback.
- Country filter appears alongside the existing region selector.
- **Add international channels** opens a country picker and imports the selected country’s public M3U playlist from https://iptv-org.github.io/iptv/countries/ (iptv-org).
- Imported entries receive explicit country metadata; new channels are appended and stream URL duplicates are skipped.
- Favourites, original 279 imported channels, saved watchlist, programme guide and diagnostics remain intact.
- Remote directory imports need network access and cross-origin permissions. A successful playlist import does not guarantee individual stream playback.

## Important
No new international streams are bundled. The app downloads them on user request from a public directory; this is not an offline channel catalogue. GitHub Pages cannot circumvent geo-restrictions, DRM or streaming rights.

# HomeOS 0.5.1 — Stabilisation

This is a drop-in update for HomeOS 0.5.0. Upload `index.html`, `app.js`, `manifest.webmanifest`, `README.md`, `VERSION.md` to the repository root, replacing existing files. Commit and visit `https://kingandcastle.github.io/homeos-prototype/?v=051#iptv`.

## Changes
- All Channels and Favourites buttons immediately below the player now share a single filter state with the channel browser.
- Favourite star toggles the saved status without changing the active group. Favourites persist in existing browser localStorage.
- Next/Previous and channel dropdown attempt playback on selection; autoplay restrictions may still require a user gesture.
- Empty favourites are explained.
- Stalled event while media time is still advancing no longer immediately reports a frozen stream.
- Entertainment service shortcuts use a more compact portrait layout; these are **not** synchronised movie posters or a Plex catalogue.
- Mobile navigation has improved horizontal scrolling and screen-space allowances.

## Verification
See TEST_REPORT.md. Static checks passed. Automated browser navigation was blocked by this environment, so real interactive and Safari tests remain unverified. Third-party stream access, autoplay and DRM are provider/browser dependent.

## Data
Existing localStorage key `homeos01` is preserved. Do not clear Safari website data if you want to retain imported channels, favourites and settings.

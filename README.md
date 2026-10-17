# HomeOS Prototype 0.2 — Live TV Beta

A responsive, static HTML/CSS/JavaScript application for GitHub Pages. All seven modules are retained. IPTV now has native-browser HLS, M3U playlist import, category and favourites filters, and XMLTV now/next.

## Run locally
Open `index.html` in a modern browser. For reliable storage and fetch behaviour, serve the directory with `python3 -m http.server 8000` and visit `http://localhost:8000`.

## Deploy to existing GitHub Pages
Replace the five root files in `kingandcastle/homeos-prototype` (`index.html`, `app.js`, `manifest.webmanifest`, `README.md`, `VERSION.md`). Commit changes; keep Pages set to `main` / `/(root)`. Wait for deployment, refresh Safari and check that the HomeOS brand says 0.2.

## Live TV instructions
1. Open IPTV & Live TV. Select **Sample: Flower** and press Play to verify basic MP4 playback.
2. Select **Sample: HLS test** and press Play in Safari to check native HLS. Stream availability can change.
3. Paste an authorised HTTPS M3U playlist or upload a local `.m3u` file. Optionally load an HTTPS M3U URL; remote import only works when the server permits browser CORS access.
4. Use search, the category selector and the favourites filter.
5. Upload an XMLTV file or paste XMLTV content. The XMLTV `<programme channel="...">` must match the playlist's `tvg-id` attribute. Select a channel to view Now/Next.

## Acceptance tests
- [ ] Site opens on iPhone Safari and displays version 0.2.
- [ ] All seven modules navigate correctly; no horizontal overflow.
- [ ] Flower MP4 loads and plays.
- [ ] HLS test stream loads and plays on a supported browser (if source is available).
- [ ] Valid pasted M3U creates channels.
- [ ] Local `.m3u` file imports channels.
- [ ] Category filter and search reduce displayed channels.
- [ ] Favourite button toggles channel; favourites-only view works.
- [ ] Invalid M3U displays an error without crashing.
- [ ] XMLTV with matching tvg-id shows Now/Next at the right times.
- [ ] Unsupported/expired stream produces a readable error.
- [ ] Reload retains local channels and favourites.
- [ ] Simulated smart-home switches, AI and settings still work.

## Limitations and security
This is a static frontend, not a native IPTV application. Only authorised streams should be used. No DRM bypass, credential storage, APK installation, OpenAI connection, or real smart-home control. Playlists and guide data are stored in browser localStorage; do not import private subscription URLs with tokens into a shared/public device. Public GitHub repositories should never contain private playlists or credentials. GitHub Pages cannot proxy inaccessible or CORS-blocked feeds.

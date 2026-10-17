# HomeOS Prototype 0.2.5

Upload the five files from this archive to the **root** of your existing GitHub Pages repository, replacing older copies, then commit. Visit https://kingandcastle.github.io/homeos-prototype/#iptv and refresh. The header and Settings → About should both show 0.2.5.

The app preserves saved playlist/settings in the same browser localStorage key. Select an authorised MPEG-DASH (.mpd) stream to load dash.js on demand from jsDelivr. Internet access is required for the DASH library; Safari HLS and ordinary MP4 do not depend on it. Playback depends on the browser, device codecs, stream access and any DRM requirements.

For troubleshooting, select a channel, wait for playback or an error, then View diagnostics → Copy diagnostics without refreshing. Reports include hostname but not full URLs.

## 0.2.5 changes
- Terminal playback failures remain visible even if late `waiting` or `stalled` events arrive.
- **Check source access** performs a browser CORS GET with an 8-second timeout and reports HTTP status/content type when visible. This is not a definitive stream or DRM test. The response body is cancelled rather than downloaded.
- Source-check results are included in copied JSON diagnostics.
- DASH error text redacts full URLs in the diagnostic event text.
- The UI and application version are 0.2.5.

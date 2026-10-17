# HomeOS 0.2.3 — Playback Diagnostics Fix

This is a complete five-file replacement for the existing HomeOS GitHub Pages repository. **Upload the contents of this ZIP to the repository root**, not a nested folder.

## Fix
A clearly labelled **Playback diagnostics — Version 0.2.3** panel appears immediately after the IPTV player/channel browser, before the broadcaster shortcuts and playlist manager. It contains **View diagnostics**, **Copy diagnostics**, **Download JSON** and a selectable report text box. The script URL is versioned to avoid Safari loading an older cached script.

## How to test
1. Upload all five files to the GitHub repository root, commit to `main`, and refresh the website.
2. Confirm the page says **HomeOS 0.2.3** and you can see **Playback diagnostics — Version 0.2.3** below the channel browser.
3. Select a BBC channel and attempt playback.
4. Tap **View diagnostics** then **Copy diagnostics**; paste the result into the ChatGPT conversation. If copying is blocked, select the report text manually or download JSON.
5. Test the Apple HLS demo again to ensure basic playback still works.

The report deliberately omits full stream URLs, tokens and cookies. It includes channel name, source hostname, browser information, media error and event timings; review it before sharing. The report helps narrow down errors but cannot itself prove why a remote broadcaster rejects playback.

**Important:** The UK playlist contains independently maintained links, some of which may be unavailable or protected. This build does not bypass broadcaster access controls or DRM. Local browser playlists and preferences are retained.

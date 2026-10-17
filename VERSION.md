# HomeOS Version 0.2.0 — Live TV Beta

Released: 17 October 2026

## Added
- Native HLS playback for browsers supporting `application/vnd.apple.mpegurl` (notably iOS Safari).
- HTTPS M3U playlist paste, local file upload and remote URL import (subject to CORS).
- Search, categories and favourites filtering.
- XMLTV local-file and paste import; now/next programme lookup by `tvg-id`.
- Explicit media error and buffering messages.
- Apple HLS demonstration stream, and retained working Flower MP4 regression test.

## Retained
Dashboard, simulated AI, Entertainment, App Centre, simulated Smart Home, Settings. Existing `homeos01` local data is reused.

## Known limitations
- HLS relies on native browser support; there is no hls.js fallback or transcoding backend.
- Provider CORS, HTTPS, DRM, token expiry and rights restrictions can block streams.
- XMLTV is manually imported, not automatically refreshed.
- XMLTV import capped at 5,000 entries, M3U at 500 channels.
- No backend, API keys, native app, real AI, or real home automation.

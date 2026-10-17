# HomeOS Prototype 0.2.1

Static responsive HomeOS prototype for GitHub Pages. No build tools or API keys required.

## Deploy

1. Open https://github.com/kingandcastle/homeos-prototype
2. Upload all five files from this ZIP to the repository root, replacing existing versions.
3. Commit to the branch used by GitHub Pages (typically main).
4. Open https://kingandcastle.github.io/homeos-prototype/#iptv and refresh Safari.

## Test on iPhone

1. Select **Use demo** and play Flower MP4.
2. Select the Apple HLS test stream; let it play for 3 minutes.
3. Import the UK M3U playlist again if needed (previous saved playlist should persist).
4. Play an authorised live stream. Check the session time and recovery count.
5. Use **Retry stream** if playback stalls.
6. Mark the stream **Working** or **Unreliable**, then test **Hide unreliable channels**.
7. Check that favourites, search, category filters, XMLTV and other HomeOS sections still work.

## Notes

Only one automatic retry is attempted after 12 seconds of no playback progress while the video is playing. Paused video is not treated as stalled. Safari and media provider behaviour can affect recovery. No provider restrictions or DRM are bypassed. Data stays in local browser storage; external stream requests go directly to their providers.

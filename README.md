# HomeOS 0.2.2 — UK TV Diagnostics

Static GitHub Pages prototype. This is an incremental update to 0.2.1, preserving the seven modules and local browser data.

## New
- Export session diagnostics as JSON: timestamps, playback events, ready/network state, video time, buffered end, error summary and source hostname (not full URL).
- Copy a short diagnostic summary.
- BBC iPlayer, ITVX, Channel 4 and 5 official-service launch links as fallbacks.
- Improved handling of pause events during stream interruptions.

## Deploy
Replace the five root files in your existing GitHub Pages repository (`main` branch, root). Refresh the deployed site. Local browser playlist settings are preserved unless you clear browser storage.

## Test
1. Play Apple HLS demo for 3 minutes.
2. Import the UK playlist and try a channel that previously stalled.
3. When playback stalls, wait for recovery and use Export session diagnostics.
4. Send the JSON file for analysis, preferably after reviewing its contents. The report includes channel name, source host and browser user agent but deliberately excludes the full stream URL.

## Limitations
The app does not provide or unlock restricted streams. Official broadcaster links open external sites. HLS remains native browser playback and is not a substitute for DRM-enabled official players. Browser CORS and streaming-provider permissions remain in force. Automatic recovery does not guarantee successful playback.

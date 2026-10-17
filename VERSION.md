# HomeOS 0.2.1 — IPTV Reliability & Interface Improvements

Released 17 October 2026.

- Preserves the native HTML5 MP4 and Safari HLS playback engine.
- Moves the player above channel browser on narrow screens.
- Adds playback diagnostics (session seconds, recovery count, media status).
- Detects lack of video progress while playing; attempts a maximum of one automatic recovery per selected stream.
- Provides a manual Retry stream control.
- Lets users mark channels Working or Unreliable, and hide unreliable entries.
- Saves user-assigned statuses locally by stream URL.
- Retains M3U import, XMLTV guide, favourites, categories and all other HomeOS modules.

## Limitations

Provider restrictions, DRM, expiring URLs and unavailable streams cannot be repaired by client-side retry. Automatic recovery is best effort; a one-off freeze is not proof of an application defect. Channel statuses are user assessments, not external uptime monitoring. Existing stored playlists are retained in the same browser storage key.

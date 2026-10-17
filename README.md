# HomeOS 0.5.0 Hybrid — consolidated release

## Deploy
Upload all five files to the root of the existing GitHub Pages repository, replacing previous versions. Open `https://kingandcastle.github.io/homeos-prototype/?v=050#dashboard`.

## Scope
- TV player displayed above channel browser on all screen sizes; All/Favourites channel tuner; favourites star does not change the browser filter. Next/Previous and dropdown immediately attempt playback. Safari may require a user gesture; no DRM or provider restrictions are bypassed.
- Entertainment: midnight cinema design, search, service collections, persistent service watchlist, links to legitimate services and local-file playback. These are service shortcuts, not a licensed film catalogue or Plex account sync.
- AI: prompt shortcuts and rule-based local demo. No real OpenAI connection, credentials or voice service.
- Existing dashboard, IPTV diagnostics, playlists, EPG, smart-home demonstration and settings retained.

## Single-pass acceptance checklist
1. Version reads 0.5.0 in header and diagnostics.
2. TV: import playlist; mark a favourite; verify full browser stays visible; switch to Favourites beneath player; use Next/Previous and observe immediate playback attempt.
3. TV: use All group; verify channels can be selected without scrolling; banner disappears.
4. Entertainment: search a service, save it, select Watchlist, refresh and confirm it remains. Open a provider and play a local video.
5. AI: tap a quick prompt, send it, confirm simulated reply and disclaimer.
6. Dashboard and Settings: confirm existing saved data and modules still open.

## Limitations
Browser autoplay with audio is subject to Safari policy. Third-party streams may be unavailable. Entertainment services open externally and may require accounts. Assistant and smart-home controls remain simulations.

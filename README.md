# HomeOS Prototype 0.1.0

A responsive, offline-first browser prototype. Copyright in original contributions is subject to applicable law. **HomeOS is a provisional name, not a cleared trade mark.**

## Run

**Fastest:** unzip the archive and open `index.html` in a modern browser. Most features work from a local file. Some browsers restrict local storage or video when opened with `file://`.

**Recommended local server:** open a terminal in the `homeos-0.1` folder and run:

```bash
python3 -m http.server 8000
```

Open `http://localhost:8000` on that computer. To test on another device on the same trusted Wi-Fi network, use `http://COMPUTER_LAN_IP:8000` if your firewall permits it. Do not expose this development server publicly.

No Node.js, Flutter, build tool or account is needed for the prototype. For production, the UI can later be migrated into a Flutter application or wrapped using an appropriate web/native strategy; this package is **not** a native Android/iOS app.

## Modules and truth-in-functionality

| Module | Working in 0.1 | Simulated / not implemented |
|---|---|---|
| Dashboard | Responsive navigation, live clock, saved household name | Household data metrics |
| IPTV | Local M3U text parsing (up to 500 entries), search, favourites, HTML5 video test, public sample videos | Actual EPG/XMLTV, DRM, HLS support in browsers without native support, channel availability |
| AI | Chat UI, conversation history, rule-based sample responses | Real ChatGPT, OpenAI API, microphone and wake word |
| Entertainment | External website links, local file playback | Native streaming-app integration, casting |
| App Centre | Module shortcuts | APK installation, OS launcher, iOS app installation |
| Smart Home | Interactive simulated switches and scenes | Real device controls, Home Assistant/Matter integration |
| Settings | Theme, household name, JSON export, reset, local persistence | Cloud synchronisation and user accounts |

The demo video URLs are from Google's public sample-video bucket. They require internet and may become unavailable. Importing a playlist does not guarantee playable channels. Browser playback is limited by codec, CORS, mixed-content and provider restrictions. Only access streams you are authorised to use.

## Security and privacy

- Settings, imported playlists and demo conversations are stored in the browser's localStorage.
- Do not paste credentials, private IPTV provider tokens or secrets into this prototype. Exported JSON can contain imported stream URLs.
- No OpenAI API key should ever be embedded in a browser client. A future AI integration needs a secured backend.
- No actual home automation commands are sent.
- App sideloading is Android-specific and requires native OS APIs, consent and careful package validation.

## Acceptance tests

1. Open the page at desktop width and mobile width; navigation and cards must reflow without horizontal page overflow.
2. Switch among all seven modules; each module must render.
3. On Dashboard, observe clock updating; click Watch TV and verify navigation.
4. IPTV: select sample Big Buck Bunny; verify a video element loads and can play with internet access. If blocked, expect an explicit playback error.
5. IPTV: paste `#EXTM3U\n#EXTINF:-1 group-title="Test",Demo\nhttps://storage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4`; import; verify one entry appears. Search `Demo`.
6. IPTV: favourite selected entry; verify star appears; refresh and confirm it persists.
7. AI: submit `How do I use IPTV?`; verify a clearly simulated reply; refresh and confirm conversation persists.
8. Smart Home: toggle a switch; try the Away scene; verify state changes; refresh and verify persistence.
9. Settings: change theme and household name; refresh; verify both persist.
10. Export JSON; verify it contains the saved name/theme. Reset; verify defaults return.
11. Entertainment: select a local video and verify the browser opens its player.
12. Confirm no app promises a real OpenAI response, installed APK, EPG, or physical smart-home action.

## Known limitations

- No backend, database, authentication, native launcher or native mobile build.
- IPTV import supports pasted M3U text, not remote URL fetch, because cross-origin restrictions can prevent browser downloads.
- Only the first 500 playlist entries are parsed; the channel list renders at most 250 search matches to protect low-powered devices.
- HTML5 video may not support HLS/M3U8 in all browsers; production should use platform-specific playback (Media3 on Android, AVPlayer on iOS) or a well-tested web HLS library where suitable.
- Simulated devices are deliberately not connected to real hardware.
- Local video object URLs last only for the current page session.

## Proposed 0.2 priorities

1. Create version-controlled repository and formal requirements/traceability.
2. Choose cross-platform framework based on native media, launcher and app-store constraints.
3. Implement secured backend for OpenAI and user authentication.
4. Implement robust IPTV player, XMLTV guide and error reporting with authorised test streams.
5. Build Android-specific launcher and installer as separately permissioned modules.
6. Add Home Assistant integration with explicit user pairing and safe device-control permissions.
7. Automated tests, accessibility, threat model, licensing review and brand clearance.

## Project files

- `index.html`: layout and responsive styling
- `app.js`: prototype modules, interactions, M3U parser and local state
- `manifest.webmanifest`: web-app metadata
- `README.md`: this document, setup and tests
- `VERSION.md`: release notes

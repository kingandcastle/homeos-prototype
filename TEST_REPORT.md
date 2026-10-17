# HomeOS 0.5.1 — Release Verification

## Static checks
- PASS: JavaScript syntax
- PASS: Unified group filter used by browser
- PASS: Unified group filter used by tuner
- PASS: All channels button present
- PASS: Favourites button present
- PASS: Favourites persisted
- PASS: Previous and Next invoke playback
- PASS: Selected channel attempts autoplay
- PASS: No false stall when recent progress
- PASS: Media cards constrained to portrait ratio
- PASS: Version synchronized

## Environment limitations
Interactive Chromium navigation was blocked by the environment (`ERR_BLOCKED_BY_ADMINISTRATOR`), for both local HTTP and file URLs. Therefore end-to-end browser testing, iPhone Safari rendering, live IPTV playback, and visual layout approval are **not verified**. The checks above are source inspections and syntax checks, not a substitute for browser acceptance tests.

## Known boundaries
- AI remains a simulated offline assistant.
- Entertainment tiles are service shortcuts, not a synchronised Plex catalogue; actual movie poster data requires an authorised provider.
- Browser autoplay, codecs and third-party stream availability cannot be guaranteed.

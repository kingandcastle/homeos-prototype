# HomeOS Prototype 0.2.5

- Unified version constant in app.js, applied to header, settings, diagnostics and exported reports.
- MPEG-DASH detection (.mpd), optional dash.js player loaded from jsDelivr on demand.
- Retains native HLS on Safari and HTML5 video for MP4.
- DASH player errors added to diagnostics; reports include playerEngine.
- No DRM, credential or rights bypass; MSE/codec support and accessible stream required.

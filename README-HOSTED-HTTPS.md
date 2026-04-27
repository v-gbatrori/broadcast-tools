# Broadcast Tools Hosted HTTPS

This package is for static hosting only. No Node server is required.

Upload `index.html` or `broadcast-tools.html` to:

- Netlify drag-and-drop
- Cloudflare Pages
- GitHub Pages

## Recommended workflow

1. Open the hosted HTTPS URL on the laptop.
2. Go to `Latency Meter`.
3. Select `Generator / Master Marker`.
4. Press `QR telefon`.
5. Scan the QR on the phone.
6. The phone opens the same hosted page in `Kamera Analizátor` mode.
7. Press `Kamera indítás`.
8. Point phone at the laptop screen and press `Baseline kalibrálás`.
9. Point phone at the final broadcast monitor.
10. Read `BROADCAST KÉSÉS`.

## Sync modes

### Baseline only
Default. No network/server sync required. This is the most reliable hosted mode.

### Internet sync
Tries `/cdn-cgi/trace` and Cloudflare trace. Best if hosted on Cloudflare Pages or a Cloudflare-proxied domain. If it fails, the app falls back to baseline mode.

### Custom time URL
Optional. Enter a CORS-enabled HTTPS endpoint that returns one of:

```json
{"t": 1730000000000}
```

or Cloudflare-style text with:

```text
ts=1730000000.123
```

## Important

The QR uses an external QR image service:

```text
https://api.qrserver.com/
```

If that service is blocked, copy the displayed phone URL manually.

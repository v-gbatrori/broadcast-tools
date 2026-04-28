Broadcast Tools - SYNQR V5 STABILITY FIX

Changes from V4:
- Baseline only is now the default sync mode for stable local testing.
- Added Page Date sync, using the Cloudflare Worker Date header.
- Public Internet Auto sync no longer displays huge uncertainty if it is unstable.
- Stale audio values are ignored after a few seconds.
- Audio must have at least 2 fresh samples before AV OFFSET is displayed.
- Session Runner shows VIDEO OK when video has enough samples but audio is weak.

Recommended:
1. Session Runner -> Create Session.
2. Open Generator -> Upload ON.
3. For video-only test keep Audio off.
4. For AV test turn Audio click ON and keep laptop volume loud.
5. Phone -> Start camera.
6. If audio is weak, trust VIDEO first; then improve audio separately.

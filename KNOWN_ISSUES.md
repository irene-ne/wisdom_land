# Known Issues — Wisdom Land Animal World MVP

## Current limitations

1. **Local server required for development.**  
   The app uses ES modules. Opening `index.html` directly via `file://` may be blocked by browser CORS/module restrictions. Use any static HTTP server (e.g., `python -m http.server`) or deploy to GitHub Pages.

2. **Audio not audibly verified in this pass.**  
   Audio file paths resolve correctly and the playback API is wired, but clips were not individually listened to during QA.

3. **Real-device testing recommended.**  
   Layouts are designed for iPad landscape and desktop browsers. Touch targets and animations should be validated on the target devices before a public launch.

4. **No automated unit test suite.**  
   Verification was performed through visual QA, route smoke tests, and a programmatic progression test. A future iteration may add a lightweight test runner if Node.js becomes available in the build environment.

5. **Progress is stored per origin.**  
   `localStorage` is tied to the domain/path where the app is hosted. Progress will not transfer between `localhost`, a GitHub Pages URL, and any other deployment.

## Resolved before release

- `DataAdapter.getZones()` now includes `chapters`, restoring hub progress dots and correct sequential unlocks.
- Router regex replacement order fixed so parameterized routes capture correctly.
- Bonus Discovery direct-URL guard added to prevent skipping locked content.
- Reward engine zone-star calculation fixed to iterate over chapter objects.

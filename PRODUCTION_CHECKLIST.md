# Production Checklist — Wisdom Land Animal World MVP

## Release package

- [x] Folder named `wisdom-land-v0.1.0-animal-world-mvp/`.
- [x] Top-level `index.html` present and references only relative paths.
- [x] `data/animal-world.json` present and uses relative asset paths.
- [x] `assets/` includes `animals/`, `backgrounds/`, and `audio/`.
- [x] `src/` includes app shell, screens, components, game engines, and shared utilities.

## Cleanup

- [x] Removed development-only pages (`tests/game-lab.html`, `phase3-progression-test.html`, `test-result.html`).
- [x] Removed temporary scripts (`generate_images.py`).
- [x] Removed source content spreadsheet (`content/animal-world.xlsx`).
- [x] Removed design artifacts, prototypes, and version-history folders (`Asset/`, `Ver 1/`, `Discovery Kingdom Prototype.docx`, ChatGPT images).
- [x] Removed hidden development panel (`dev-panel.js`, `dev-panel.css`) and all references in `main.js`, `app-header.js`, and screen files.
- [x] No absolute `file://` or `http://localhost` references in runtime code.

## Path & hosting compatibility

- [x] All module and asset paths use `./` relative references from `index.html`.
- [x] Router uses hash fragments (`#/route`) for refresh-safe static hosting.
- [x] No `<base href>` or root-absolute paths (`/assets/...`, `/src/...`).
- [x] Works from GitHub Pages root or a subfolder without server rewrites.

## Asset & code integrity

- [x] 60 animal folders present, each with `hero.webp`, `transparent.webp`, `silhouette.webp`.
- [x] 6 zone background images present.
- [x] 120 audio files present.
- [x] Bracket/brace balance check passed for all JS and CSS files.
- [x] No `console.log` debug statements remain in runtime code.
- [x] No `debugger` statements remain.

## Documentation

- [x] `README.md` with quick start, deployment, routing, and content-editing instructions.
- [x] `CHANGELOG.md` summarizing v0.1.0 scope.
- [x] `RELEASE_NOTES.md` with deployment steps and verification status.
- [x] `PRODUCTION_CHECKLIST.md` (this file).
- [x] `KNOWN_ISSUES.md` with current limitations.

## Final QA status

- [x] Home route renders.
- [x] Discovery Kingdom route renders.
- [x] Animal World hub renders with zone cards and progress dots.
- [x] Zone screen renders chapter grid.
- [x] Chapter discovery route renders animal cards.
- [x] Locked Bonus Discovery route shows locked state when not unlocked.
- [x] Sequential progression unlocks next chapter, Bonus, and next zone correctly.
- [x] Star totals update and deduplicate on replay.
- [x] Sound toggle propagates.
- [x] Browser refresh returns to the same hash route.

## Result

**Ready for GitHub Pages deployment.**

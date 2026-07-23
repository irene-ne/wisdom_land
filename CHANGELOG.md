# Changelog

## [0.1.0] — 2026-07-24

### Added — Animal World MVP

- Home screen and Discovery Kingdom world picker.
- Animal World hub with six zone cards and progress dots.
- Zone screen with chapter grid and Bonus Discovery reveal.
- Chapter flow: Discover → Play → Complete.
- Bonus Discovery flow with lock guard before Chapter 3 is finished.
- Seven reusable mini-game engines:
  - Who Am I?
  - Memory Match
  - Silhouette
  - Jigsaw Puzzle
  - Odd One Out
  - Sort Them
  - Word Scramble
- Centralized `RewardEngine` awarding stars once per stable achievement ID.
- Sequential progression: chapters unlock in order; Bonus unlocks after Chapter 3; next zone unlocks after Bonus.
- Practice Mode replays without duplicate rewards.
- `ProgressStore` with `localStorage` persistence, schema version `1.0.0`, and automatic migration.
- Global sound toggle propagated to all game engines.
- Lazy image loading with SVG placeholder fallback.
- Hash-based router for static-host compatibility.
- 60 animals across 6 zones, 24 chapters, 120 audio clips, 186 images.

### Production readiness

- Removed development-only pages, scripts, and temporary QA artifacts from the release package.
- Removed hidden development panel and its CSS from production build.
- Verified all asset and module paths are relative and GitHub Pages subfolder-safe.
- Verified bracket balance across all 46 JS and 17 CSS files.
- Generated release archive `wisdom-land-v0.1.0-animal-world-mvp.zip`.

# Release Notes — Wisdom Land Animal World MVP

**Version:** 0.1.0  
**Date:** 2026-07-24  
**Status:** Ready for GitHub Pages deployment

## Overview

This release delivers the first playable world of Wisdom Land: **Animal World**. It is a fully static, frontend-only experience built with plain HTML/CSS/JS ES modules and is intended to be published directly to GitHub Pages without further development.

## Included content

- 6 zones: Wild Lands, Farm Life, Desert Adventure, Bird Paradise, Coral Reef, Polar World
- 24 chapters (4 per zone: Chapters 1–3 + Bonus Discovery)
- 60 animals with hero, transparent, and silhouette images
- 120 audio files (pronunciation + narration for every animal)
- 7 reusable mini-games

## What's ready

- Hash-based routing works from root or any GitHub Pages subfolder.
- All paths are relative; no server rewrite is required.
- Refresh-safe: reloading `#/chapter/wild-lands/1` returns to the same route.
- Sequential progression and star rewards verified.
- Practice Mode prevents duplicate rewards on replay.
- Sound preference and progress persist in `localStorage`.

## Deployment

1. Unzip `wisdom-land-v0.1.0-animal-world-mvp.zip`.
2. Upload the folder contents to your GitHub Pages branch (root or `/docs`).
3. Enable Pages from that branch/folder.
4. Share the URL.

## Not in scope

- User accounts or backend
- Additional worlds (Nature, Weather, Space, etc.)
- Coins, badges, timers, or leaderboards
- Further image/audio generation

## Verification

- Bracket-balance sanity check: **PASS** (46 JS, 17 CSS).
- Route smoke test: **PASS** (home, hub, zone, chapter, locked bonus).
- Progression test: **PASS** (sequential unlocks, star totals, no duplicate rewards).

See `PRODUCTION_CHECKLIST.md` and `KNOWN_ISSUES.md` for details.

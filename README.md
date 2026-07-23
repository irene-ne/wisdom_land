# Wisdom Land — Animal World

A frontend-only, child-friendly animal discovery web app. This package is the **Animal World MVP (v0.1.0)**: six zones, four chapters per zone, a Bonus Discovery surprise, seven reusable mini-games, and a star-based progression system. It is ready to publish on GitHub Pages or any static HTTP host.

## What's inside

- `index.html` — single entry point with hash-based routing.
- `data/animal-world.json` — zones, chapters, animals, asset paths, and facts.
- `assets/` — animal images (`hero`, `transparent`, `silhouette`), zone backgrounds, and audio clips.
- `src/` — plain ES modules: app shell, screens, components, game engines, and shared utilities.
- `CHANGELOG.md`, `RELEASE_NOTES.md`, `PRODUCTION_CHECKLIST.md`, `KNOWN_ISSUES.md`.

## Version

**v0.1.0 — Animal World MVP**

## Quick start (local)

Because the app uses ES modules, open it through a local HTTP server rather than double-clicking `index.html`.

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000/`.

## GitHub Pages deployment

1. Copy the contents of `wisdom-land-v0.1.0-animal-world-mvp/` to the root (or a subfolder) of your Pages branch.
2. Enable GitHub Pages from that branch/folder.
3. Visit `https://<username>.github.io/<repo>/` or `https://<username>.github.io/<repo>/<subfolder>/`.

All asset and module paths are relative, and routing uses hash fragments (`#/animal-world`, `#/chapter/wild-lands/1`, etc.), so no `404.html` or server rewrite is needed. Refreshing any route lands back on the same screen.

## Navigation

| Route | Screen |
|-------|--------|
| `#/` | Wisdom Land home |
| `#/discovery-kingdom` | Discovery Kingdom world picker |
| `#/animal-world` | Animal World hub (zone cards) |
| `#/zone/:zoneId` | Zone chapter grid |
| `#/chapter/:zoneId/:chapterId` | Chapter flow: Discover → Play → Complete |
| `#/bonus/:zoneId` | Bonus Discovery flow |

## Chapter flow

1. **Let's Discover!** — Flip animal cards, hear pronunciations and narration, and read fun facts. First discovery of each animal awards **1 star**.
2. **Let's Play!** — Play a random playlist of 3–4 mini-games built from the chapter animals. Completing each unique game in the chapter awards **1 star**.
3. **Chapter Complete!** — Awards **2 stars** the first time through and unlocks the next chapter, the Bonus Discovery, or the next zone.

Bonus Discovery follows the same Discover → Play pattern, awards **3 stars**, and unlocks the next zone when completed.

## Progress persistence

Progress is saved in the browser under the `localStorage` key `wisdomLand_progress`.

Stored data includes:

- Total stars
- Sound on/off preference
- Discovered animals
- Completed activities, chapters, and zones
- Unlocked chapters and zones

The app migrates saved data to the current schema on load and always ensures Wild Lands Chapter 1 is unlocked.

## Content editing

To change animals, chapters, or zones:

1. Edit `data/animal-world.json`.
2. Add or replace images under `assets/animals/{id}/` (`hero.webp`, `transparent.webp`, `silhouette.webp`).
3. Add or replace audio under `assets/audio/{id}-pronunciation.mp3` and `{id}-narration.mp3`.
4. Add or replace zone backgrounds under `assets/backgrounds/{zoneId}.webp`.
5. Refresh the browser.

No app code needs to change unless the data shape changes.

## Browser support

Targets modern browsers with ES module and pointer event support. Designed for iPad landscape Safari and desktop Chrome/Edge.

## License / attribution

Built for internal Wisdom Land project use. Animal facts reference sources listed in `data/animal-world.json`.

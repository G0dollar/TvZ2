# Turret vs Zombies

Turret vs Zombies is a browser-based arcade defense game. Move a turret across the lanes, shoot incoming zombies, survive increasingly difficult waves, and spend collected resources on upgrades. The game includes Standard Battle, class raids, an endless mode, and persistent progression.

## Play

There is no build step, package manifest, or dependency installation. From the project root, start Python's static file server:

```powershell
py -m http.server 8000
```

If the Windows Python launcher (`py`) is unavailable, use `python -m http.server 8000` if Python is on your `PATH`. Then open <http://localhost:8000/TvZ2.html>. Alternatively, open the project in VS Code and use a static-file server extension such as Live Server.

> The page imports its Rajdhani and Share Tech Mono fonts from Google Fonts, so an internet connection is needed to load those fonts. The game code and gameplay assets are otherwise local.

## Controls

| Action | Keyboard | On-screen controls |
| --- | --- | --- |
| Move left / right | `←` / `A`, `→` / `D` | Arrow buttons |
| Shoot | `Space` / `Enter` | **FIRE** button |
| Reload | `R` | Reload button |
| Switch utility | `Q` | Utility button |
| Deploy utility | `E` | Deploy button |
| Open weapon shop | `B` / `P` | Use the in-game menu |

Touch controls are available on mobile devices. The input mode can also be changed in Settings.

## Progress and settings

Game progress is saved in this browser's `localStorage`; it is not synced between browsers or devices. Audio preferences and the selected controls mode are currently kept in memory only and reset when the page reloads. Use **Wipe All Save Data** in Settings to reset saved game progress.

## Project structure

```text
TvZ2.html           Game markup, embedded styles, and script loading
README.md           Project overview and setup instructions
.gitignore          Ignore rules for OS files, logs, and editor metadata
.vscode/
  launch.json       Empty placeholder; no VS Code launch configuration yet
js/
  config.js         Grid, gameplay constants, and upgrade/class configuration
  audio.js          Web Audio sound effects and music
  particles.js      Canvas particle effects
  game.js           Game state, UI, controls, persistence, and gameplay loop
```

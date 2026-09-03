# Shooter Game Hub 🎯

A standalone, self-contained collection of **7 shooting games** — extracted from the
larger Game Hub and packaged as a single HTML file. No build tools, no server, no
dependencies. Just open `index.html` and play.

## Games

| # | Game | Type | Controls |
|---|------|------|----------|
| 1 | **FPS Arena** | First-person raycasted shooter | WASD move, mouse/click/space shoot, R reload |
| 2 | **Archer Duel** | Aim-and-shoot archery | Mouse aim, click to shoot arrows (mind the wind) |
| 3 | **Arena Battle** | Top-down 1v1 projectile duel | P1: WASD + F · P2: arrows + Enter · dash: Space/Shift |
| 4 | **Bowmasters** | Drag-to-aim projectile duel | Drag to aim/power, release to shoot; character select |
| 5 | **Zombie Survival: Horde** | Top-down survival roguelite | WASD/arrows move, Space dash; weapons auto-fire |
| 6 | **Asteroids** | Classic space shooter | A/D rotate, W thrust, Space fire |
| 7 | **Target Practice** | Click-the-target accuracy test | Click moving targets, 30-second timer |

## Play

Open `index.html` in any modern browser. That's it — all games, art, audio, and
logic are embedded in the one file.

```bash
# optionally serve it locally
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Repository contents

```
index.html   # the entire game hub (7 games + shared UI/CSS)
README.md    # this file
```

## Notes

- This build contains **only** the shooting-type games. Puzzle, racing, idle, and
  other non-shooting games from the original Game Hub were removed to keep the
  collection focused.
- A pre-existing crash in Zombie Survival (the render loop running one frame before
  the player object exists) has been patched with a null guard in `draw()`.
- The Zombie Survival main-menu overlay was nudged down so it no longer clips the
  page title.
- Developer/admin backdoor code from the original file was removed as dead code.

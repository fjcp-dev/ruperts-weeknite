# Rupert's Weeknite!

A 100-player battle royale FPS that runs in the browser — built for (and with) Rupert,
age 9. Playable on iPad, iPhone and Mac. No install, no server: one self-contained
`index.html` plus Three.js from a CDN.

## Play

**GitHub Pages:** https://fjcp-dev.github.io/ruperts-weeknite/

- **iPad / iPhone:** open in Safari, Share → Add to Home Screen for fullscreen play.
  Left thumb moves, right thumb aims, big FIRE button shoots. Tap the weapon readout
  (bottom-left) to cycle weapons.
- **Mac:** click to lock the mouse. WASD move, Shift sprint, Space jump, 1–5 to switch
  weapons, click to shoot.

## How it plays

- Every match: you + 99 named bots skydive onto the island from 100 m, gliders pop at 40 m
- Bots brawl each other all over the map (watch the kill feed); one hunts you, with a leash
- Golden loot chests fire rarity-coloured beams into the sky; walk up and the lid swings
  open, step on to collect the weapon (Pistol → SMG → Assault Rifle → Shotgun → Sniper)
- Four health bars: three blue shield bars drain first, then green health
- Each kill heals half a bar; last one standing gets the VICTORY ROYALE screen

## Development

The whole game lives in `index.html` (game code inline, no build step). Open it via any
static server, e.g. `python3 -m http.server 8000` from the repo root.

- The version shown on the in-game menu follows [semver](https://semver.org/): patch for
  balance tweaks and fixes, minor for features, major for reworks
- `tmp/repro.js` (untracked) headlessly boots the game in Node with Three.js stubbed to
  smoke-test spawn logic and game state

## Repo history

Lives in git since v1.18.0; earlier history (it began as a subdirectory of
[wall-climber](https://github.com/fjcp-dev/wall-climber)) is in that repo's log.

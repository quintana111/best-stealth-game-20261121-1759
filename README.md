# The Brass Ledger

[![best-stealth-game-20261121-1759](https://make.fun/badge/best-stealth-game-20261121-1759.svg)](https://make.fun/bounty/best-stealth-game-20261121-1759)
[![rank](https://make.fun/badge/best-stealth-game-20261121-1759/quintana111/best-stealth-game-20261121-1759/rank.svg)](https://make.fun/bounty/best-stealth-game-20261121-1759)
[![reward](https://make.fun/badge/best-stealth-game-20261121-1759/quintana111/best-stealth-game-20261121-1759/reward.svg)](https://make.fun/bounty/best-stealth-game-20261121-1759)

A top-down stealth game: a night archivist slips into the Clockmaker's
Archive to steal the Brass Ledger, then reaches the green EXIT unseen.
Three guards patrol with large gold vision cones; crates block sight,
hatched shadow zones hide you, lamplight exposes you from across the room.
Throw coins to distract guards, sneak with SHIFT, spend one smoke bomb
with Q. One polished level, 1280×720, no network requests, WebAudio beeps
only.

## Run

```sh
# Play locally
node serve.ts
# then open http://localhost:8080

# Hand the entry in (writes /output/dossier.json)
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
```

## Files

- `game/index.html` — the whole game (inline CSS + JS, static, offline)
- `main.ts` — Node 22, stdlib only; copies `game/` and `screenshots/` to
  `/output` and writes `/output/dossier.json` with the vendored make.fun
  library
- `vendor/makefun-game.ts` — the kit's library, unchanged
- `screenshots/` — 4 shots of the game (start, suspicious, hidden, exit)
- `shots.json` — the `?shot=` states behind the screenshots

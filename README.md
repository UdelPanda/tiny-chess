# tiny-chess

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/UdelPanda/tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/UdelPanda/tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in 4 KB of Python — v11 is 3,436 bytes, built for make.fun's tiny-chess-01 bounty. Practice Elo ~1,514 mean across 3 trials (best trial 1,545), above the 1,154 floor for the final. An 80,000-node budget per move (never a clock, so replays are deterministic). PVS with check extensions, transposition table, killer moves, history heuristic, null-move pruning, late-move reductions, draw contempt, quiescence over captures (and all replies to check, with a mate fix), PeSTO-style tapered middlegame/endgame evaluation with a bishop-pair bonus. It talks to the env alone (`POST /game`, `/move`) and makes no model calls.

## Run it

```sh
python3 test.py perft   # move generation vs python-chess
python3 build.py        # repack main_src.py into main.py
```

MIT — see `LICENSE`.

---

<sub>Entered on [make.fun](https://make.fun/?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>

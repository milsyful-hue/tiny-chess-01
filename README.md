# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/milsyful-hue/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/milsyful-hue/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A from-scratch chess engine in 4 KB of Python, built by an AI agent for make.fun's "Build the strongest chess engine in 4 KB of Python" bounty ($500 in USDC).

## How it plays

`main.py` talks to the env at `MAKEFUN_ENV_URL` (`POST /game`, `/move`) and picks each move with a negamax alpha-beta search: iterative deepening to a fixed budget of 60,000 nodes a move, quiescence over captures and promotions (and all replies to check), MVV-LVA + transposition-table move ordering, and a piece-square evaluation. No clock, no randomness, so replays play the same moves.

`main.py` is the engine, packed by the kit's `makefun compress` command; the readable source is archived with the build, outside this repository.

## Run it

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:8080 python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=kgkgd9xs&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>

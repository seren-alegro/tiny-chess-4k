# Tiny Chess — 4 KB Python chess engine

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/seren-alegro/tiny-chess-4k/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/seren-alegro/tiny-chess-4k/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

An original chess engine in 4,075 bytes of Python 3 (standard library only),
built for the make.fun bounty [Build the strongest chess engine in 4 KB of Python](https://make.fun/bounty/tiny-chess-01).

`main.py` is the whole engine: it plays the gauntlet through the env at
`MAKEFUN_ENV_URL` (POST /game, POST /move, UCI moves). Fixed 42,000-node
budget, no clock, no randomness — the same position always gets the same move.

Design: 0x88 board, negamax alpha-beta with PVS, quiescence, transposition
table, null-move pruning and LMR; formulaic material + piece-square evaluation.

## Run it

```sh
MAKEFUN_ENV_URL=<env url> python3 main.py
```

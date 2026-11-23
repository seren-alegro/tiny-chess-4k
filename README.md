# Tiny Chess — 4 KB Python chess engine

An original chess engine in 4,075 bytes of Python 3 (standard library only),
built for the make.fun bounty "Build the strongest chess engine in 4 KB of Python".

`main.py` is the whole engine: it plays the gauntlet through the env at
`MAKEFUN_ENV_URL` (POST /game, POST /move, UCI moves). Fixed 42,000-node
budget, no clock, no randomness — the same position always gets the same move.

Design: 0x88 board, negamax alpha-beta with PVS, quiescence, transposition
table, null-move pruning and LMR; formulaic material + piece-square evaluation.

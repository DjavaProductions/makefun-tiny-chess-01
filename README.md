# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/DjavaProductions/makefun-tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/DjavaProductions/makefun-tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in at most 4,096 bytes of Python, written for the
make.fun bounty "Build the strongest chess engine in 4 KB of Python".

`main.py` is the whole engine: a 0x88-board negamax search with
alpha-beta pruning, quiescence search, MVV-LVA move ordering and
iterative deepening under a fixed node budget (deterministic — no
clock, no randomness). It talks to the make.fun env over HTTP and
answers in UCI.

`main.py` is a packed entrypoint produced by `makefun compress` from
the readable source `source.py` (kept beside it, uncommitted); the
packed bytes and the source are linked in the submission bundle.

## Build

    node <kit>/cli/makefun.mjs compress source.py --out main.py

## Grade locally

    node <kit>/cli/makefun.mjs grade-local --kit <kit> --bot . --driver docker

## License

MIT, see LICENSE.

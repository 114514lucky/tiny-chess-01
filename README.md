# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/114514lucky/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/114514lucky/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

Strongest chess engine in 4 KB of Python: 0x88-board negamax
alpha-beta with a transposition table, MVV-LVA + killer move ordering,
quiescence search, piece-square evaluation and a king-safety term
(pawn shield, only while queens are on the board). Fixed node budget
per move (350,000 nodes, max depth 6) with an 8-second wall-clock
guard that falls back to the last completed depth; no unseeded
randomness. Practice trials averaged ~1,365 Elo, and the Berlin line
as Black is a win (checkmate in 96 plies). v7 refactored repetition
avoidance and the search/eval internals; aggressive LMR, futility
and rook terms were A/B-tested and reverted.

## Run it

```sh
MAKEFUN_ENV_URL=<env-url> python3 main.py
```

`main.py` (Python 3.13, standard library only) is the compressed form
of the readable source and talks to the game environment at
`$MAKEFUN_ENV_URL`; it does not run standalone without the kit env
server.

---

<sub>Entered on [make.fun](https://make.fun/?ref=d5a50dzy&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>

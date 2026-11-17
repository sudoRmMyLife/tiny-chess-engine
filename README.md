# tiny-chess-engine

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/sudoRmMyLife/tiny-chess-engine/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/sudoRmMyLife/tiny-chess-engine/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in 4 KB of Python: negamax search with alpha-beta pruning, principal-variation search and late move reductions, a transposition table with mate-score adjustment, check extensions, and quiescence (captures and promotions, with delta pruning) folded into a single recursive search. Evaluation is material plus piece-square tables with separate middlegame/endgame king tables, maintained incrementally alongside Zobrist hashing, repetition and fifty-move detection. The readable source is minified and packed with LZMA + base85 (Python standard library only) to fit the 4,096-byte cap; main.py unpacks and runs it. It plays through the make.fun env at MAKEFUN_ENV_URL and searches to a fixed node budget, never a clock, so every game replays move for move.

## Run it

```sh
MAKEFUN_ENV_URL=http://localhost:8080 python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=2tnm35pq&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>

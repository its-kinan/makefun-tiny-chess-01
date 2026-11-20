# makefun-tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/its-kinan/makefun-tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/its-kinan/makefun-tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in 4,096 bytes of Python (MIT). `main.py` is a compressed (LZMA) payload of the readable source: a 0x88-board negamax engine with alpha-beta, iterative deepening to a fixed 40,000-node budget, quiescence search, transposition table, null-move pruning, late-move reductions, killers + history, MVV-LVA ordering, and a tapered piece-square eval with pawn structure. No clock, no randomness — the same position always gets the same move. Practice trials against the sealed env and scorer: mean Elo 1364 across three trials, vs the sunfish baseline's 1365.

## Run it

```sh
makefun grade-local --kit . --bot <your repository> --driver docker
```

The grader runs the entry as `python3 -P -s main.py`; it plays through the make.fun env. Local grading needs Docker and the kit CLI.

---

<sub>Entered on [make.fun](https://make.fun/?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>

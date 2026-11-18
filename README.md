# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/androyesfernandez/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/androyesfernandez/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A complete chess engine in 4,080 bytes of Python (standard library only). `main.py` is the whole engine: a one-line lzma+base85 unpacker around an 8.2 KB engine with a 0x88 board, full legal move generation (perft-exact), incremental material + piece-square evaluation with a middlegame-to-endgame king blend, and negamax alpha-beta search with iterative deepening under a fixed 65,000-node budget (never a clock, so replays are identical), PVS, a transposition table, capture quiescence with check evasions, null-move pruning, LMR, check extensions, and MVV-LVA + killer move ordering. Measured on the kit's own practice ladder: about 1,425 Elo, above the 1,154 gate for the live gauntlet. It plays through the competition env at `MAKEFUN_ENV_URL`.

## Run it

```sh
MAKEFUN_ENV_URL=<env-url> python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=ktpzxevq&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>

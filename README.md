[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/Bungsuu11jore7/tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/Bungsuu11jore7/tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

# Tiny Chess Engine in 4 KB of Python

A chess engine in 4,094 bytes of Python (0x88 board, alpha-beta +
transposition table + killer moves + quiescence + late-move reductions,
N=200k node budget, deterministic, stdlib only).

`main.py` is the entry: lzma preset 9 + base85 packed source with a
two-line unpacker (line 1 imports lzma/base64, line 2 execs the
payload). Verified: perft 12/12, Zobrist round-trip,
determinism (same position, same move, twice).
Practice Elo 1669 (trial-0, 6W/0D/2L), submitted as v10a-n200.

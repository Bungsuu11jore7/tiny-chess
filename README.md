# Tiny Chess Engine in 4 KB of Python

A chess engine in 4,094 bytes of Python (0x88 board, alpha-beta +
transposition table + killer moves + quiescence + late-move reductions,
N=200k node budget, deterministic, stdlib only).

`main.py` is the entry: lzma preset 9 + base85 packed source with a
two-line unpacker (line 1 imports lzma/base64, line 2 execs the
payload). Verified: perft 12/12, Zobrist round-trip,
determinism (same position, same move, twice).
Practice Elo 1669 (trial-0, 6W/0D/2L), submitted as v10a-n200.

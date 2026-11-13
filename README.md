# Tiny Chess Engine in 4 KB of Python

A chess engine in 4,069 bytes of Python (0x88 board, alpha-beta +
transposition table + killer moves + quiescence + late-move reductions,
fixed 40,000-node budget, deterministic, stdlib only).

`main.py` is the entry: lzma preset 9 + base85 packed source with a
two-line unpacker (line 1 imports lzma/base64, line 2 execs the
payload). Verified: perft 12/12, Zobrist round-trip,
determinism (same position, same move, 40,001 nodes, twice).
Practice Elo ~871 (below the 1,154 final floor), submitted as-is.

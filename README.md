[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/lx191765461-eng/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/lx191765461-eng/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

# tiny-chess-01 entry

An original chess engine in a single Python file (standard library only).
main.py is the engine packed with make.fun's compress tool — an LZMA
stream of the readable source inside a small stub: 3,944 bytes total.

The engine: full legal move generation (castling, en passant, promotions),
negamax alpha-beta with PVS, LMR and null-move pruning, quiescence search
(captures, promotions, check evasions) with delta pruning, check
extensions, a transposition table, MVV-LVA / TT-move / killer ordering,
in-search and game-history repetition handling, and material plus
piece-square evaluation with a bishop-pair term. Iterative deepening runs
under a fixed node cap per move (150,000 nodes before ply 80, 80,000
after) — no clock anywhere, so play is fully deterministic and replays
move for move.

License: MIT (see LICENSE).

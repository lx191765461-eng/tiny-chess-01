# tiny-chess-01 entry

An original chess engine in a single Python file (standard library only).
main.py carries the engine as an lzma payload stored in a latin-1 string
literal (see the coding line) with a two-line unpacker: 3,987 bytes total.

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

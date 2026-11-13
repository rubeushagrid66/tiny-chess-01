# tiny-chess-01

A compact chess engine in 4 KB of Python, built from scratch for the
make.fun "strongest chess engine in 4 KB" bounty.

Engine: alpha-beta negamax with iterative deepening under a fixed node
budget, quiescence search, transposition table with seeded Zobrist hashing,
MVV-LVA + killer move ordering, and a tapered piece-square-table evaluation
on a 0x88 board. Deterministic: no clock, no unseeded randomness.

`main.py` is a compressed build of the clear source in `dev/engine.py`.
Run it as `python3 -P -s main.py` with `MAKEFUN_ENV_URL` set to the
environment endpoint. `CHESS_NODES` overrides the per-move node budget
(default 60000).

License: MIT.

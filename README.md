# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/muherilobak-web/tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/muherilobak-web/tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A from-scratch 0x88 chess engine in 4 KB of Python. `main.py` is the whole
engine (3,956 bytes as committed): alpha-beta + quiescence, transposition
table, killers, history, null-move pruning, LMR, tapered midgame/endgame
evaluation with pawn structure, and repetition contempt that plays the
tournament, not just the position. Fixed node budget per move (35k/25k/20k
by ply), never a clock, fully deterministic.

Practice (local, 3 trials vs the house gauntlet, 35k nodes/move):
trial-0 Elo 1,451, trial-1 Elo 1,279, trial-2 Elo 1,654 — mean 1,461.
Deterministic: trial-0 replayed move-for-move identical. No timeouts in
18 games at the 35k budget (a 60k budget timed out once under CPU load).

Built by [Doc](https://make.fun/r/bt57jd3y) for
[@muheri-lobak](https://make.fun/u/muheri-lobak) on
[make.fun](https://make.fun/r/bt57jd3y).

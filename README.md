# tiny-chess-01 entry

A chess engine in one Python file (at most 4,096 bytes) for the make.fun
tiny-chess-01 bounty. Negamax alpha-beta search with quiescence, a small
transposition table and a fixed node budget (no clock, so replays match),
material plus compact positional terms. It plays the whole gauntlet
through the env at MAKEFUN_ENV_URL and exits when every game is over.

MIT licensed, see LICENSE.

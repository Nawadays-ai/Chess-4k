# tiny-chess-01 entry

A chess engine in one Python file (at most 4,096 bytes) for the make.fun
tiny-chess-01 bounty. Iteration 5: the iteration-2 recipe re-implemented
on a mailbox board (list of 64 ints) with an incremental Zobrist hash
keying the transposition table and the repetition tables, the legality
test inside the search loop, and the transposition table cleared at the
start of each game — about 1.65x the nodes per second of the previous
entry. Negamax alpha-beta search with quiescence (captures, promotions
and check evasions), check extensions, MVV-LVA move ordering, and the
root single-legal-move shortcut; evaluation is material plus full
piece-square tables and the bishop pair, and repetitions and the
fifty-move rule score as draws inside the search. A fixed node budget
of 28,000 per move (no clock) keeps replays deterministic; a per-game
budget cap was measured to cost points on the practice gauntlet and is
not used. Practice score: 10.0/18 (Elo 1545 / 1191 / 1279 across the
three trials) against 9.5/18 for the iteration-2 entry.
The file is a two-line stub that unpacks (lzma + base85) and runs the
engine source, so the entry stays plain ASCII text.
It plays the whole gauntlet through the env at MAKEFUN_ENV_URL and
exits when every game is over.

MIT licensed, see LICENSE.

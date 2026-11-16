# Tiny chess baseline

Experimental Python 3.13 engine for tiny-chess-01. Standard library only;
embedded LZMA source, 0x88 legal moves, alpha-beta, transposition cache
and quiescence. Fixed cap: 20,000 nodes, depth 8. No model calls.

Run: python main.py with MAKEFUN_ENV_URL set to the local competition env.

Development source, tests and builder are outside this entry tree.
No official Elo, sandbox timing or submission acceptance is claimed.
This README is provisional; platform badges/About and transcript preflight
must be completed before any future submission.
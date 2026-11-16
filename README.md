# tiny-chess-01

[![make.fun tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/davenETH69/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/davenETH69/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A deterministic chess engine in 3,870 bytes of Python 3.13 for the
[Build the strongest chess engine in 4 KB of Python bounty](https://make.fun/bounty/tiny-chess-01).
Standard library only, with embedded LZMA source, a 0x88 board, legal move
generation, alpha-beta, iterative deepening, tactical move ordering,
quiescence, repetition and insufficient-material handling, killer moves,
and material, centralization, bishop-pair and king-safety evaluation.
Search stops at 20,000 nodes or depth 8; it never uses a clock or calls a model.

## Run it

Set MAKEFUN_ENV_URL to the competition environment, then run:

```sh
python3 main.py
```

The engine uses the environment's JSON HTTP /game and /move protocol, with UCI
moves. It exits when all games finish. It does not implement a UCI stdin server.

## Local validation

The official kit's Docker grade on practice trial 0 scored 1,451: four wins,
two losses. Both live and replay finished under 1 CPU, 512 MiB and 64 PIDs,
with identical canonical state hashes and zero model calls. This is a local
practice result, not a server submission score or a guarantee on final openings.
The local harness used Node v22.23.4 versus kit server metadata v26.13.1;
the kit-pinned Python and scorer images were used unchanged.

main.py is packed using makefun compress. Its readable source is provided
beside the original coding-session transcripts in the submission bundle,
outside this size-limited entry tree. Preserve main.py's Latin-1 encoding
and exact bytes. Development fixtures and tools are not engine dependencies.

## Verify the engine

SHA-256 of the tested main.py:
`183825e256824a5c6b452b493a647659ee98f17f64356bf3c376f30fe2853f3b`.
Use `sha256sum main.py` on Linux, or `Get-FileHash main.py -Algorithm SHA256`
in PowerShell. A matching hash identifies the exact engine used in the local
Docker live/replay test; README and ownership metadata do not affect its search.

---

Built with an AI coding agent for [make.fun](https://make.fun/?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01), where AI agents build software for cash rewards.
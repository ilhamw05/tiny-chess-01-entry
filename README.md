# tiny-chess-01-entry

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/ilhamw05/tiny-chess-01-entry/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/ilhamw05/tiny-chess-01-entry/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in at most 4,096 bytes of Python (main.py is 3,385 bytes, an lzma-packed single file, standard library only). It plays the whole gauntlet through the competition env: fixed node budgets, no clock, fully deterministic.

## Credit

This is a fork of **Sunfish** by Thomas Ahle and contributors (https://github.com/thomasahle/sunfish), built from `nnue_4k/pst_entry.py` at commit e396948acbd80cdcbad3dccfb07e878fba9df8f4, licensed GPL-3.0-only. Changes from upstream: the UCI loop and clock are replaced with a driver for this competition's env (POST /game, POST /move), and the fixed 50,000-node budget is replaced with a deterministic schedule — 70,000 nodes in the endgame (12 or fewer pieces, where nodes are cheapest) and 49,000 nodes everywhere else.

## Run it

```sh
MAKEFUN_ENV_URL=<env origin> MAKEFUN_PROMPT_FILE=/input/prompt.txt MAKEFUN_TRIAL_SEED=<seed> python3 main.py
```

---

<sub>Built for the [make.fun tiny-chess-01 bounty](https://make.fun/bounty/tiny-chess-01) by an AI agent.</sub>

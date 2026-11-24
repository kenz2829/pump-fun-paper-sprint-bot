# pump-fun-paper-sprint-bot

[![make.fun · u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b](https://make.fun/badge/u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b.svg)](https://make.fun/bounty/u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b?utm_source=github&utm_medium=readme&utm_campaign=u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b)
[![rank](https://make.fun/badge/u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b/kenz2829/pump-fun-paper-sprint-bot/rank.svg)](https://make.fun/bounty/u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b)
[![reward](https://make.fun/badge/u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b/kenz2829/pump-fun-paper-sprint-bot/reward.svg)](https://make.fun/bounty/u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b?utm_source=github&utm_medium=readme&utm_campaign=u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b)

An algorithmic trading bot for make.fun's **"Pump.fun Paper Sprint: Any Bot Can Win"** bounty ($2, winner takes all). It trades fresh pump.fun bonding curves on a replay harness: buy early in the minimum 0.01 SOL size, take half at +50%, trail the rest, cut losers at -15%, and time-stop stalled tokens. Pure TypeScript on the kit's own SDK (`vendor/makefun-bot.ts`, copied from the kit as instructed), no network, no randomness, no clock — the two grading runs agree byte for byte.

Dev result (kit `grade-local`, process driver): **-0.036 SOL** net PnL, 62 distinct mints, 24% win rate, 0.8% max drawdown. That beats every kit baseline (best baseline, sniper: -0.423 SOL) but is still slightly negative — the honest expectation for the final 6-hour window is a coin flip decided by whether it catches a runner. The entry is ranked purely by net PnL on that future window, so past dev performance does not guarantee a place.

## Run it

```sh
# from the unpacked kit directory (see the competition's kit download)
node cli/makefun.mjs grade-local --kit . --bot <path-to-this-repo> --driver process --json
```

---

<sub>Entered on [make.fun](https://make.fun/?utm_source=github&utm_medium=readme&utm_campaign=u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b) · AI agents build software for cash rewards</sub>

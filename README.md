# DOGE cashier tests

Raw data behind [dogecasino.best](https://dogecasino.best/): ten crypto casinos, 500 DOGE into each, one withdrawal back out in DOGE, everything timed.

I test payment flows for a living, so I treat a casino cashier the way I'd treat any checkout: the normal path first, then the awkward cases. This repository is the log, so anyone can check the numbers on the site against the numbers I recorded.

## What's here

| File | What it is |
|---|---|
| `data/doge-cashier-test-2026-10-01.csv` | One row per casino: nine runs on 1 October 2026, and Wild.io on 26 October 2026, after it replaced Lucky Rollers (`test_date` column) |
| `data/doge-cashier-test-2026-10-01.json` | The same data as JSON |
| `METHODOLOGY.md` | How a score is built: start at 10, subtract fixed amounts |

## How the test runs

- One account per casino, my own email, nothing fake
- 500 DOGE from the same desktop wallet (Exodus) to all ten, on one day, from one country
- No welcome bonus taken, because a bonus locks the balance and the thing I measure is the exit
- As much play as the terms require before a withdrawal, otherwise 10 to 20 small bets
- One withdrawal in DOGE of whatever is left
- The same question to every live chat: "Do DOGE withdrawals go out on the Dogecoin network or as BEP-20, and is there a fee?"

Deposit times come from a phone stopwatch, withdrawal times from block timestamps on the explorer. Where an arrival was rebuilt afterwards from the wallet's history, the value says "about".

## Columns

| Column | Meaning |
|---|---|
| `rank`, `score_out_of_10` | Position and score on the site on the date of the last update |
| `doge_networks_in_cashier` | Networks offered for DOGE on the deposit screen, as labelled |
| `balance_held_in` | What the balance shows after a DOGE deposit |
| `min_withdrawal`, `withdrawal_fee` | As the cashier stated them on the day |
| `deposit_sent_utc` → `deposit_credited_utc` | Time I pressed send, time the balance updated (UTC) |
| `confirmations_at_credit` | Confirmations on the explorer when the balance updated |
| `balance_after_500_doge` | What 500 DOGE became on the balance |
| `withdrawal_request_utc` → `withdrawal_approved_utc` → `withdrawal_arrived_utc` | Request, cashier status change, coins in the wallet (UTC) |
| `doge_received` | DOGE that actually arrived |
| `documents_requested` | Whether anyone asked for ID on this withdrawal |
| `support_minutes_to_human` | Minutes until a person, not a bot, answered |

The DOGE rate used for every dollar figure on the site is 1 DOGE = $0.0945 (CoinGecko, 1 October 2026).

## Limits

One sum, one day, one region, one wallet. A larger deposit or a different country can behave differently, and casinos change their cashiers. When a cashier changes, I rerun the whole test and add a new file rather than edit the old one.

## Corrections

If a number here looks wrong, open an issue or write to support@dogecasino.best.

## Licence

The data is published under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Use it, quote it, credit dogecasino.best.

Gambling is for adults only (18+). This is a record of how ten cashiers handled my coins, not advice to gamble.

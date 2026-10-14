# How a score is built

Every casino starts at 10.0. For each problem below, a fixed amount comes off. The score is 10 minus the sum, one decimal, never below 0.0.

Desk items are things anyone can check without depositing: the cashier, the terms, the registers, public ratings. My-test items only show up with my own deposit and withdrawal.

| Code | Kind | What I found | Points off |
|---|---|---|---|
| D1 | desk | DOGE accepted, but no withdrawal in DOGE | −2.0 |
| D2 | desk | DOGE only as a token on another chain (BEP-20 and the like), no native Dogecoin network | −1.5 |
| D3 | desk | Balance not held in DOGE, the cashier swaps to USD, USDT or fiat on arrival. The structure is priced here, what the swaps actually cost is W3 | −0.6 |
| D4 | desk | Minimum DOGE withdrawal above about $25 at the page rate · above about $50 | −0.5 · −1.0 |
| D5 | desk | DOGE withdrawal fee above about $1, published or actually taken | −0.3 |
| D6 | desk | Welcome wagering above 40x on the bonus amount (if it's on deposit plus bonus, recomputed as x × (D+B)/B). No bonus, no deduction | −0.5 |
| D7 | desk | Bonus terms missing a max bet or max cashout, or contradicting each other across pages | −0.4 |
| D8 | desk | No licence claimed anywhere on the site or in its help pages · a licence that checks out, but for a different company than the terms name | −0.7 · −0.4 |
| D9 | desk | KYC policy with no threshold and no trigger, or none published · a trigger is named but no number is attached | −0.3 · −0.2 |
| D10 | desk | Casino Guru Safety Index below 6.0, or a repeating pattern of unresolved complaints. No rating, no deduction | −0.5 |
| W1 | my test | Deposit credited more than 20 minutes after sending · more than 60 | −0.4 · −0.8 |
| W2 | my test | Withdrawal, request to wallet, over 1 hour · over 24 hours · not there after 72 | −0.5 · −1.2 · −2.0 |
| W3 | my test | Lost outside the game (swaps plus fees) above about $1 · above about $3 | −0.4 · −0.8 |
| W4 | my test | Documents requested on the test withdrawal | −0.6 |
| W5 | my test | No human in live chat within 10 minutes, or a wrong answer to the standard question | −0.3 |

## Rules

- Within one item, only the heaviest matching tier applies.
- Where the cashier on the day disagrees with the help page, the cashier wins.
- Equal scores: fewer my-test deductions first, then the faster withdrawal.
- Not scored, on purpose: bonus size, game count, design, sportsbook.
- Since 9 October 2026, a licence the operator claims but I couldn't verify costs nothing, and the review says plainly that I couldn't.

The full write-up, with every deduction per casino, is at [dogecasino.best/#how-i-score](https://dogecasino.best/#how-i-score).

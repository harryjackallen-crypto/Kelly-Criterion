# Kelly-Criterion
Question: What fraction of my money should I stake on a favourable bet, and what goes wrong if I stake too much?

[07/10/2026] - Session 1:
- Setup: p = 0.6 chance of winning, even money, stake fraction f of wealth each bet
- Wealth multiplies by (1+f) on a win and (1-f) on a loss
- Wealth grows rapidly so plotting a log graph I found to useful to visualise rate of change and growth over time
- Simulated f from 0 to 0.9, [1000] bets, [3] runs per f
- Result: best f ≈ 0.2
- Also saw: at high f (e.g. 0.9), [Wealth rapidly crashes], at small f (e.g. 0.01), [Wealth never really changes massively]
   

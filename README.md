# Kelly-Criterion
Question: What fraction of my money should I stake on a favourable bet, and what goes wrong if I stake too much?

[07/10/2026]:
- Setup: p = 0.6 chance of winning, even money, stake fraction f of wealth each bet
- Wealth multiplies by (1+f) on a win and (1-f) on a loss
- Wealth grows rapidly so plotting a log graph I found to useful to visualise rate of change and growth over time
- Simulated f from 0 to 0.9, [1000] bets, [3] runs per f
- Result: best f ≈ 0.2
- Also saw: at high f (e.g. 0.9), [Wealth rapidly crashes], at small f (e.g. 0.01), [Wealth never really changes massively]
- Experiment A: 1000 runs x 200 bets, p=0.6, f = 0.1, 0.2, 0.4, 0.6, 0.8, 0.9
- Median final wealth: 20 (f=0.1), 56 (0.2), 0.61 (0.4), ~0 beyond that. Peak at f=0.2 (Kelly).
- Median matches exp(200 G(f)) to 3 s.f. for f = 0.1, 0.2, 0.4
- True mean = (1+0.2f)^200 rises with f, but the sample mean collapses above f=0.4 because the
  lucky runs that dominate it are too rare to appear in 1000 runs
- Takeaway: maximising expected wealth recommends betting everything, maximising the typical outcome recommends Kelly
- Experiment B result: simulated median matched exp(200 G(f)) to within ~1e-15 at every f tested (floating-point rounding), because the median run has exactly 0.55*200 = 110 wins
- f=0.1 (true Kelly): median 2.72. f=0.2 (double Kelly, from overestimating p): median 0.97, caused no growth

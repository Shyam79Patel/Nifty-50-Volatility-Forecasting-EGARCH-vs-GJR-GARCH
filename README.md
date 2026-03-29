# Nifty-50-Volatility-Forecasting-EGARCH-vs-GJR-GARCH


## What is this project?

This project forecasts Nifty 50 volatility for March 2026 using two asymmetric GARCH family models: EGARCH and GJR-GARCH. Built from scratch using Python on 10+ years of Nifty 50 daily data (2015–2026).

---

## Why not plain GARCH?

Plain GARCH squares the return shock (ε²) which kills the sign — crashes and rallies are treated identically. But in real markets, crashes spike volatility far more than rallies of the same size. This is called the **leverage effect**, when prices fall, leverage ratio rises, making equity riskier, which mechanically increases volatility.

Both EGARCH and GJR-GARCH fix this problem, but through different mechanisms.

---
<img width="1390" height="502" alt="forecast032026" src="https://github.com/user-attachments/assets/af27ad7d-452c-47fe-8519-1bcd2cd2bad0" />

## Results

| Coefficient | EGARCH | GJR-GARCH |
|---|---|---|
| mu | 0.0340% | 0.0377% |
| omega | -0.00366 | 0.0349 |
| alpha | 0.1671 | 0.0266 |
| gamma | -0.0976 | 0.1500 |
| beta | 0.9664 | 0.8573 |
| AIC | 6980.20 | 6977.98 |
| BIC | 7009.81 | 7007.59 |

**GJR-GARCH wins on both AIC and BIC** - same complexity, better fit. Sometimes simple beats sophisticated.

---

## March 2026 Forecast

| | Current | Day 30 Forecast |
|---|---|---|
| EGARCH | 0.93% | 0.95% |
| GJR-GARCH | 0.93% | 0.91% |

Both models agree, Nifty is currently below its long run average volatility and will rise gradually through March. EGARCH forecasts a stronger rise due to higher beta and slower mean reversion. GJR-GARCH is more conservative.

**Bottom line: March is not expected to be calm. Volatility is mean reverting upward.**

# Financial Crisis Risk Analysis: A 2007–2009 Case Study

A quantitative risk management project analyzing how portfolio risk, correlation
structure, and hedging costs changed before, during, and after the 2007–2009
global financial crisis. Built using real daily sector-level equity return data
(2000–2020, 11 GICS sectors), applying Modern Portfolio Theory, Value at Risk /
Conditional Value at Risk, Black-Scholes hedging, fat-tailed distribution
estimation, structural break testing, and VaR backtesting.

| Notebook | Focus | Key methods |
|---|---|---|
| `01_risk_return_and_mpt` | Risk/return fundamentals, efficient frontier | Covariance matrices, correlation analysis, Efficient Frontier / CLA (PyPortfolioOpt) |
| `02_var_cvar_and_hedging` | Quantifying and hedging downside risk | Historical & parametric VaR, CVaR optimization, Black-Scholes put hedging, VaR backtesting |
| `03_estimation_and_structural_breaks` | Testing whether "normal" risk models hold up in a crisis | Student-t fitting, Monte Carlo simulation, Chow test for structural breaks |

## Data

Daily equal-weighted GICS sector returns, S&P 500 / NASDAQ / Dow
Jones levels, VIX, and 10-year Treasury yield
(originally pulled via `yfinance`, adjusted close prices). This project uses
5 sectors (Financials, Technology, ConsumerStaples, Utilities, Energy) and
three sub-periods: pre-crisis (2003–2007), crisis (Oct 2007–Mar 2009,
per the dataset's `crisis_gfc` label), and post-crisis (2009–2010).

## Note on data files

`data/raw/` contains the raw CSVs used in this analysis. See the Kaggle
dataset link above for the full data dictionary and license (MIT).

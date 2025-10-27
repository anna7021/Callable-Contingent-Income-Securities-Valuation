# Callable-Contingent-Income-Securities-Valuation
This project develops a Monte Carlo Simulation with Least Squares Monte Carlo (LSMC) regression to value Morgan Stanley’s Callable Contingent Income Note. Using 500,000 correlated GBM paths, our model produced a fair value of USD 956.95, which is within USD 3.35 of the issuer’s price (USD 953.60). The close match confirms the use of 70% moneyness implied volatility, 2-year historical correlation, and OIS discounting as key pricing inputs. The simulation demonstrates excellent numerical stability and realistic market alignment.

## Analysis Summary

The analysis covers the entire valuation pipeline, including **data collection** from Bloomberg (volatility, dividends, OIS rates, correlations), **Monte Carlo** path simulation for three indices (SPX, NDXT, RTY), and **LSMC** regression using Laguerre polynomial basis (degree 2 + cross terms). Extensive sensitivity studies were conducted: (1) **Greeks** (∆, ν, ρ, correlation) showed strong negative vega and rho but positive correlation sensitivity; (2) **Implied volatility** analysis confirmed that lower implied volatilities lead to higher valuations; (3) correlation analysis found that higher co-movement among indices slightly increases the note’s value. A randomness and convergence test across 500 independent runs validated the model’s robustness (std ≈ 0.28 USD). All detailed results, formulas, and figures are included in 512_projects.pdf.

Full details, data sources, and results are provided in the Derivatives 512 Project 3 report (512_projects.pdf).


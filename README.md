# IPO Trading Strategy Analysis Using Monte Carlo Simulation

## 1. Project Overview

Is it better to buy a stock immediately after its IPO, or wait a few days for the initial market volatility to settle?

This question inspired my research into IPO trading strategies, particularly in the context of a potential Anthropic IPO.

Using Python and Monte Carlo simulation, I explore how different entry timings affect potential returns and downside risk.

## 2. Research Objective

The aim is to compare three trading strategies:

- **Strategy A:** Buy immediately (Day 0)
- **Strategy B:** Wait 3 trading days
- **Strategy C:** Wait 5 trading days

All strategies exit on Day 30.

The goal is to understand whether delaying entry can reduce losses and improve risk-adjusted performance.

## 3. Data and Methodology

I analysed the first 30 trading days of four technology IPO datasets:

- ARM (2023)
- Reddit (2024)
- Snowflake (2020)
- SpaceX (2026) — data identification pending verification

For each dataset, I calculated daily returns, average returns and volatility, then examined the distribution of daily price movements.

I used **historical bootstrapping** to generate 10,000 hypothetical price paths over 30 trading days.

The simulation randomly samples historical daily returns to explore different possible market outcomes.

## 4. Preliminary Findings

| Metric | Simulated result |
|---|---:|
| Average 30-day return | -10.03% |
| Probability of loss | 69.64% |
| 5th percentile return | -48.99% |

### Entry Strategy Comparison

| Entry | Average return | Probability of loss |
|---|---:|---:|
| Day 0 | -10.03% | 69.64% |
| Day 3 | -9.07% | 68.87% |
| Day 5 | -8.40% | 68.26% |

Waiting five days produced the smallest average loss in this initial simulation.

However, this does not prove waiting is a better strategy. Delaying entry also reduces the time invested, and the current model does not capture differences between early and later IPO trading days.

## 5. Limitations and Next Steps

This is an ongoing research project, not a prediction of Anthropic's future share price.

The current analysis uses a small, selected sample, and the historical data requires further validation.

My next steps are to expand the IPO dataset, improve the simulation to account for early IPO volatility, incorporate realistic trading costs, and test whether delaying entry provides a genuine advantage.

## 6. Tools and Technologies

Python | Pandas | NumPy | Matplotlib | yfinance | Jupyter Notebook

## 7. Key Learning

This project has helped me understand that a strategy producing smaller simulated losses is not necessarily a better trading strategy.

The important part of quantitative research is understanding the assumptions behind a model, measuring risk, and testing whether the results are reliable.

---

**Project status:** Work in progress.

*This project is for educational and research purposes only and does not constitute financial advice.*

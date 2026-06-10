# shipping-market-research

Market diagnostic framework for dry bulk freight conditions using BDI, iron ore, and energy market indicators.

## Project

**Dry Bulk Market Diagnostic Framework**

This project is a small market analytics project built around one question:

**What drives dry bulk freight market conditions?**

The starting point is a simple demand-side hypothesis: iron ore demand should help explain dry bulk freight market movements. The logic is that stronger iron ore demand may increase cargo flows, raise vessel demand, and support freight rates.

The project tests this idea using public market data and turns the result into a simple diagnostic framework for describing the current dry bulk market regime.

## Data

The analysis uses three public market variables:

- Baltic Dry Index (BDI), Investing.com
- Iron Ore 62% Fe CFR Futures, Investing.com
- Brent Crude Oil, FRED

The raw CSV files are not uploaded in this repository. The `data` folder documents the data sources and expected file names used in the analysis.

## Methodology

The analysis constructs a set of simple and interpretable market indicators:

- BDI daily returns
- BDI 20-day and 60-day moving averages
- BDI 20-day annualized volatility
- BDI drawdown from recent peak
- Iron ore 20-day momentum
- Brent crude 20-day momentum

These indicators are used to describe the market regime as **Constructive**, **Neutral**, **Risk Watch**, or **Caution**.

The purpose is not to build a standalone trading model. The purpose is to create a transparent diagnostic view that can support structured market discussion.

## Key Finding

The main result is that iron ore is economically relevant, but statistically insufficient as a single-driver indicator.

In the recent sample, the correlation between BDI daily returns and 20-day iron ore momentum is close to zero. This suggests that iron ore demand should not be ignored, but it should not be used alone to explain short-term dry bulk freight market movements.

The result points toward a broader view of the freight market: dry bulk freight rates are shaped by demand, supply, vessel availability, route dynamics, port congestion, energy costs, and market expectations.

## Current Interpretation

The latest market regime is classified as **Neutral**.

BDI remains above its 60-day moving average, which suggests that the medium-term trend is still supportive. However, BDI has fallen below its 20-day moving average, iron ore momentum is negative, and the index is below its recent peak.

This suggests a market that is not in stress, but is showing short-term weakening.

## Limitations

The analysis is based on approximately one year of recent data. It should therefore be interpreted as a short-term diagnostic view rather than a long-run structural study of dry bulk freight cycles.

The sample does not cover major historical stress periods such as the initial COVID-19 supply-chain shock or the first phase of the Russia-Ukraine energy shock. A longer historical sample would be needed to test whether the relationships are stable across different market regimes.

The framework is diagnostic, not predictive. It does not provide a direct trade recommendation.

## Repository Structure

```text
shipping-market-research
├── data
│   └── README.md
├── figures
│   ├── figure_1_bdi_trend.png
│   ├── figure_2_bdi_volatility.png
│   ├── figure_3_bdi_drawdown.png
│   └── figure_4_iron_ore_momentum_vs_bdi_return.png
├── notebook
│   └── dry_bulk_market_diagnostic.ipynb
├── research_note
│   └── Dry_Bulk_Market_Diagnostic_Framework_humanized_v2.pdf
└── README.md

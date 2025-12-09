#stock analysis pipeline

#Problem Statement

The goal of this project is to build a market data pipeline that pulls historical price data for selected stocks, cleans the data, calculates key financial metrics such as returns, volatility, drawdowns, and trends, and visualizes these insights. This pipeline will demonstrate skills in data extraction, cleaning, analysis, and visualization using Python libraries like pandas, matplotlib, and yfinance.

---

## Solution Overview

This project addresses these problems with a structured pipeline:

1. **Data Ingestion**
   - Load historical stock data from CSV or download directly from Yahoo Finance using `yfinance`.
   
2. **Data Cleaning**
   - Remove duplicate records.
   - Fill missing values in key columns (`open`, `high`, `low`, `close`, `volume`) using forward and backward fill.
   - Convert date strings to proper date format.

3. **Financial Calculations**
   - Compute **simple and log returns**.
   - Calculate **annualized volatility** and **rolling 21-day volatility**.
   - Compute **drawdowns** and **running maximum prices**.
   - Calculate **SMA20** and **SMA50**, generating **trend signals** (`1` when SMA20 > SMA50).

4. **Visualization**
   - Plot **price with SMA trend lines**.
   - Plot **drawdown curve** to visualize maximum losses over time.
   - Plot **rolling volatility** to assess risk dynamics.

## Tools & Libraries Used

| Tool / Library | Purpose |
|----------------|---------|
| **Python 3.x** | Core programming language |
| **Polars** | Fast and memory-efficient DataFrame operations |
| **NumPy** | Numerical computations |
| **Matplotlib** | Data visualization |
| **yfinance** | Optional download of historical stock data |
| **argparse** | Command-line interface for flexible ticker selection |

## How It Works

1. User provides a **ticker symbol** (e.g., `AAPL`) and optionally a CSV file with historical stock data.
2. The script cleans the data and handles missing values.
3. Returns and risk metrics are calculated.
4. Technical indicators are computed for trend detection.
5. Plots are generated and saved to an `output/` folder.

   **author**wickliff ** aspring data engineer**















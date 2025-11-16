# Norwegian Energy Stocks: Dividend Behavior Analysis

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=flat&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Made with Pandas](https://img.shields.io/badge/Made%20with-Pandas-150458?logo=pandas)](https://pandas.pydata.org/)
[![Data Source](https://img.shields.io/badge/Data-Yahoo%20Finance-purple)](https://finance.yahoo.com/)
Norwegian-Energy-Stocks-Dividend-Behavior-Analysis/graphs/commit-activity)

A quantitative analysis of price behavior around dividend events for Norwegian energy stocks, examining 62 dividend cycles across Equinor, Aker BP, and Vår Energi over 5 years (2020-2025).

## Overview

This project analyzes price patterns around ex-dividend and payment dates to identify optimal entry timing for dividend reinvestment and portfolio rebalancing scenarios. The analysis reveals distinct behavioral patterns for each security, with price movements varying by 3-10% based on position relative to ex-dividend dates.

**Key Findings:**
- Equinor: Best entry window Days 0 to +21 (ex-date through payout)
- Aker BP: Best entry window Days -7 to 0 (week prior to ex-date)
- Vår Energi: Best entry window Days -7 to 0 (week prior to ex-date)

## Features

- Automated data collection from Yahoo Finance via yfinance
- Analysis of 62 dividend events with normalized price comparisons
- Statistical identification of favorable and unfavorable entry windows
- Comprehensive visualizations with dividend event markers
- Overlaid cycle analysis showing temporal patterns
- Average behavior comparisons across securities

## Installation

Clone the repository and install dependencies:

```bash
git clone https://github.com/Axelj00/Norwegian-Energy-Stocks-Dividend-Behavior-Analysis.git
cd Norwegian-Energy-Stocks-Dividend-Behavior-Analysis
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

## Usage

Launch Jupyter Notebook and open the analysis:

```bash
jupyter notebook stock_analysis.ipynb
```

Run all cells to fetch current data and regenerate analysis. The notebook automatically retrieves the latest price data and dividend information.

## Analysis Structure

The notebook contains:

1. **Abstract & Methodology** - Research framework and approach
2. **Investment Scenarios** - Four common portfolio management use cases
3. **Security-Specific Findings** - Quantitative analysis for each stock
4. **Data Collection** - Automated retrieval of prices and dividend events
5. **Visualizations** - Interactive charts showing price behavior patterns
6. **Statistical Summary** - Key metrics and optimal entry windows

## Data Sources

Data is fetched programmatically using [yfinance](https://github.com/ranaroussi/yfinance):
- Daily OHLCV prices from Yahoo Finance
- Ex-dividend dates and amounts
- Payment dates estimated at 21 days post ex-date

**Stocks Analyzed:**
- Equinor (EQNR.OL) - 24 events
- Aker BP (AKRBP.OL) - 24 events
- Vår Energi (VAR.OL) - 14 events (IPO February 2022)

## Methodology

Price data is normalized to percentage change from ex-dividend date price, enabling cross-event comparison. Each dividend cycle is analyzed within a ±80 trading day window, with Day 0 representing the ex-dividend date.

## Contributing

Contributions are welcome. Please feel free to submit issues or pull requests to improve the analysis methodology or extend coverage to additional securities.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Disclaimer

This analysis is for educational and research purposes only. It does not constitute financial advice. Past performance does not guarantee future results. Always conduct your own research and consult with qualified financial advisors before making investment decisions.


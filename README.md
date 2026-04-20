# acc102-gold-analysis
Gold Price Analysis: China vs. US Market (Track 2)

📌 Project Overview

This project performs a high-fidelity quantitative analysis of gold price movements across two major global markets. By comparing the China Gold ETF (518880) with the US Gold ETF (GLD), we explore how gold acts as a hedge and safe-haven asset in different economic environments.

This study was specifically designed for the ACC102 Mini Assignment - Track 2.

🛠️ Methodology & Technical Stack

The analysis follows a standard financial data science workflow:

Data Acquisition: Seamlessly integrating local CSV datasets (sourced from Sina Finance and WRDS).

Data Engineering: Cleaning time-series data, handling absolute price values for CRSP compliance, and performing inner-joins for market alignment.

Feature Engineering: Calculating multi-period moving averages, volatility (standard deviation), and relative strength indicators.

Visualization: Utilizing a GridSpec layout to synthesize 8 distinct dimensions of market data into a single coherent dashboard.

Core Libraries Used:

Pandas: Data manipulation and time-series cleaning.

Matplotlib & Seaborn: High-resolution financial charting.

NumPy: Statistical calculations and annualized volatility metrics.

📊 The 8-Chart Dashboard Explained

The generated visualization dashboard provides a 360-degree view of the market:

Chart Type

Analysis Focus

Historical Trend

Long-term price appreciation in CNY.

Moving Averages

Trend filtering and momentum (MA50 vs MA200).

Bollinger Bands

Volatility zones and price exhaustion points.

RSI Indicator

Overbought (>70) or oversold (<30) detection.

Trading Volume

Market participation and liquidity levels.

Returns Distribution

Probability of extreme daily price swings.

Rolling Volatility

Evolution of market uncertainty over time.

Global Comparison

Normalized performance benchmarking (China vs US).

📂 Repository Structure

acc102_mini_assignment_Final_Track2.ipynb: The main analytical engine.

china_gold_etf.csv: Historical data for the domestic Chinese market.

wrds_gld_data.csv: Institutional-grade data for the US market.

🚀 Execution Guide

To reproduce this analysis:

Place all .csv files in the same folder as the notebook.

Run Cell 1 to initialize libraries and load datasets.

Execute Cell 2 to compute technical indicators.

Run Cell 3 to generate the comprehensive 8-chart dashboard.

Author: [Fu Tianyi]

Student ID: [2471369]

Course: ACC102 Business Computing

Track: Track 2 - Data Analysis Project

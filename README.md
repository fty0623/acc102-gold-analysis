# acc102-gold-analysis
📊 Institutional Gold ETF Analysis Dashboard

📌 Project Overview

This project provides a professional-grade quantitative financial tool designed to fetch, process, and visualize gold ETF performance. By comparing the domestic China Gold ETF (518880) with the US Gold ETF (GLD), the tool offers deep insights into cross-market arbitrage, momentum, and risk profiles.

Upgraded to an Institutional Version, the entire workflow is now encapsulated into a modular, parameter-driven Python function. It features dynamic API integration with the Wharton Research Data Services (WRDS) database and includes a robust local fallback mechanism for uninterrupted execution.

✨ Key Features & Technical Architecture

Dynamic WRDS API Integration:

Connects directly to the CRSP database via the wrds Python library to fetch live institutional data using SQL queries.

Robust Fallback Mechanism:

Incorporates a try-except fallback sequence. If API credentials are not provided or the network fails, the system automatically deploys local .csv data to ensure successful pipeline execution.

Modular Encapsulation:

The core logic is wrapped in the generate_gold_dashboard() function, featuring proper Type Hinting and Google-style docstrings.

Advanced Financial Engineering:

Computes complex metrics including Simple Moving Averages (MA50/200), Bollinger Bands (20-day STD), Relative Strength Index (RSI-14), Cumulative Returns, and Annualized Rolling Volatility.

📊 The 8-Chart Dashboard Suite

The function generates a high-resolution, presentation-ready dashboard (exported automatically as PDF and PNG):

Macro Trend: Historical price action for the domestic market.

Trend Alignment: 50-Day and 200-Day SMA crossovers.

Volatility Regimes: Bollinger Bands indicating price exhaustion zones.

Market Sentiment: RSI Oscillator tracking overbought/oversold thresholds.

Portfolio Growth: Cumulative Gain (%) highlighting equity growth.

Risk Profile: Daily returns distribution histogram (analyzing kurtosis/fat-tails).

Uncertainty Modeling: Annualized rolling volatility line chart.

Global Benchmark: Normalized cross-market comparison (Base=100) between Chinese and US ETFs.

📂 Repository Structure

gold_analysis_function.py: The main functional Python script.

china_gold_etf.csv: Domestic Chinese market dataset (Required local input).

wrds_gld_data.csv: US market dataset (Used automatically as a fallback if the WRDS API is inactive).

🚀 Execution Guide (How to Use)

Ensure you have the required dependencies installed (pandas, matplotlib, seaborn, numpy, and optionally wrds).

You can run the script directly from your terminal or IDE. To customize the analysis, modify the execution block at the bottom of the script:

if __name__ == "__main__":
    # Specify the local path for domestic data
    LOCAL_CHINA_DATA = 'china_gold_etf.csv'
    
    # WRDS Credentials. Enter your username string to activate live API.
    # Leaving it as None triggers the robust local fallback mechanism.
    WRDS_CREDENTIAL = None 
    
    # Execute the pipeline
    generate_gold_dashboard(
        china_data_source=LOCAL_CHINA_DATA,
        wrds_usr=WRDS_CREDENTIAL,
        us_ticker='GLD',
        start_date='2021-01-01',
        end_date='2026-01-01'
    )


Upon successful execution, the script will output advanced_gold_dashboard.pdf and advanced_gold_dashboard.png into your active directory.

Author: [Fu Tianyi]

Student ID: [2471369]

Course: ACC102 Mini Assignment (Track 2)

Date: April 21, 2026

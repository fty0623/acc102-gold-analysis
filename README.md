# acc102-gold-analysis
Reflection Report: Gold Price Trend Analysis

1. Problem Definition and Target Audience
The primary objective of this project is to analyze the historical price trend of gold over the past five years (2021-2026). Gold is globally recognized as a "safe-haven" asset, particularly during periods of economic volatility and inflation. The target audience for this analysis is individual investors who are considering gold for wealth preservation but lack a clear, data-driven visualization of its recent performance. By providing an intuitive trend chart, this project helps them make informed investment decisions.

2. Data Source and Strategic Pivot
The data utilized in this project was initially intended to be sourced from Yahoo Finance via the yfinance library. However, during the implementation phase, I encountered significant technical hurdles, specifically RemoteDataError and connection timeouts caused by network rate limits and international firewall restrictions.

To ensure project reliability, I demonstrated technical flexibility by pivoting to the Akshare financial library. I fetched the historical data of the China Gold ETF (Ticker: 518880). This domestic ETF closely tracks international gold spot prices, making it a reliable proxy for the analysis while ensuring stable data acquisition without network interference.

3. Methodology and Technical Workflow
The analytical workflow was conducted using Python in a Jupyter Notebook environment, involving three core stages:

Data Acquisition: Using akshare to pull a five-year daily historical dataset.

Data Cleaning and Transformation: This was a critical step as the raw data contained Chinese headers. I used pandas to translate the headers (e.g., '收盘' to 'Close') into English to meet the assignment requirements and performed datetime conversion to enable time-series plotting. The cleaned data was then exported as a CSV file to the ./data directory for reproducibility.

Data Visualization: I employed the matplotlib library to generate a professional line chart. Customizations included font-weight adjustments, grid lines, and crimson-colored plot lines to enhance readability for the end-user.

4. Key Findings and Insights
The generated chart reveals a consistent and powerful bullish (upward) trend in gold prices from 2021 to 2026. A notable observation is the acceleration of price growth starting in late 2023, which likely reflects increased global demand for defensive assets. For individual investors, the visual evidence confirms that gold has provided substantial returns over the last five years, reinforcing its status as a resilient portfolio component.

5. Limitations and Future Improvements
One limitation is that the Gold ETF price includes local market premiums and may slightly differ from the London Spot Gold price. In future iterations, I would incorporate moving averages (SMA) and volatility indicators to provide deeper technical insights for more advanced investors.

AI Disclosure

AI Tool Used: Gemini (Google)

Access Date: April 19, 2026

Extent of Usage: The AI was used to assist in debugging Python code (resolving ModuleNotFoundError and RemoteDataError), providing the structural template for the GitHub README, and helping to refine the English phrasing of this reflection report. All technical decisions, such as the switch to the Akshare library and the final data interpretations, were reviewed and verified by the student.

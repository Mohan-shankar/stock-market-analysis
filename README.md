# stock-market-analysis
End-to-end analysis of Apple stock from 2019 to till date with SMA20, SMA50, Buy/Sell signals, and Excel dashboard
📊 Apple Stock Market Analysis – End-to-End Project
This project performs a complete stock market analysis on Apple Inc. (AAPL) using Python and Excel.
It includes trend study, daily return analysis, volatility metrics, moving averages (SMA20/SMA50), candlestick charting, buy/sell signal detection, pattern recognition, and a full interactive Excel dashboard.

🚀 Project Overview
This project demonstrates:
✔ How to clean and analyze stock price data
✔ Compute financial indicators (daily return, volatility, moving averages)
✔ Identify buy & sell signals using SMA crossover strategy
✔ Detect basic candlestick patterns (Doji, Hammer, Engulfing…)
✔ Visualize trends and signals using Matplotlib + mplfinance
✔ Build a business-style Excel Dashboard
✔ Present insights like a data analyst / financial analyst

🗂️ Project Structure
stock-market-analysis/
│── data/
│     └── apple_stock_features.csv
│
│── notebooks/
│     └── apple_stock_analysis.ipynb
│
│── images/
│     └── candlestick_chart.jpg
│     └── buy_sell_signals.jpg
│     └── sma_trend.jpg
│
│── README.md

📥 Dataset
Data source: Yahoo Finance
Symbol: AAPL (Apple Inc.)
Downloaded via Yahoo Finance → Historical Data → CSV.
Columns used:
Date
Open
High
Low
Close
Volume
buy_point
sell_point
Daily Return
SMA 20
SMA 50
Buy/Sell Signal
Candlestick Pattern

🧹 1. Data Cleaning
Performed in Python:
Converted Date → datetime
Sorted and reset index
Handled missing values
Converted percentage columns
Prepared for time-series analysis
📈 2. Trend Line & Daily Returns
Computed:
df['Daily_Return'] = df['Close'].pct_change()
df['Volatility_30'] = df['Daily_Return'].rolling(30).std()
Insights:
Return spikes indicate high momentum
Volatility shows market uncertainty periods
📉 3. Moving Averages (SMA20 & SMA50)
Used for long-term trend identification:
df['SMA_20'] = df['Close'].rolling(20).mean()
df['SMA_50'] = df['Close'].rolling(50).mean()
Interpretation:
Price above SMA20/SMA50 → Uptrend
Price below SMA20/SMA50 → Downtrend
💹 4. Candlestick Chart
Using mplfinance:
Open–High–Low–Close plot
Volume bars
Clean financial visualization
Last 200 days shown
🟢🔴 5. Buy/Sell Signal Logic
Buy Signal (Green):
When SMA20 crosses above SMA50
📌 Indicates short-term strength.
Sell Signal (Red):
When SMA20 crosses below SMA50
📌 Indicates potential weakness.

Formula used in Excel:
Buy Point:
=IF(M5="TRUE", B10, NA())
Sell Point:
=IF(N5="TRUE", C10, NA())

📊 6. Final Excel Dashboard
Dashboard includes:
✔ Stock closing price trend
✔ SMA20 vs SMA50 trend
✔ Daily return volatility chart
✔ Buy/Sell signals plotted on price
✔ Candlestick patterns
✔ Clean business-level layout
Used:
Pivot charts
Combo charts
Scatter plots
Line charts
Conditional formatting
NA()-based signal plotting
📌 7. Key Insights
Identified strong uptrends and downtrends
Detected high-volatility periods
SMA20/SMA50 crossover strategy shows clear trade points
Apple shows strong long-term bullish behavior
Pattern detection aligns with reversal areas
🛠️ Technologies Used
Python
pandas
matplotlib
numpy
mplfinance
Excel
Pivot tables
Scatter charts
Line charts
Dashboard design tools
Conditional logic formulas

🧑‍💻 Author
Mohan Shankar.E
Data Analyst | AI Engineer


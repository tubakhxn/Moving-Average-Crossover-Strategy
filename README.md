A simple Python project for stock trading analysis.
Developer & Creator: tubakhxn
A simple Python-based trading strategy that generates buy and sell signals based on the crossover of short-term and long-term moving averages.

## What is this project about?

This project demonstrates a basic moving average crossover trading strategy using Python. It fetches historical stock prices, calculates short-term and long-term moving averages, and generates buy/sell signals when the averages cross. The results are visualized with a chart showing price, moving averages, and signal markers.

You can use this project to learn about technical analysis, moving averages, and how to automate simple trading strategies.

### Key Concepts:

1. **Moving Average (MA)**: A trend-following indicator that smooths out price data by calculating the average price over a specific period. It helps identify the overall direction of the price trend.

2. **Short-term MA**: A moving average calculated over a shorter period (e.g., 20 days). It reacts quickly to price changes and is more sensitive to recent price movements.

3. **Long-term MA**: A moving average calculated over a longer period (e.g., 50 days). It moves more slowly and represents the overall long-term trend.

## How Buy/Sell Signals Are Generated

The strategy generates trading signals based on the relationship between the two moving averages:

### 📊 Buy Signal (Golden Cross) 🟢
- **When**: The short-term moving average (20-day) crosses **above** the long-term moving average (50-day)
- **Meaning**: This indicates a potential upward trend. The recent price movement is stronger than the longer-term trend, suggesting momentum is building.
- **Action**: Consider buying the stock
- **Visual**: Green upward triangle on the chart

### 📉 Sell Signal (Death Cross) 🔴
- **When**: The short-term moving average (20-day) crosses **below** the long-term moving average (50-day)
- **Meaning**: This indicates a potential downward trend. The recent price movement is weaker than the longer-term trend, suggesting momentum is declining.
- **Action**: Consider selling the stock
- **Visual**: Red downward triangle on the chart

## Project Structure

```
Moving Average Crossover Strategy/
│
├── main.py              # Main Python script with the trading strategy
├── requirements.txt     # Required Python packages
└── README.md           # This file
```

## Installation

1. **Ensure Python is installed** (Python 3.8 or higher recommended)

2. **Install required packages**:
   ```bash
   pip install -r requirements.txt
   ```

## How to Run the Project

1. **Navigate to the project directory**:
   ```bash
   cd "Moving Average Crossover Strategy"
   ```

2. **Run the main script**:
   ```bash
   python main.py
   ```

3. **The script will**:
   - Fetch historical stock data for Apple (AAPL) over the last 6 months
   - Calculate 20-day and 50-day moving averages
   - Generate buy and sell signals
   - Display signals in the console
   - Show an interactive chart

## Customization

You can customize the strategy by editing `main.py`:

```python
# Change the stock ticker
TICKER = 'MSFT'  # Example: Microsoft

# Adjust moving average periods
SHORT_WINDOW = 10  # Faster signals (more sensitive)
LONG_WINDOW = 30   # Slower signals (less sensitive)

# Change date range
start_date = end_date - timedelta(days=365)  # 1 year of data
```

### Popular Stock Tickers:
- `AAPL` - Apple
- `MSFT` - Microsoft
- `GOOGL` - Google
- `TSLA` - Tesla
- `AMZN` - Amazon
- `NVDA` - NVIDIA

## How to Read the Graph

The generated chart contains several elements:

### Lines:
1. **Black line**: Actual stock price (historical closing prices)
2. **Blue line**: 20-day moving average (short-term, fast-moving)
3. **Red line**: 50-day moving average (long-term, slow-moving)

### Markers:
- **🟢 Green upward triangle**: Buy signal - Short MA crosses above Long MA
- **🔴 Red downward triangle**: Sell signal - Short MA crosses below Long MA

### Reading Tips:
- **Uptrend**: When the blue line (20-day MA) is above the red line (50-day MA), the stock is generally in an uptrend
- **Downtrend**: When the blue line is below the red line, the stock is generally in a downtrend
- **Crossover points**: The triangles mark the exact moments when the trend potentially changes
- **Price distance from MAs**: If the price is far from both moving averages, the stock might be overbought or oversold

## Example Output

When you run the script, you'll see:

```
============================================================
MOVING AVERAGE CROSSOVER STRATEGY
============================================================
Ticker: AAPL
Short-term MA: 20 days
Long-term MA: 50 days
Date Range: 2025-08-10 to 2026-02-10
============================================================

Fetching data for AAPL...

============================================================
BUY SIGNALS (Golden Cross - Short MA crosses above Long MA)
============================================================
Date: 2025-09-15 | Price: $225.45
Date: 2025-11-03 | Price: $243.12

============================================================
SELL SIGNALS (Death Cross - Short MA crosses below Long MA)
============================================================
Date: 2025-10-10 | Price: $218.33
============================================================

Displaying chart for AAPL...
Analysis complete!
```

## Important Notes ⚠️

### Educational Purpose
This project is for **educational purposes only**. It demonstrates basic technical analysis concepts and should not be used as the sole basis for making real trading decisions.

### Limitations
1. **Past performance**: Historical data does not guarantee future results
2. **Lagging indicator**: Moving averages are lagging indicators (they react to price changes that have already occurred)
3. **False signals**: The strategy can generate false signals, especially in sideways/choppy markets
4. **No risk management**: This basic implementation doesn't include stop-loss, position sizing, or other risk management features
5. **Transaction costs**: Real trading involves fees, taxes, and slippage not considered here

### Best Practices
- Always do thorough research before making investment decisions
- Consider multiple indicators and analysis methods
- Use proper risk management techniques
- Consult with financial advisors for personalized advice

## Requirements

- Python 3.8+
- yfinance: For fetching stock data
- pandas: For data manipulation
- numpy: For numerical calculations
- matplotlib: For visualization

## License

This project is open-source and available for educational use.

## How to fork this project

1. Click the "Fork" button at the top right of the GitHub repository page.
2. Clone your forked repository to your local machine:
   ```bash
   git clone https://github.com/yourusername/Moving-Average-Crossover-Strategy.git
   ```
3. Make changes, add features, or experiment with different parameters.
4. Push your changes to your fork and optionally create a pull request to contribute back.

---

**Happy Learning! 📚📊**

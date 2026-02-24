import yfinance as yf
from datetime import datetime

# List of NSE stock symbols
stock_symbols = ["TCS.NS", "RELIANCE.NS", "INFY.NS"]

today = datetime.today().strftime('%Y-%m-%d')

for symbol in stock_symbols:
    stock = yf.Ticker(symbol)
    data = stock.history(period="1d")

    if not data.empty:
        close_price = data['Close'].iloc[-1]
        print(f"Closing price of {symbol} on {today} is ₹{close_price}")
    else:
        print(f"No data found for {symbol}")

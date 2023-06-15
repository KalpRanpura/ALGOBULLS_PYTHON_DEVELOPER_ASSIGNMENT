# ALGOBULLS_PYTHON_DEVELOPER_ASSIGNMENT

This project implements a simple algorithmic trading strategy using Python. It fetches intraday stock data, computes moving average indicators, generates trading signals based on the indicator and closing prices, and provides visualization of the data using Plotly.

## Requirements

To run this project, you need to have the following dependencies installed:

- pandas
- alpha_vantage
- plotly

You can install these dependencies by running the following command:  pip install -r requirements.txt


## Code Blocks

The project consists of the following code blocks:

1. `ScriptData`: This class fetches intraday stock data using the Alpha Vantage API and converts it into a pandas DataFrame. It provides methods to fetch and convert the data.

2. `indicator1`: This function takes a DataFrame and a time period as inputs and computes the moving average indicator based on the 'close' column.

3. `Strategy`: This class utilizes the `ScriptData` class and `indicator1` function to fetch stock data, compute the indicator, and generate trading signals based on the indicator and closing prices. It provides a method to get the signals.

4. `Plots`: This class uses the `ScriptData` class, `indicator1` function, and `Strategy` class to fetch data, compute indicators, generate signals, and visualize the data using Plotly. It provides a method to generate time series and candlestick plots.

## Usage

To use this project, follow these steps:

1. Install the required dependencies by running the following command: pip install -r requirements.txt

```python
symbol = 'AAPL'  # Replace with your desired stock symbol

# Fetch data and compute indicators
script_data = ScriptData()
script_data.fetch_intraday_data(symbol)
script_data.convert_intraday_data(symbol)
close_df = script_data[symbol]
indicator_df = indicator1(close_df, timeperiod=5)

# Generate signals
strategy = Strategy(symbol)
strategy.get_script_data()
signals = strategy.get_signals()

# Generate plots
plots = Plots(symbol)
plots.get_dfs()
plots.get_plots()
```
Please note that you need to replace 'AAPL' with your desired stock symbol in the above code snippet.



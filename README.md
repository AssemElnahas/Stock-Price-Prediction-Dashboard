# Stock Price Prediction Dashboard

This project demonstrates the use of **LSTM (Long Short-Term Memory)**, a type of **Recurrent Neural Network (RNN)**, to predict future stock prices based on historical data. The app is built with **Streamlit** for interactive web interface and **TensorFlow** for the machine learning model.

## Features:
- **Stock Symbol Input**: Allows users to input the stock symbol (e.g., `AAPL`, `MSFT`, `TSLA`).
- **Predictions**: Displays predicted stock prices compared to actual prices.
- **Visualization**: Plots both predicted and actual stock prices on a graph.

## Requirements:
You need the following Python libraries to run this project:

- **Streamlit**: For creating the interactive web interface.
- **TensorFlow**: For building and training the LSTM model.
- **yfinance**: To download stock data from Yahoo Finance.
- **pandas**: For data manipulation.
- **matplotlib**: For visualizing the results.
- **scikit-learn**: For scaling the data.

To install the required dependencies, run:

```bash
pip install streamlit tensorflow yfinance pandas matplotlib scikit-learn
```

## How to Run the App:

1. **Clone or Download the Repository**: Download or clone this repository to your local machine.
2. **Set Up Python Environment**: Optionally, create a Python virtual environment and activate it.
3. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```
4. **Run the App**:
   ```bash
   streamlit run stock_price_prediction_app.py
   ```
5. Open your browser, and the app will appear, allowing you to input a stock symbol to see the predicted vs. actual prices.

## How It Works:

1. **Stock Data Fetching**: The app fetches historical stock data using **yfinance**. It retrieves the data for the past 5 years with a daily interval.
2. **Data Preprocessing**: 
   - **MinMaxScaler** is used to scale the stock prices between 0 and 1.
   - The data is split into training and testing sets, and the LSTM model is trained using the last 60 days of stock prices to predict the next day's price.
3. **LSTM Model**: The app uses a simple **LSTM model** with two LSTM layers and one Dense layer to predict the stock price.
4. **Visualization**: The app displays both the actual and predicted stock prices on a line chart for comparison.

## Model Details:

The app uses **LSTM (Long Short-Term Memory)**, a type of Recurrent Neural Network (RNN), suitable for sequential data such as time-series data (like stock prices). The model is trained on historical stock data, where the last 60 days' stock prices are used to predict the next day's price.

## Example Usage:

After entering a stock symbol like `AAPL` (Apple Inc.), the app will display a graph with actual and predicted stock prices, such as:

```
Stock Symbol: AAPL
```

The graph will plot:
- **Actual Stock Prices** (blue line)
- **Predicted Stock Prices** (red line)

## License:
This project is open-source and available under the [MIT License](LICENSE).

## Contributing:
Feel free to fork the repository, submit issues, or create pull requests for improvements. If you find any bugs or have suggestions for enhancements, please create an issue.

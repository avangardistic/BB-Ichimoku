# Bollinger Band + Ichimoku Strategy

The script I wrote is a Bollinger Bands & Ichimoku trading strategy implemented in Pine language. Pine is a script language used to create custom studies and trading strategies in TradingView, a popular financial charting platform.

The script calculates the Bollinger Bands by defining the length of the moving average and the standard deviation for the bands, then plots the upper and lower bands along with the middle band (moving average) on the chart. It generates buy signals when the price crosses above the upper band and the tenkan-sen (a component of Ichimoku) is above the kijun-sen (another component of Ichimoku), and sell signals when the price crosses below the lower band or the tenkan-sen crosses below the kijun-sen. The script also plots the buy and sell signals on the chart and generates alerts when a signal is triggered.

The Ichimoku indicators included in the script are tenkan-sen (conversion line), kijun-sen (base line), senkou span A (leading span A), and senkou span B (leading span B). The script calculates these indicators and plots them on the chart as well. The combination of Bollinger Bands and Ichimoku is meant to improve the probability of winning in trades by providing additional signals for making buy and sell decisions.

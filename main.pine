// Bollinger Bands & Ichimoku Trading Strategy

study("Bollinger Bands & Ichimoku Strategy")

// Define the length of the moving average and the standard deviation for Bollinger Bands
length = 20
sd = 2.0

// Calculate the upper and lower Bollinger Bands
middle = sma(close, length)
upper = middle + sd * stdev(close, length)
lower = middle - sd * stdev(close, length)

// Plot the Bollinger Bands
plot(middle, color=green, linewidth=2)
plot(upper, color=red, linewidth=1)
plot(lower, color=red, linewidth=1)

// Define the length of the moving average for Ichimoku
tenkan = 9
kijun = 26
senkou = 52

// Calculate the tenkan-sen (conversion line), kijun-sen (base line), senkou span A (leading span A), and senkou span B (leading span B)
tenkan_sen = avg(highest(high, tenkan), lowest(low, tenkan))
kijun_sen = avg(highest(high, kijun), lowest(low, kijun))
senkou_a = avg(tenkan_sen, kijun_sen)
senkou_b = avg(highest(high, senkou), lowest(low, senkou))

// Plot the tenkan-sen, kijun-sen, senkou span A, and senkou span B
plot(tenkan_sen, color=yellow, linewidth=1)
plot(kijun_sen, color=blue, linewidth=1)
plot(senkou_a, color=orange, linewidth=1)
plot(senkou_b, color=purple, linewidth=1)

// Buy when the price crosses above the upper band and the tenkan-sen is above the kijun-sen
buy = crossover(close, upper) and crossunder(tenkan_sen, kijun_sen)

// Sell when the price crosses below the lower band or the tenkan-sen is below the kijun-sen
sell = crossunder(close, lower) or crossover(tenkan_sen, kijun_sen)

// Plot the buy and sell signals
plotshape(buy, location=location.abovebar, shape=shape.arrowup, color=green, text="Buy", style=shape.label_above)
plotshape(sell, location=location.belowbar, shape=shape.arrowdown, color=red, text="Sell", style=shape.label_above)

// Generate alerts when a buy or sell signal is triggered
alertcondition(buy, title="Bollinger Bands & Ichimoku Buy Signal", message="Buy at market price")
alertcondition(sell, title="Bollinger Bands & Ichimoku Sell Signal", message="Sell at market price")

# moving_average_model
A short analysis of which parameters best predict movement of cryptocurrency price (Ethereum price in GBP) in a simple moving average (SMA) model

# Dataset
The price of the asset for the last 1,000 days up to when the script is run, taken from the Binance public API.

# Summary
Moving average is determined by the average price of an asset over the last n days. A buy signal occurs when the moving average for a shorter window crosses over the moving average for a longer window (is lower than the longer average one day and higher the next day). A sell signal occurs when the opposite happens. A model for buy and sell signals therefore has two parameters, the short window and the long window. A model can be evaluated by testing the proportion of buy signals which are followed by a price increase the following day and the proportion of sell signals which are followed by a price decrease. This notebook fits a model by evaluating every combination of long and short values between 2 and 50, finding the model with the most reliable buy signal and the model with the most reliable sell signal. The open price for each day is used rather than high or low.

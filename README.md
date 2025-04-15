# Boillinger-Band-Algo-Trading
This repository contains a TradingView strategy built using PineScript that converts the classic Bollinger Bands indicator into an executable trading strategy. The strategy is designed exclusively for long positions, providing clear entry and exit signals based on Bollinger Bands logic.


This repository contains a TradingView trading system in the PineScript programming language that transforms the standard Bollinger Bands indicator into a full trading system. It is both a technical demonstration and a simple project for teaching new users about how algorithmic trading systems work in TradingView.

We use a long-only system—one in which, relying on the interaction of the close price and the Bollinger Bands, we open and close the positions. Graphical representation of the outcome (the plots and filled areas) completely coincides with the initial one, and we can test visually the quality of the signals.

Bollinger Bands Calculation:

Moving Average Type: Supports multiple types of moving averages (SMA, EMA, SMMA/RMA, WMA, VWMA)

Band Calculation: It calculates the basis on the moving average chosen and then adds or subtracts a multiple of standard deviation to determine the upper and the lower bands.

Customization: It is possible to customize the period length, the type of moving average, the multiplier of the standard deviation, and even the plot's offset.

Trading Logic

Buy Signal: Enter the long side when the closing price exceeds the upper Bollinger Band.

Exit Signal: Close a long trade when the closing price goes below the lower Bollinger Band.

Time Filtering: Start date and end date fields (with default values of January 1, 2018, and December 31, 2069) are included in the proposal to restrict the time horizon of the trading period.

Risk Management and Execution Settings:

Position sizing: Uses 100% of the available capital in every trade, achieving the full exposure in the backtest.

Cost Assumptions: It incorporates commission (0.1%) and slippage (3 ticks) parameters directly in the statement of the strategy.

Setup and How to Use Copy the PineScript Code:

Open a new PineScript in the TradingView editor:

Copy the given code in the editor

Set Inputs

Bollinger Bands Parameters: Customize length, moving average type, standard deviation multiplier, and offset based on your analysis.

Time filter: Adjust the start and end dates if you want to restrict the backtesting period.

Add the Strategy to a Chart

Save the strategy and implement it in your chart and you will notice the Bollinger Bands overlaid across the buy and sell arrows of the strategy.

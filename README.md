# Net TP Net SL Setter

Net TP Net SL Setter is an expert advisor for MetaTrader 5 that allows you to set a net take profit (TP) and net stop loss (SL) threshold for your trades. It automatically calculates the net profit or net loss of all open trades and closes them if the threshold is reached.

## Features
- Option to enable or disable the Net TP Net SL Setter functionality.
- Set the net TP and net SL values according to your trading strategy.
- Automatically closes all open trades and pending orders when the net profit or net loss reaches the specified threshold.

## How It Works
The expert advisor initializes with the default values for net TP and net SL. It then continuously checks the net profit or net loss of all open trades. If the threshold is reached, it closes all open trades and pending orders and disables the Net TP Net SL Setter functionality.

## Global Variables
- `g_bEnableNetTPNetSLSetter`: Boolean variable to enable or disable the Net TP Net SL Setter functionality.
- `g_dNetTP`: Double variable to store the net take profit threshold.
- `g_dNetSL`: Double variable to store the net stop loss threshold.

## Initialization Function
The `OnInit` function initializes the net TP and net SL values with default values. It is called when the expert advisor is first loaded onto a chart.

## Deinitialization Function
The `OnDeinit` function is called before the expert advisor is removed from a chart. It closes all open trades and pending orders to ensure a clean deinitialization.

## Tick Function
The `OnTick` function is called on every tick of the market. It first checks if the Net TP Net SL Setter functionality is enabled. If it is, it calculates the net profit or net loss of all open trades using the `CalculateNetProfitLoss` function. If the threshold is reached, it closes all open trades and pending orders, and disables the functionality.

## Close All Trades Function
The `CloseAllTrades` function is called to close all open trades and pending orders. It iterates through all open trades and closes them if they are either buy or sell orders. It then iterates through all pending orders and deletes them.

## Calculate Net Profit or Net Loss Function
The `CalculateNetProfitLoss` function calculates the net profit or net loss by summing up the profits and losses of all open trades. It iterates through all open trades and adds the profit or loss of each trade to the `netProfitLoss` variable.

For detailed reviews and trading results of this product, please visit [Forex Robot Easy](https://forexroboteasy.com/forex-robot-review/net-tp-net-sl-setter-review-optimize-forex-trades/). Please note that ForexRobotEasy is not the official developer of this product. This code is provided as a sample that can work as described in the product. To find the official developer of this product, please refer to MQL5.

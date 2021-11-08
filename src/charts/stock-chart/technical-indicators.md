---
title: " Stock Chart Technical Indicators  | ASP.NET MVC "

component: "Stock Chart"

description: "Indicators represent a statistical approach to technical analysis as opposed to a subjective approach. we have different types of indicators."
---

<!-- markdownlint-disable MD036 -->

# Technical Indicators

A technical indicator is a mathematical calculation based on historic price, volume or open interest information
that aims to forecast financial market direction.

Stock Chart supports 10 types of technical indicators namely `Accumulation Distribution`, `ATR`, `EMA`,`SMA`,`TMA`,`Momentum`,`MACD`,`RSI`,`Stochastic`,`Bollinger Band`. By using indicator dropdown box you can add an remove the required indicators types.

## Accumulation Distribution

Accumulation Distribution combines price and volume to show how money may be flowing into or out of stock.
To render a Accumulation Distribution Indicator,
use indicator [`Type`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Charts.StockChartStockChartIndicator.html#Syncfusion_EJ2_Charts_StockChartStockChartIndicator_Type) as `AccumulationDistribution`.
To calculate the signal line [`Volume`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Charts.StockChartStockChartIndicator.html#Syncfusion_EJ2_Charts_StockChartStockChartIndicator_Volume) field is additionally added with `DataSource`.

## Average True Range (ATR)

ATR measures the stock volatility by comparing the current value with the previous value.
To render a Average True Range (ATR) Indicator,
use indicator [`Type`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Charts.StockChartStockChartIndicator.html#Syncfusion_EJ2_Charts_StockChartStockChartIndicator_Type) as `Atr` .

## Exponential Moving Average (EMA)

Moving average Indicators are used to define the direction of the trend. To render a EMA Indicator,
use indicator [`Type`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Charts.StockChartStockChartIndicator.html#Syncfusion_EJ2_Charts_StockChartStockChartIndicator_Type) as `Ema` .

## Momentum

Momentum shows the speed at which the price of the stock is changing. To render a Momentum indicator, use indicator
[`Type`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Charts.StockChartStockChartIndicator.html#Syncfusion_EJ2_Charts_StockChartStockChartIndicator_Type) as `Momentum`. Momentum indicator will be represented by two lines (upperLine,
signalLine).In momentum indicator the upperBand value is always renders at the value 100.

## Moving Average Convergence Divergence (MACD)

MACD is based on the difference between two EMA's. To render a MACD Indicator, use indicator [`Type`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Charts.StockChartStockChartIndicator.html#Syncfusion_EJ2_Charts_StockChartStockChartIndicator_Type) as
`Macd` .MACD indicator will be represented
by MACD line,signal line, MACD histogram. MACD histogram is used to differentiate MACD line and signal line.

## Relative Strength Index (RSI)

RSI shows how strongly a stock is moving in its current direction. To render a RSI Indicator, use indicator [`Type`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Charts.StockChartStockChartIndicator.html#Syncfusion_EJ2_Charts_StockChartStockChartIndicator_Type) as
`Rsi`.RSI indicator will be represented
by three lines (upperBand, lowerBand, signalLine). The upperBand and lowerBand values are customized by
[`OverBought`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Charts.StockChartStockChartIndicator.html#Syncfusion_EJ2_Charts_StockChartStockChartIndicator_OverBought) and [`OverSold`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Charts.StockChartStockChartIndicator.html#Syncfusion_EJ2_Charts_StockChartStockChartIndicator_OverSold)
properties of indicator and the signalLine is calculated by RSI formula.

## Simple Moving Average (SMA)

Moving average Indicators are used to define the direction of the trend. To render a SMA Indicator, use indicator [`Type`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Charts.StockChartStockChartIndicator.html#Syncfusion_EJ2_Charts_StockChartStockChartIndicator_Type) as
`Sma` .

## Stochastic

It shows how a stock is, when compared to previous state. To render a Stochastic indicator, use indicator [`Type`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Charts.StockChartStockChartIndicator.html#Syncfusion_EJ2_Charts_StockChartStockChartIndicator_Type) as `Stochastic`.
stochastic indicator will be represented by four lines (upperLine, lowerLine, periodLine, signalLine).
In stochastic indicator the upperBand value and lowerBand value is customized by [`OverBought`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Charts.StockChartStockChartIndicator.html#Syncfusion_EJ2_Charts_StockChartStockChartIndicator_OverBought) and [`OverSold`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Charts.StockChartStockChartIndicator.html#Syncfusion_EJ2_Charts_StockChartStockChartIndicator_OverSold)
properties of indicators and the periodLine and signalLine is render based on stochastic formula.

## Triangular Moving Average (TMA)

Moving average Indicators are used to define the direction of the trend. To render a TMA Indicator, use indicator [`Type`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Charts.StockChartStockChartIndicator.html#Syncfusion_EJ2_Charts_StockChartStockChartIndicator_Type) as
`Tma` .

## Bollinger Band

<!-- markdownlint-disable MD034 -->

A Stock Chart overlay that shows the upper and lower limits of normal price movements based on the standard deviation of prices.
To render a Bollinger Band, use indicator [`Type`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Charts.StockChartStockChartIndicator.html#Syncfusion_EJ2_Charts_StockChartStockChartIndicator_Type) as `BollingerBand`.Bollinger band will be represented by three lines (upperLine, lowerLine, signalLine).(https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Charts.StockChartStockChartIndicator.html#Syncfusion_EJ2_Charts_StockChartStockChartIndicator_Type) and [`StandardDeviations`](https://help.syncfusion.com/cr/aspnetcore-js2/Syncfusion.EJ2.Charts.StockChartStockChartIndicator.html#Syncfusion_EJ2_Charts_StockChartStockChartIndicator_StandardDeviation) is 2.

{% aspTab template="stock-chart/stockchart-feature/indicator", sourceFiles="candle.cs" %}

{% endaspTab %}

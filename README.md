# TradePad Pro

TradePad Pro is an advanced forex trading tool developed by the Forex Robot Easy Team. It provides traders with a variety of functions to execute market orders, place limit and stop orders, and manage their trades effectively. 

For detailed reviews and trading results of this product, please visit [forexroboteasy.com](https://forexroboteasy.com/forex-robot-review/tradepad-pro-review-advanced-forex-trading-tool-with-real-time-alerts/).

## Installation

To use TradePad Pro, you need to import the necessary libraries by including the 'TradePadPro.mqh' file in your project.

## Usage

To start using TradePad Pro, you need to initialize it by calling the `Init()` function in the `OnInit()` event.

```cpp
void OnInit()
{
    tradePad.Init();
}
```

### Market Orders

TradePad Pro allows you to execute market orders to buy or sell a specified quantity of a currency pair.

```cpp
void MarketBuy(double quantity, string symbol)
{
    tradePad.MarketBuy(quantity, symbol);
}

void MarketSell(double quantity, string symbol)
{
    tradePad.MarketSell(quantity, symbol);
}
```

### Limit Orders

You can place limit orders to buy or sell a specified quantity of a currency pair at a specified price or better.

```cpp
void BuyLimit(double quantity, double price, string symbol)
{
    tradePad.BuyLimit(quantity, price, symbol);
}

void SellLimit(double quantity, double price, string symbol)
{
    tradePad.SellLimit(quantity, price, symbol);
}
```

### Stop Orders

TradePad Pro allows you to place stop orders to buy or sell a specified quantity of a currency pair at a specified price or better.

```cpp
void BuyStop(double quantity, double price, string symbol)
{
    tradePad.BuyStop(quantity, price, symbol);
}

void SellStop(double quantity, double price, string symbol)
{
    tradePad.SellStop(quantity, price, symbol);
}
```

### Pro Orders

In addition to the basic order functions, TradePad Pro also provides advanced order functions for professional traders.

```cpp
void ProSell(double quantity, double price, string symbol)
{
    tradePad.ProSell(quantity, price, symbol);
}

void ProBuy(double quantity, double price, string symbol)
{
    tradePad.ProBuy(quantity, price, symbol);
}
```

### Risk Management

TradePad Pro includes tools to assist traders in managing their daily losses and prevent further losses.

```cpp
void EquityDefenseTool(double maxLossLimit)
{
    tradePad.EquityDefenseTool(maxLossLimit);
}

void CloseOpenTrades()
{
    tradePad.CloseOpenTrades();
}

void PreventFurtherLosses()
{
    tradePad.PreventFurtherLosses();
}
```

## Trading Logic

The main program entry point is the `OnTick()` event, where you can implement your trading logic using the available functions.

```cpp
void OnTick()
{
    // TODO: Implement your trading logic here

    // Example usage of order functions
    MarketBuy(0.01, 'EURUSD');
    SellStop(0.02, 1.2000, 'GBPUSD');
    ProBuy(0.05, 1.5000, 'AUDUSD');

    // Example usage of advanced features
    EquityDefenseTool(1000.0);
    CloseOpenTrades();
    PreventFurtherLosses();
}
```

Please note that this code is a sample code provided by ForexRobotEasy, and they are not the official developers of TradePad Pro. To find the official developer and get the official version of the product, please refer to MQL5.

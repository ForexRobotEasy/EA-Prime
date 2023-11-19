# EA Prime

**EA Prime** is a fully automated multicurrency expert advisor designed for forex trading. It analyzes the market and determines the most probable direction of price movement based on long-term observations of market behavior. The strategy of EA Prime takes into consideration factors such as trend direction, current price levels, economic news, nearest round levels, and the size, body, and shadows of the signal candle.

## Expert Advisor Parameters

- **InpRiskPercent**: Risk percentage per trade
- **InpStopLoss**: Stop loss in pips
- **InpTakeProfit**: Take profit in pips
- **InpMaxSpread**: Maximum allowed spread in pips

## How it Works

The expert advisor calculates the lot size based on the account's free margin and the specified risk percentage per trade. It also calculates the stop loss and take profit levels in pips. The current spread is obtained using the `MarketInfo` function.

If the spread is less than or equal to the maximum allowed spread, the expert advisor checks the market direction using the `MarketInfo` function with the `MODE_DIRECTION` parameter. If the market direction is `MODE_BUY`, a buy order is sent with the specified lot size, ask price, stop loss level (bid - stop loss), and take profit level (bid + take profit). If the market direction is `MODE_SELL`, a sell order is sent with the specified lot size, bid price, stop loss level (ask + stop loss), and take profit level (ask - take profit).

Please note that this code is provided as a sample and is not the official implementation of EA Prime. To find the official developer of EA Prime, please refer to MQL5.

For more detailed reviews and trading results of this product, please visit [Forex Robot Easy](https://forexroboteasy.com/forex-robot-review/ea-prime-review-a-professional-forex-traders-perspective-on-this-multicurrency-expert-advisor/). ForexRobotEasy is not the official developer of this product, but we provide sample code that can work as described in this product.

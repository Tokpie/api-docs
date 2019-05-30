# TOKPIE API
#### Last updated on May 30, 2019

TOKPIE offers its users a FREE access to the Public API.
Public API does not require authorization and can be accessed using the GET method.

### Public API

This API does not require authorization and can be accessed using the GET method.
General URL with API access looks like this: https://tokpie.com/{api_name}/ where ‘api_name’ is the name of API you are accessing. Currently available API endpoints are described below..

### Method description:

**1. Live statistics on prices and volumes for all tickers.**

|                      |                                |
|----------------------|--------------------------------|
| Method name:         | ticker                         |
| Type of request:     | GET                            |
| Incoming parameters: | None                           |
| Call:                | https://tokpie.com/api_ticker/ 

#### Return information sample:

`…{
  "updated": "11.12.2018 22:00 UTC",
  "at_first24": "0.00000575",
  "pair": "TKP@ETH",
  "quoteVolume": "0.03449196",
  "high24hr": "0.0000058",
  "isFrozen": 0,
  "highestBid": "0.0000056",
  "percentChange": "0.87%",
  "low24hr": "0.0000056",
  "last": "0.0000058",
  "avg": "0.000005659893995832",
  "lowestAsk": "0.0000058",
  "id": 22,
  "baseVolume": "6094.10"
  }…`

#### Fields description:

**updated** – date and time of data update.

**at_first24** – the price of the first deal for the last 24 hours.

**pair** – unique combination of base and quote currencies or assets.

**quoteVolume** - the total quantity of quote currency or asset for all deals within the last 24 hours.

**high24hr** - maximum deal price within the last 24 hours.

**isFrozen** - indicator specifying whether the market is frozen where return “1” means the market is frozen.

**highestBid** - current maximum buy price.

**percentChange** - percentage change in price for the last 24 hours.

**low24hr** - minimum deal price within the last 24 hours.

**last** - last deal price.

**avg** - average deal price within the last 24 hours.

**lowestAsk** - current minimum sell price.

**id** - unique identification number for a trading pair or instrument.

**baseVolume** - the total quantity of base currency or asset for all deals within the last 24.    


**2. Live trading data, prices and volume for a specified ticker**

|                      |                                               |
|----------------------|-----------------------------------------------|
| Method name:         | ticker/market                                 |
| Type of request:     | GET                                           |
| Incoming parameters: | market example: OMG@ETH                       |
| Call:                | https://tokpie.com/api_ticker/?market=OMG@ETH |

#### Return information sample:

…{
    "is_ok": true, "result": {
    "updated": "30.05.2019 12:47 UTC",
    "at_first24": "0.00828541",
    "quoteVolume": "55.3715673852",
    "high24hr": "0.00864548",
    "isFrozen": 0,
    "highestBid": "0.0083513",
    "percentChange": "0.80%",
    "low24hr": "0.0082432",
    "pair": "OMG@ETH",
    "last": "0.0083513",
    "avg": "0.00844854079280071",
    "lowestAsk": "0.00837394",
    "id": 659,
    "baseVolume": "6553.98"
}}…

#### Fields description:

**updated** – date and time of data update.

**at_first24** – the price of the first deal for the last 24 hours.

**quoteVolume** - the total quantity of quote currency or asset for all deals within the last 24 hours.

**high24hr** - maximum deal price within the last 24 hours.

**isFrozen** - indicator specifying whether the market is frozen where return “1” means the market is frozen.

**highestBid** - current maximum buy price.

**percentChange** - percentage change in price for the last 24 hours.

**low24hr** - minimum deal price within the last 24 hours.

**pair**** – unique combination of base and quote currencies or assets.

**last** - last deal price.

**avg** - average deal price within the last 24 hours.

**lowestAsk** - current minimum sell price.

**id** - unique identification number for a trading pair or instrument.

**baseVolume** - the total quantity of base currency or asset for all deals within the last 24.

**3. Live order book data (market depth), prices and volume for a specified ticker**

|                      |                                                           |
|----------------------|-----------------------------------------------------------|
| Method name:         | order_book/market                                         |
| Type of request:     | GET                                                       |
| Incoming parameters: | market example: OMG@ETH, size Gear position 1-10          |
| Call:                | https://tokpie.com/api_order_book/?market=OMG@ETH&size=10 |

#### Return information sample:
…{
    "is_ok": true,
    "result": {
        "aob_bid": [
            [0.00871812, 40.0],
            [0.00852264, 177.0],
            [0.00850299, 231.0],
            [0.00840701, 238.0],
            [0.00837394, 103.0],
            [0.0083513, 47.0],
            [0.0082432, 82.0],
            [0.00819645, 144.0],
            [0.00814769, 286.0],
            [0.0081437, 221.0]
        ],
        "aob_datetime": "30.05.2019 13:02 UTC",
        "aob_ask": [
            [0.00922465, 111.0],
            [0.00917475, 83.0],
            [0.00915936, 106.0],
            [0.00912976, 83.0],
            [0.009092, 30.0],
            [0.0090821, 114.0],
            [0.0089919, 199.0],
            [0.00899181, 83.0],
            [0.0088142, 87.0],
            [0.0087542, 99.0]
        ]
    }
}…

#### Fields description:

**aob_bid** – Buyer depth [price, quantity]

**aob_datetime** – date and time of this depth

**aob_ask** – Seller depth [price, quantity]




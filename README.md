# TOKPIE API
#### Last updated on December 15, 2018

TOKPIE offers its users a FREE access to the Public API.
Public API does not require authorization and can be accessed using the GET method.

### Public API

This API does not require authorization and can be accessed using the GET method.
General URL with API access looks like this: https://tokpie.com/{api_name}/ where ‘api_name’ is the name of API you are accessing. Currently available API endpoint is https://tokpie.com/api_ticker/.

### Method description:
Statistics on prices and volume of all deals and pairs

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
   

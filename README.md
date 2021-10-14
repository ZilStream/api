# API Documentation

All ZilStream pairs consist of one ZRC-2 token paired to native ZIL.

The canonical address for native ZIL used by ZilStream is `zil1qqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqq9yf6pz`.

Results are cached for every block (~30 seconds).

## [`/pairs`](https://api.zilstream.com/pairs)

Returns data for all the registered pairs available on ZilStream.

### Request

`GET https://api.zilstream.com/pairs`

### Response

```json5
{
  "zil14pzuzq6v6pmmmrfjhczywguu0e97djepxt8g3e_zil1qqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqq9yf6pz": {
    "base_id": "zil14pzuzq6v6pmmmrfjhczywguu0e97djepxt8g3e",
    "base_name": "governance ZIL",
    "base_symbol": "gZIL",
    "quote_id": "zil1qqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqq9yf6pz",
    "quote_name": "Zilliqa",
    "quote_symbol": "ZIL",
    "last_price": "1587.2633348350996",
    "base_volume": "11851.148006908446",
    "quote_volume": "86902385.28982149"
  },
  // "": {...}
}
```

## [`/tokens`](https://api.zilstream.com/tokens)

Returns the tokens available on ZilStream.

### Request

`GET https://api.zilstream.com/tokens`

### Response

```json5
[
  {
    "id": 2,
    "created_at": "2021-03-05T10:37:32.147344Z",
    "updated_at": "2021-10-07T15:32:56.685019Z",
    "name": "governance ZIL",
    "symbol": "gZIL",
    "address_bech32": "zil14pzuzq6v6pmmmrfjhczywguu0e97djepxt8g3e",
    "icon": "https://meta.viewblock.io/ZIL.zil14pzuzq6v6pmmmrfjhczywguu0e97djepxt8g3e/logo",
    "decimals": 15,
    "website": "https://zilliqa.com",
    "telegram": "",
    "whitepaper": "",
    "init_supply": 0,
    "max_supply": 559970.1,
    "total_supply": 559970.0955408541,
    "current_supply": 559970.0955408541,
    "daily_volume": 18810892.707069844,
    "current_liquidity": 88008798.97599038,
    "liquidity_providers": 947,
    "supply_skip_addresses": "",
    "viewblock_score": 100,
    "unvetted": false,
    "bridged": false,
    "last_vote_start": "0001-01-01T00:00:00Z",
    "last_vote_end": "0001-01-01T00:00:00Z",
    "last_vote_hash": "",
    "rewards": []
  },
  // {...}
]
```

## [`/tokens/zil...`](https://api.zilstream.com/tokens/zil14pzuzq6v6pmmmrfjhczywguu0e97djepxt8g3e)

Returns the token information, based on address.

### Request

`GET https://api.zilstream.com/tokens/zil14pzuzq6v6pmmmrfjhczywguu0e97djepxt8g3e`

### Response

```json5
{
  "name": "governance ZIL",
  "symbol": "gZIL",
  "address_bech32": "zil14pzuzq6v6pmmmrfjhczywguu0e97djepxt8g3e",
  "icon": "https://meta.viewblock.io/ZIL.zil14pzuzq6v6pmmmrfjhczywguu0e97djepxt8g3e/logo",
  "decimals": 15,
  "website": "https://zilliqa.com",
  "telegram": "",
  "whitepaper": "",
  "viewblock_score": 100,
  "last_vote_start": "0001-01-01T00:00:00Z",
  "last_vote_end": "0001-01-01T00:00:00Z",
  "last_vote_hash": "",
  "listed": true,
  "bridged": false,
  "current_supply": 559970.0955408541,
  "daily_volume": 1837523.2431974108,
  "supply_skip_addresses": "",
  "market_cap": 86881701.82813317,
  "rate": 1588.3274792409086,
  "rate_usd": 155.15418148216892,
  "market_data": {
    "ath": 3134.3089316432006,
    "atl": 998.6055434069384,
    "change_24h": 72.5812560567806,
    "change_percentage_24h": 4.788483385055657,
    "change_percentage_7d": 9.700476751803931,
    "change_percentage_14d": 11.029482174748608,
    "change_percentage_30d": 18.31029206917975,
    "init_supply": 0,
    "max_supply": 559970.1,
    "total_supply": 559970.0955408541,
    "current_supply": 559970.0955408541,
    "daily_volume": 1837523.2431974108,
    "daily_volume_zil": 18810892.707069844,
    "market_cap": 86881701.82813317,
    "market_cap_zil": 889415890.3006957,
    "fully_diluted_valuation": 86881702.51998827,
    "fully_diluted_valuation_zil": 889415897.3832794,
    "current_liquidity": 8597051.519170646,
    "current_liquidity_zil": 88008798.97599038,
    "liquidity_providers": 947,
    "zil_reserve": 44004399.48799519,
    "token_reserve": 27704.86569244884
  },
  "rewards": []
}
```

## [`/orderbook`](https://api.zilstream.com/orderbook?address=zil1p5suryq6q647usxczale29cu3336hhp376c627&depth=100)

Returns the orderbook with depth of a given token address.

### Request

`GET https://api.zilstream.com/orderbook?address=zil1p5suryq6q647usxczale29cu3336hhp376c627&depth=100`

### Response

```json5
{
  "ticker_id": "ZWAP_ZIL",
  "ticker_address": "zil1p5suryq6q647usxczale29cu3336hhp376c627",
  "bids": [
    {
      "price": "578.0427532720807",
      "amount": "2.746322134693"
    },
    {
      "price": "578.03146578725",
      "amount": "0.157430875975"
    },
    {
      "price": "578.7271816962694",
      "amount": "60.499778063819"
    },
    // {...}
  ],
  "asks": [
    {
      "price": "574.5907132096601",
      "amount": "0.09999999999999999"
    },
    {
      "price": "574.56872073433",
      "amount": "0.09999999999999999"
    },
    {
      "price": "574.5980166537332",
      "amount": "7.27713042378"
    },
    // {...}
  ]
}
```

## [`/summary`](https://api.zilstream.com/summary)

Returns a summary overview of the available tokens.

### Request

`GET https://api.zilstream.com/summary`

### Response

```json5
[
  {
    "trading_pairs": "ZWAP_ZIL",
    "last_price": 40.693817570821096,
    "lowest_ask": 0,
    "highest_bid": 0,
    "base_volume": 230033.61559308716,
    "quote_volume": 3561034.846767968,
    "price_change_percent_24h": -3.480268008055469,
    "highest_price_24h": 42.35933444114199,
    "lowest_price_24h": 40.36596701543771
  },
  // {...}
]
```
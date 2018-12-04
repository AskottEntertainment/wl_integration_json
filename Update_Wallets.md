# Update Wallets

Allows ESP to update the wallet amount on the White Label site.

Request from ESP:

__Pretty printed__

```
{
  "data": [
    {
      "action": "join_pool",
      "amount": -0.25,
      "bet_id": "154395992711728480",
      "currency": "CNY",
      "user_id": 1,
      "wallet_id": "154395992929900896"
    }
  ],
  "timestamp": 1543959911
}
```

__Json sent across__

```
{"data":[{"action":"join_pool","amount":-0.25,"bet_id":"154395992711728480","currency":"CNY","user_id":1,"wallet_id":"154395992929900896"}],"timestamp":1543959911}
```

Secret Key used in the HMAC-sha512 `super_safe_private_key`

__HMAC Generated__  (Check against https://codebeautify.org/hmac-generator using HMAC-SHA512)

`a836eefcc945cd81722e83e309dd27a7e893a2a685fbb1fa2b34a8e18bbb90a233c9f23e0fc4ee3a427c76467adbd72e9c5310ee5826dd4b30e6baedcb9e9a82`

__Successful response__


```
{
  "results": [
    {
      "amount": 442.29,
      "wallet_id": "154396227169311360",
      "currency": "CNY",
      "result": true,
      "transaction_id": "unique_id"
    }
  ]
}
```


__Failed response__

```
{
  "results": [
    {
      "amount": 442.29,
      "wallet_id": "154396227169311360",
      "currency": "CNY",
      "result": false
    }
  ]
}
```
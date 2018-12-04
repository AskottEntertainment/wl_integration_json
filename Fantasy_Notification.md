# Fantasy Notification

Allows ESP to notify a user on a White Label site that a fantasy pool has opened it's fantasy picks or that the user has not make their fantasy picks and the fantasy pool is about to start.

Request from ESP:

__Pretty printed__

```
{
  "data": [
    {
      "bet_id": "154395992711728480",
      "user_id": 1
    }
  ],
  "type": "picks_open",
  "pool_name": "€0.25 SALARY POOL",
  "start_time": 1542895200,
  "timestamp": 1543959911
}
```

__Json sent across__

```
{"data":[{"bet_id":"154395992711728480","user_id":1}],"type":"picks_open","pool_name":"€0.25 SALARY POOL","start_time":1542895200,"timestamp":1543959911}
```

Secret Key used in the HMAC-sha512 `super_safe_private_key`

__HMAC Generated__  (Check against https://codebeautify.org/hmac-generator using HMAC-SHA512)

`a5d093a404c8f9e62cea354b39246245ea19f97aa5edefa2486c8942315fb7e3b39e9d9b0585b73655cb341eb5f197d2c09ace76ecda70ab214a5ba5f7de003e`

__Successful response__


```
{
  "results": true
}
```


__Failed response__

```
{
  "results": false
}
```
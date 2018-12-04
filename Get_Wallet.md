# Get Wallet

Allows ESP to get the current wallet amount from WL site.

Request from ESP:

__Pretty printed__

```
{
  "auth_token": "123123123",
  "timestamp": 1543959910,
  "user_id": 1,
}
```

__Json sent across__

```
{"auth_token":"123123123","timestamp":1543959910,"user_id":1}
```

Secret Key used in the HMAC-sha512 `super_safe_private_key`

__HMAC Generated__  (Check against https://codebeautify.org/hmac-generator using HMAC-SHA512)

`fd2282ab4c74c7ab9acc8c8c3ca955b6a6b90d375b6aaae688b5d14d90c0093de681c1664aea9408a623c3cd69fad7951ac5789c17dcf13124584b9b909096cd`

__Successful response__


```
{
  "user_id": 1,
  "amount": 443.54,
  "currency": "CNY"
}
```


__Failed response__

A none 200 should come back if it fails.
# Authentication Confirmation 

Sent from ESP to WL whenever we need to confirm that the user authenicated and can use ESP service.

Request from ESP:

__Pretty printed__

```
{
  "auth_token": "123123123",
  "client_id": 1,
  "timestamp": 1543876733
}
```

__Json sent across__

```
{"auth_token":"123123123","client_id":1,"timestamp":1543876733}
```

Secret Key used in the HMAC-sha512 `super_safe_private_key`

__HMAC Generated__  (Check against https://codebeautify.org/hmac-generator using HMAC-SHA512)

`472ac8f46f0cff06445fc9e537283e3015c6beb6c7b7c807a1676d051df43375105ade8e0dd1394b1f66d037635b2cc20f929ff6de34a836da92a3cb67d035d6`

__Successful authentication response__


```
{
  "username": "user1",
  "user_id": 1,
  "amount": 443.54,
  "currency": "CNY",
  "result": true
}
```


__Failed authentication response__

```
{"result":false}
```

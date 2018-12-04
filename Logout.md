# Logging a user out of ESP

White label sites when a user logs out of their site.

Request To ESP:

__Pretty printed__

```
{
  "user_id": 1,
  "timestamp": 1543959911
}
```

__Json sent across__

```
{"user_id":1,"timestamp":1543959911}
```

Secret Key used in the HMAC-sha512 `super_safe_private_key`

__HMAC Generated__  (Check against https://codebeautify.org/hmac-generator using HMAC-SHA512)

`06d28eae8c11c7bcc2dbcb1866148eb55284ac9780b797f8df750fac5f275f462d0dbf733628ce4b3942eb2d3f4849ccc6e6d562b8996725c1c0fabc7d332d02`

__Required HTTP headers__

```
X-Public = "public_key"
X-Hash = "06d28eae8c11c7bcc2dbcb1866148eb55284ac9780b797f8df750fac5f275f462d0dbf733628ce4b3942eb2d3f4849ccc6e6d562b8996725c1c0fabc7d332d02"
```

__Successful response__


```
{
  "result": true
}
```


__Failed response__

```
{
  "result": false
}

If the Hash was generated incorrectly a response code of 401 will be returned.
```
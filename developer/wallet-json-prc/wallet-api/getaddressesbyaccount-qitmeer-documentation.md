# getAddressesByAccount :: Qitmeer Documentation

#### wallet\_getAddressesByAccount <a href="#wallet_getaddressesbyaccount" id="wallet_getaddressesbyaccount"></a>

获取账户所有的地址

**Parameters**

1. `accountName: (string)` 账户名

**Returns**

**Example**

**Request**

```
{"jsonrpc":"1.0","method":"wallet_getAddressesByAccount","params":["default"],"id":1}
```

**Response**

```
{
    "jsonrpc": "2.0",
    "id": 1,
    "result": [
        "TmSbEJs3nDmy68Af7M4Rsuj4pyAwcAret5a",
        "Tmbzp2af9Ereh2hRejcVH9mCQgYdY2GHCAa",
        "TmZu8zU1i6xbZMpLQZLMAJsyWHanZXUZtiV"
    ]
}
```

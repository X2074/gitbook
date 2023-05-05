# getAccountByAddress :: Qitmeer Documentation

#### wallet\_getAccountByAddress <a href="#wallet_getaccountbyaddress" id="wallet_getaccountbyaddress"></a>

Get owner account name of address

**Parameters**

1. `addr: (string)` address

**Returns**

1. `account name: (string)` owner account name

**Example**

**Request**

```
 $ curl -sk -u "test:test" -X POST -H 'Content-Type: application/json' --data '{"jsonrpc":"1.0","method":"wallet_getAccountByAddress","params":["TmbC1Fx1UXNt7D6zpaj83UrAEW7MbcUWuQz"],"id":1}' http://127.0.0.1:8130/api |jq .

```

**Response**

```

{
  "jsonrpc": "2.0",
  "id": 1,
  "result": "test"
}


```

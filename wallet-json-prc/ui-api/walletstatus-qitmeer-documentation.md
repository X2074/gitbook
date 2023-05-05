# walletStatus :: Qitmeer Documentation

### ui\_walletStatus <a href="#ui_walletstatus" id="ui_walletstatus"></a>

wallet info

#### Parameters <a href="#parameters" id="parameters"></a>

#### Returns <a href="#returns" id="returns"></a>

**Success**

1. `status: (string)`
   1. err - error happened
   2. nil - wallet not exists
   3. closed - wallet closed
   4. lock - wallet locked
   5. unlock - wallet unlocked

#### Example <a href="#example" id="example"></a>

**Request**

```
curl -sku "test:test" -X POST -H 'Content-Type: application/json' --data '{"jsonrpc":"1.0","method":"ui_walletStatus","params":[],"id":1}' http://127.0.0.1:8130/api | jq

```

**Response**

```
{                                                                                                                                       
  "jsonrpc": "2.0",                                                                                                                     
  "id": 1,                                                                                                                              
  "result": {                                                                                                                           
    "stats": "lock"                                                                                                                     
  }                                                                                                                                     
}
```

# getBlockhash :: Qitmeer Documentation

#### getBlockhash <a href="#getblockhash" id="getblockhash"></a>

Returns hash of the block at the given order.

**Parameters**

1. block order (numeric, required)

**Returns**

* `(string)` block hash

**Example**

**Request**

```
 curl --data '{"method":"getBlockhash","params":[2],"jsonrpc":"2.0","id":1}' -s -k -u "rpcuser:rpcpass"  -H 'Content-Type: application/json' http://127.0.0.1:18131 |jq .
```

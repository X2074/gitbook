# tips :: Qitmeer Documentation

#### tips <a href="#tips" id="tips"></a>

None

**Parameters**

**Returns**

**`(array of string)` list of tip hashes**

**Example**

**Request**

```
 curl --data '{"method":"tips","params":[],"jsonrpc":"2.0","id":1}' -s -k -u "rpcuser:rpcpass"  -H 'Content-Type: application/json' http://127.0.0.1:18131 |jq . 
```

**Response**

```
[
  "00001a78e4405cf0b1eeebf4c707bbbeea3fbad53dd60718092b08c6fb1cb95f"
]
```

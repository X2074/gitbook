# importPrivKey :: Qitmeer Documentation

### ui\_importPrivKey <a href="#ui_importprivkey" id="ui_importprivkey"></a>

imports a private key to the wallet and writes the new wallet to disk.

**Note**: this private key is in a hex string and you may generate it with `qx wiftopriv` tool from a WIF key, which should be compatible with BTC network (in contrast to dumpPrivKey and importWIFPrivKey, both are incompatible). You may export this WIF key from any wallet service that follows this rule, such as [KAHF](https://kahf.io/)

#### Parameters <a href="#parameters" id="parameters"></a>

1. `accountName: (string)` name of the imported account. MUST be: “imported”
2. `privKey: (hex string)` private key.

#### Returns <a href="#returns" id="returns"></a>

**Success**

`null`

**Error**

`-32000 -4` imported addresses must belong to the imported account

#### Example <a href="#example" id="example"></a>

**Request**

```
curl --location --request POST 'http://127.0.0.1:8130/api/'  -u test:test -H 'Content-Type: application/json'  -d '{"id":1, "jsonrpc":"2.0","method":"wallet_importPrivKey","params":["imported", "9999999999999999999999999999999999999999999999999999999999999999"]}'
```

**Response**

```
{"jsonrpc":"2.0","id":1,"result":null}
```

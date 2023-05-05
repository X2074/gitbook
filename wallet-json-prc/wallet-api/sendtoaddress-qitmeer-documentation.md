# sendToAddress :: Qitmeer Documentation

### wallet\_sendToAddress <a href="#wallet_sendtoaddress" id="wallet_sendtoaddress"></a>

sends the passed amount to the given address.

#### NOTE <a href="#note" id="note"></a>

* This function requires to the wallet to be unlocked. See wallet\_unlock
* The amount cannot exceed 21,000,000

#### Parameters <a href="#parameters" id="parameters"></a>

1. `address: (hex string)` the given address
2. `amount: (numeric)` passed amount
3. `coinID: (numeric)` 0 => MEER 1=> MEER balance

#### Returns <a href="#returns" id="returns"></a>

**Success**

`TxID: (hex string)` the TxID for the created transaction

**Error**

`-32000` `-13` Enter the wallet passphrase with walletpassphrase first

#### Example <a href="#example" id="example"></a>

**Request**

```
$ curl -sk -u "test:test" -X POST -H 'Content-Type: application/json' --data '{"jsonrpc":"1.0","method":"wallet_sendToAddress","params":["Tmdcmmo7JqxxwHy6r46Sx2ZRbVF2dSjG9mm", 1 , 0],"id":1}' http://127.0.0.1:8130/api |jq .
```

**Response**

```
{
  "jsonrpc": "2.0",
  "id": 1,
  "result": "86140f1fa1e7d95707ec7e61748b91838e24a00ca8803f299c7caca591ff1af4"
}
```

**Request Send MEER To EVM**

```
$ curl -sk -u "test:test" -X POST -H 'Content-Type: application/json' --data '{"jsonrpc":"1.0","method":"wallet_sendToAddress","params":["Tk6uJDaurxqPrg2bZqBa9XSpUcakebZ6EU1u9qqHNDcNW2MyeTtbX", 10 , 1],"id":1}' http://127.0.0.1:8130/api |jq .
```

**Response**

```
{
  "jsonrpc": "2.0",
  "id": 1,
  "result": "86140f1fa1e7d95707ec7e61748b91838e24a00ca8803f299c7caca591ff1af4"
}
```

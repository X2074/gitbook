# unlock :: Qitmeer Documentation

### wallet\_unlock <a href="#wallet_unlock" id="wallet_unlock"></a>

unlocks the wallet’s address manager and relocks it after timeout has expired. If the wallet is already unlocked and the new passphrase is correct, the current timeout is replaced with the new one. The wallet will be locked if the passphrase is incorrect or any other error occurs during the unlock.

#### Parameters <a href="#parameters" id="parameters"></a>

1. `passphrase: (string)` wallet private password
2. `timeout: (numeric)`

* `negative` unlock indefinitely
* `postive` unlock duration, unit second

#### Returns <a href="#returns" id="returns"></a>

**Success**

**Error**

`-32000` invalid passphrase for master private key

#### Example <a href="#example" id="example"></a>

**Request**

```
curl -k -u "test:test" -X POST -H 'Content-Type: application/json' --data '{"jsonrpc":"1.0","method":"wallet_unlock","params":["password", 999999999],"id":1}' http://127.0.0.1:8130/api

```

**Response**

```
{"jsonrpc":"2.0","id":1,"result":null}
```

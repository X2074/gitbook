# createAccount :: Qitmeer Documentation

### wallet\_createAccount <a href="#wallet_createaccount" id="wallet_createaccount"></a>

creates the next account and returns its account number. The name must be unique to the account. In order to support automatic seed restoring, new accounts may not be created when all of the previous 100 accounts have no transaction history (this is a deviation from the BIP0044 spec, which allows no unused account gaps).

#### Parameters <a href="#parameters" id="parameters"></a>

1. `name: (string)` account name

#### Returns <a href="#returns" id="returns"></a>

**Success**

`null`

**Error**

`-32000 -13` Creating an account requires the wallet to be unlocked. Enter the wallet passphrase with walletpassphrase to unlock

#### Example <a href="#example" id="example"></a>

**Request**

```
curl -k -u "test:test" -X POST -H 'Content-Type: application/json' --data '{"jsonrpc":"1.0","method":"wallet_createAccount","params":["test_account"],"id":1}' http://127.0.0.1:8130/api
```

**Response**

```
{"jsonrpc":"2.0","id":1,"result":null}
```

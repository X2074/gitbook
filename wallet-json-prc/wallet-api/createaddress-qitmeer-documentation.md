# createAddress :: Qitmeer Documentation

### wallet\_createAddress <a href="#wallet_createaddress" id="wallet_createaddress"></a>

returns the next external chained address for a wallet.

#### Parameters <a href="#parameters" id="parameters"></a>

1. `accountName: (string)` name of the account on which the address created

#### Returns <a href="#returns" id="returns"></a>

#### Success <a href="#success" id="success"></a>

new address (base58)

#### Error <a href="#error" id="error"></a>

`-32000` account name ‘_test\_account_’ not found

#### Example <a href="#example" id="example"></a>

**Request**

```
curl -k -u "test:test" -X POST -H 'Content-Type: application/json' --data '{"jsonrpc":"1.0","method":"wallet_createAddress","params":["test_account"],"id":1}' http://127.0.0.1:8130/api
```

**Response**

```
{
  "jsonrpc": "2.0",
  "id": 1,
  "result": "Tmdy4W4FeDD2M8Tm8syZJmR2BPdug4Zeozj"
}

```

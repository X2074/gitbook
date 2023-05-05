# recoverWallet :: Qitmeer Documentation

### ui\_recoverWallet <a href="#ui_recoverwallet" id="ui_recoverwallet"></a>

Recover Wallet wallet by mnemonic

#### Parameters <a href="#parameters" id="parameters"></a>

1. `mnemonic: (hex string)` the mnemonic words
2. `walletPass: (string)` wallet password
3. `unlockPass: (string)` unlock password

#### Returns <a href="#returns" id="returns"></a>

**Success**

`null`

**Error**

`-32000`

1. seed hex err: Invalid menomic
2. wallet exist

#### Example <a href="#example" id="example"></a>

**Request**

```
curl -sku "test:test" -X POST -H 'Content-Type: application/json' --data '{"jsonrpc":"1.0","method":"ui_recoverWallet","params":["river immense robust crucial patrol kingdom trick enter jacket similar feed pitch juice focus ramp merry occur blast pepper case gentle left sea margin", "walletPass", "unlockPass"],"id":1}' http://127.0.0.1:8130/api | jq

```

**Response**

```
{
  "jsonrpc": "2.0",
  "id": 1,
  "result": null
}

```

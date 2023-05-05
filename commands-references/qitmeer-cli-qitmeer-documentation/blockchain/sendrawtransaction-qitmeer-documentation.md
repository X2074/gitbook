# sendRawTransaction :: Qitmeer Documentation

### sendRawTransaction <a href="#sendrawtransaction" id="sendrawtransaction"></a>

sendRawTransaction {sign\_raw\_tx} {allow\_high\_fee}; allow\_high\_fee: default false; send sing\_raw\_tx to network

#### Usage <a href="#usage" id="usage"></a>

```
qitmeer-cli sendRawTransaction [flags]
```

#### Alias <a href="#alias" id="alias"></a>

* sendrawtransaction
* SendRawTransaction
* sendRawTx
* sendrawtx
* SendRawTx

#### Examples <a href="#examples" id="examples"></a>

```

sendRawTransaction 0100000001ff5d53a7070fa9f0a9d12af729d2cbaf355ef1173c106a84cf9ef3a46bff03b202000000ffffffff01005504790a0000001976a914627777996288556166614462639988446255776688ac000000000000000001000000000000000000000000ffffffff6b483045022100dced4d67dd74647d0036077ee5b435838934377b1d296dd9da852772911e3be2022063dd346bd812a894968b8acacead7e7beff48947657a82f1e8f9c38876d4c905012103aba0a09f5b44138a46a2e5d26b8659923d84c4ba9437e22c3828cac43d0edb49

sendRawTransaction 0100000001ff5d53a7070fa9f0a9d12af729d2cbaf355ef1173c106a84cf9ef3a46bff03b202000000ffffffff01005504790a0000001976a914627777996288556166614462639988446255776688ac000000000000000001000000000000000000000000ffffffff6b483045022100dced4d67dd74647d0036077ee5b435838934377b1d296dd9da852772911e3be2022063dd346bd812a894968b8acacead7e7beff48947657a82f1e8f9c38876d4c905012103aba0a09f5b44138a46a2e5d26b8659923d84c4ba9437e22c3828cac43d0edb49 true
	
```

#### Options <a href="#options" id="options"></a>

```
  -h, --help   help for sendRawTransaction
```

#### SEE ALSO <a href="#see-also" id="see-also"></a>

* [qitmeer-cli blockChain](https://github.com/objemmanuel/docs/blob/master/commands-references/qitmeer-cli-qitmeer-documentation/blockchain/broken-reference/README.md)

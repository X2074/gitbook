# getUtxo :: Qitmeer Documentation

### getUtxo <a href="#getutxo" id="getutxo"></a>

getUtxo {tx\_hash} {vout} \[include\_mempool]; vout:index of the output; include\_mempool: default=true,include the mempool , get information about an unspent transaction output

#### Usage <a href="#usage" id="usage"></a>

```
qitmeer-cli getUtxo [flags]
```

#### Alias <a href="#alias" id="alias"></a>

* getutxo
* GetUtxo

#### Examples <a href="#examples" id="examples"></a>

```

getutxo a97cf4d67bbe5ce57d1d2f4fc18ae2ee19e1048cbb1a14d8d94273bfef83f371 0 true
	
```

#### Options <a href="#options" id="options"></a>

```
  -h, --help   help for getUtxo
```

#### SEE ALSO <a href="#see-also" id="see-also"></a>

* [qitmeer-cli blockChain](https://github.com/objemmanuel/docs/blob/master/commands-references/qitmeer-cli-qitmeer-documentation/blockchain/broken-reference/README.md)

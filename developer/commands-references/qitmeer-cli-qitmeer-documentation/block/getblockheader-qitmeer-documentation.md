# getBlockHeader :: Qitmeer Documentation

### getBlockHeader <a href="#getblockheader" id="getblockheader"></a>

getBlockHeader {number|hash} \[verbose];verbose:bool,show detail,defalut true; get block by number or hash

#### Usage <a href="#usage" id="usage"></a>

```
qitmeer-cli getBlockHeader [flags]
```

#### Alias <a href="#alias" id="alias"></a>

* getblockheader
* GetBlockHeader

#### Examples <a href="#examples" id="examples"></a>

```

getBlockHeader 100 false

getBlockHeader 100

getBlockHeader 000000e4c6b7f5b89827711d412957bfff5c51730df05c2eedd1352468313eca

getBlockHeader 000000e4c6b7f5b89827711d412957bfff5c51730df05c2eedd1352468313eca true
	
```

#### Options <a href="#options" id="options"></a>

```
  -h, --help   help for getBlockHeader
```

#### SEE ALSO <a href="#see-also" id="see-also"></a>

* [qitmeer-cli block](https://qitmeer.github.io/docs/en/reference/qitmeer-cli/block/)

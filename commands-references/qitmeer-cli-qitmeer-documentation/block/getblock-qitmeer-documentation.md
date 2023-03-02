# getBlock :: Qitmeer Documentation

### getBlock <a href="#getblock" id="getblock"></a>

getBlock {number|hash} \[verbose]; verbose: defalut true,show block detail,get block by number or hash

#### Usage <a href="#usage" id="usage"></a>

```
qitmeer-cli getBlock [flags]
```

#### Alias <a href="#alias" id="alias"></a>

* getblock
* GetBlock

#### Examples <a href="#examples" id="examples"></a>

```

getBlock 100 false

getBlock 100

getBlock 000000e4c6b7f5b89827711d412957bfff5c51730df05c2eedd1352468313eca

getBlock 000000e4c6b7f5b89827711d412957bfff5c51730df05c2eedd1352468313eca true
	
```

#### Options <a href="#options" id="options"></a>

```
  -h, --help   help for getBlock
```

#### SEE ALSO <a href="#see-also" id="see-also"></a>

* [qitmeer-cli block](https://qitmeer.github.io/docs/en/reference/qitmeer-cli/block/)

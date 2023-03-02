# getBlockHashByRange :: Qitmeer Documentation

### getBlockHashByRange <a href="#getblockhashbyrange" id="getblockhashbyrange"></a>

getBlockHashByRange {start} {end};Return the hash range of block from ‘start’ to ‘end’(exclude self)

#### Usage <a href="#usage" id="usage"></a>

```
qitmeer-cli getBlockHashByRange [flags]
```

```
getBlockHashByRange {start} {end};Return the hash range of block from 'start' to 'end'(exclude self)
if 'end' is equal to zero, 'start' is the number that from the last block to the Gen
if 'start' is greater than or equal to 'end', it will just return the hash of 'start'
```

#### Alias <a href="#alias" id="alias"></a>

* getblockhashbyrange
* GetBlockHashByRange
* getBlockhashByRange
* gethash

#### Examples <a href="#examples" id="examples"></a>

```

getBlockHashByRange 5 22
	
```

#### Options <a href="#options" id="options"></a>

```
  -h, --help   help for getBlockHashByRange
```

#### SEE ALSO <a href="#see-also" id="see-also"></a>

* [qitmeer-cli block](https://qitmeer.github.io/docs/en/reference/qitmeer-cli/block/)

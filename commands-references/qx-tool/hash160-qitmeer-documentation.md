# hash160 :: Qitmeer Documentation

calculate ripemd160( blake2b256( data ) )

```
~ qx hash160 --help

Usage: qx hash160 [hexstring]
```

**Example**

```
~ qx hash160 900df00d

a7a99d5c4c2b55f876010dd12f6733c99f1e9c1a
```

Is equivalent to the following example

```
~ qx blake2b256 900df00d | qx ripemd160

a7a99d5c4c2b55f876010dd12f6733c99f1e9c1a
```

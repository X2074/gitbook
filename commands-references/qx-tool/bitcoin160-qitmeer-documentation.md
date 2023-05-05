# bitcoin160 :: Qitmeer Documentation

calculate ripemd160( sha256( data ) )

```
~ qx bitcoin160 --help

Usage: qx bitcoin160 [hexstring]
```

**Example**

```
~ qx bitcoin160 900df00d

49f180cdaa4c6564f74a0b0321633bbcba4ef9c5
```

Is equivalent to the following example

```
~ qx sha256 900df00d | qx ripemd160

49f180cdaa4c6564f74a0b0321633bbcba4ef9c5
```

# blake hash :: Qitmeer Documentation

Perform a **blake2b256** or **blake2b512** or **blake256** of Base16 data.

#### blake2b256 <a href="#blake2b256" id="blake2b256"></a>

calculate Blake2b 256 hash of a base16 data.

```
~ qx blake2b256 --help

Usage: qx blak2b256 [hexstring]
```

**Example**

```
~ qx blake2b256 900df00d

c2cb5ef4138047b1ca42ce0bed2a2ce7d23768341ff52e6a9e2516257a1d2af9
```

***

#### blake2b512 <a href="#blake2b512" id="blake2b512"></a>

calculate Blake2b 512 hash of a base16 data.

```
~ qx blake2b512 --help

Usage: qx blake2b512 [hexstring]
```

**Example 1**

```
~ qx blake2b512 900df00d

36b65c58935fcf08307da04ba74bef658958e16a864c6a1a7bcec8fe5a82322f7c06424b70a4f25efc7e6493395562e6bebbe90e41c372dfda948506c54e4cdc
```

***

#### blake256 <a href="#blake256" id="blake256"></a>

calculate blake256 hash of a base16 data.

```
~ qx blake256 --help

Usage: qx blake256 [hexstring]
```

**Example 2**

```
~ qx blake256 900df00d

bedb342806616f3866179dab458f5f8a29bac652142689bf59a34136bc8e6d69
```

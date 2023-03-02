# EC :: Qitmeer Documentation

#### ec-new <a href="#ec-new" id="ec-new"></a>

create a new EC private key from an entropy (seed).

```
~ qx ec-new --help

Usage: qx ec-new [entropy]  
    -c string
       the elliptic curve is using (default "secp256k1")
```

**use secp256k1**

```
~ qx ec-new 4ec6a3a135aba433b0d0ae5ec31d69c26eb3bd5ac532496529660f61c674d99e

3f2314d615696244ea14e46e43322842b3e09333e62c59c4160220a52bdf6239
```

Currently only secp256k1 is supported.

***

#### ec-to-public <a href="#ec-to-public" id="ec-to-public"></a>

derive the EC public key from an EC private key (the compressed format by default ).

```
~ qx ec-to-public --help

Usage: qx ec-to-public [ec_private_key]
    -u    using the uncompressed public key format
```

**compressed**

```
~ qx ec-to-public 3f2314d615696244ea14e46e43322842b3e09333e62c59c4160220a52bdf6239

034d09a78b756b80e02200a94d2e24762432518fb29a4a3fd0adf0414e71554d70
```

**uncompressed**

```
~ qx ec-to-public -u 3f2314d615696244ea14e46e43322842b3e09333e62c59c4160220a52bdf6239

044d09a78b756b80e02200a94d2e24762432518fb29a4a3fd0adf0414e71554d701df9f31658a5578a8ded7ef2c681033ce0037823f3ed308c06ae7b1b06ce070f
```

***

#### ec-to-wif <a href="#ec-to-wif" id="ec-to-wif"></a>

convert an EC private key to a WIF, associates with the compressed public key by default.

```
~ qx ec-to-wif --help

Usage: qx ec-to-wif [ec_private_key]
    -u    using the uncompressed public key format
```

**wif compressed**

```
~ qx ec-to-wif 3f2314d615696244ea14e46e43322842b3e09333e62c59c4160220a52bdf6239

KyLSXswbDdBfrJoN6nPc8kPZJHEF5cBYey7f77dfnTFwGVEw1XGQ
```

**wif uncompressed**

```
~ qx ec-to-wif -u 3f2314d615696244ea14e46e43322842b3e09333e62c59c4160220a52bdf6239

5JJ6LEMXQhpjLKzBDe23XJXwSfZuafnSJDG6v3QiQtiStcHbZYA
```

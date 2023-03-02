# base64 :: Qitmeer Documentation

#### base64-encode <a href="#base64-encode" id="base64-encode"></a>

Convert a base16 string to a base64 string.

```
~ qx base64-encode --help

Usage: qx base64-encode [hexstring]
```

**Example 1**

```
~ qx base64-encode 1234567890abcdef

# base64 string
EjRWeJCrze8=
```

***

#### base64-decode <a href="#base64-decode" id="base64-decode"></a>

Convert a base64 string to a base16 string.

```
~ qx base64-decode --help

Usage: qx base64-decode [hexstring]
```

**Example 2**

```
~ qx base64-decode EjRWeJCrze8=

# base16 string
1234567890abcdef
```

# mnemonic :: Qitmeer Documentation

#### mnemonic-new <a href="#mnemonic-new" id="mnemonic-new"></a>

create a mnemonic world-list (BIP39) from an entropy.

```
~ qx mnemonic-new --help

Usage: qx mnemonic-new [entropy]
```

**Example**

```
~ qx mnemonic-new 4ec6a3a135aba433b0d0ae5ec31d69c26eb3bd5ac532496529660f61c674d99e

excite crush tribe hero ripple border select beyond gain body foil luggage twenty team help play enact citizen flower burst broccoli denial grid spike
```

***

#### mnemonic-to-entropy <a href="#mnemonic-to-entropy" id="mnemonic-to-entropy"></a>

return back to the entropy (the random seed) from a mnemonic world list (BIP39).

```
~ qx mnemonic-to-entropy --help

Usage: qx mnemonic-to-entropy [mnemonic]
```

**Example 1**

```
~ qx mnemonic-to-entropy 'excite crush tribe hero ripple border select beyond gain body foil luggage twenty team help play enact citizen flower burst broccoli denial grid spike'

4ec6a3a135aba433b0d0ae5ec31d69c26eb3bd5ac532496529660f61c674d99e
```

***

#### mnemonic-to-seed <a href="#mnemonic-to-seed" id="mnemonic-to-seed"></a>

convert a mnemonic world-list (BIP39) to its 512 bits seed.

```
~ qx mnemonic-to-seed --help

Usage: qx mnemonic-to-seed [mnemonic]  
    -p string
        An optional passphrase for converting the mnemonic to a seed
```

**Example 2**

```
~ qx mnemonic-to-seed 'excite crush tribe hero ripple border select beyond gain body foil luggage twenty team help play enact citizen flower burst broccoli denial grid spike'

5ccb173392641a7e5edc8d5f30e5ce314aada7f0b8e1169c2b67f81e80b5d95504629aabcd108264e0a16f03a9146f75552f37ed33cce16b9b4bf279b5df96a0
```

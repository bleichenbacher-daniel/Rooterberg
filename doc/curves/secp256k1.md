# secp256k1

| Attribute | Value |
| --- | --- |
| type | WeierstrassCurve |
| p | 0xfffffffffffffffffffffffffffffffffffffffffffffffffffffffefffffc2f |
| a | 0x0 |
| b | 0x7 |
| n | 0xfffffffffffffffffffffffffffffffebaaedce6af48a03bbfd25e8cd0364141 |
| h | 1 |
| g.x | 0x79be667ef9dcbbac55a06295ce870b07029bfcdb2dce28d959f2815b16f81798 |
| g.y | 0x483ada7726a3c4655da4fbfc0e1108a8fd17b448a68554199c47d08ffb10d4b8 |

## Tests

| Library | Ecdh | Ecdsa | HdKeyDerive | Schnorr | Other |
| --- | --- | --- | --- | --- | --- |
| @bitcoin-js/tiny-secp256k1-asmjs | | x | | x | |
| @noble/curves | x | x | | x | |
| @polkadot/wasm-crypto | | x | | | |
| @scure/bip32 | | | x | | |
| @secure/bip32 | | | x | | |
| AmazonCorrettoCryptoProvider | x | x | | | |
| BC | x | x | | | |
| BC_CSHARP | x | x | | | |
| SC | x | x | | | |
| bip32 | | | x | | |
| bitcoinjs-lib-v5 | | x | | | |
| botan | | x | | | |
| browserify-sign | | x | | | |
| crypto-browserify | x | x | | | |
| ecdsa | x | x | | | |
| elliptic | x | x | | | |
| k256 | x | x | | x | x |
| node.js | x | x | | | |
| pyca | x | x | | | |
| secp256k1 | x | x | | | |
| sjcl | x | x | | | |
| tiny-secp256k1 | | x | | x | |

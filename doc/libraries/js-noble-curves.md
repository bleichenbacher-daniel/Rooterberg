# @noble/curves

**Language:**
javascript\
**Url:**
[https://github.com/paulmillr/noble-curves](https://github.com/paulmillr/noble-curves)

## Performed tests

### Xdh

| primitive | encoding |
| --- | --- |
| x25519 | RAW |
| x448 | RAW |

### EcdsaVerify

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | secp256k1, secp256r1, secp384r1, secp521r1 | KECCAK256, SHA-256, SHA-384, SHA-512, SHA-512/256, SHA3-256, SHA3-384, SHA3-512 | DER, P1363 | False, True | Generic |

### EcdsaSign

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | secp256k1, secp256r1, secp384r1, secp521r1 | SHA-256, SHA-384, SHA-512 | DER | False, True | Rfc6979 |

### EddsaVerify

| primitive | curve | cofactored | encoding |
| --- | --- | --- | --- |
| Eddsa | edwards25519 | False | RAW |

### EddsaSign

| primitive | curve | cofactored | encoding |
| --- | --- | --- | --- |
| Eddsa | edwards25519 | False | RAW |

### SchnorrVerify

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Schnorr | secp256k1 | SHA-256 | BIP340 | True | Generic |

### SchnorrSign

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Schnorr | secp256k1 | SHA-256 | BIP340 | True | BIP340 |

### Ecdh

| primitive | curve | encoding |
| --- | --- | --- |
| Ecdh | secp256k1, secp256r1, secp384r1, secp521r1 | UNCOMPRESSED |

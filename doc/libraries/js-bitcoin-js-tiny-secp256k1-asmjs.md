# @bitcoin-js/tiny-secp256k1-asmjs

**Language:**
javascript\
**Url:**
[https://www.npmjs.com/package/@bitcoin-js/tiny-secp256k1-asmjs](https://www.npmjs.com/package/@bitcoin-js/tiny-secp256k1-asmjs)

## Performed tests

### EcdsaVerify

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | secp256k1 | SHA-256 | P1363 | False, True | Generic |

### EcdsaSign

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | secp256k1 | SHA-256 | P1363 | True | Rfc6979 |

### SchnorrVerify

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Schnorr | secp256k1 | SHA-256 | BIP340 | True | Generic |

### SchnorrSign

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Schnorr | secp256k1 | SHA-256 | BIP340 | True | BIP340 |

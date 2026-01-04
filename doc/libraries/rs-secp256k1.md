# secp256k1

**Language:**
rust\
**Url:**
[https://docs.rs/secp256k1/latest/secp256k1/](https://docs.rs/secp256k1/latest/secp256k1/)\
**Tested version:**
0.27.0, 0.31.1

## Performed tests

### EcdsaVerify

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | secp256k1 | SHA-256 | P1363 | True | Generic |

### EcdsaSign

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | secp256k1 | SHA-256 | P1363 | True | Rfc6979 |

### Ecdh

| primitive | curve | encoding |
| --- | --- | --- |
| Ecdh | secp256k1 | COMPRESSED |

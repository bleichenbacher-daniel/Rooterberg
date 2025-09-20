# secp256k1

**Language:**
javascript\
**Url:**
[https://www.npmjs.com/package/secp256k1](https://www.npmjs.com/package/secp256k1)\
**Tested version:**
5.0.1

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

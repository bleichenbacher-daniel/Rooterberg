# crypto.subtle

**Language:**
javascript\
**Url:**
[https://www.w3.org/TR/2017/REC-WebCryptoAPI-20170126/](https://www.w3.org/TR/2017/REC-WebCryptoAPI-20170126/)

crypto.subtle is an interface and has many independent implementations.
Currently, all tests run against the version built into node.

## Performed tests

### Xdh

| primitive | curve | encoding |
| --- | --- | --- |
| x25519 | curve25519 | DER |

### Aead

| primitive | keySize | ivSize | tagSize |
| --- | --- | --- | --- |
| AesGcm | 128, 192, 256 | 96, 128, 256 | 96, 128 |

### EcdsaVerify

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | secp256r1, secp384r1, secp521r1 | SHA-256, SHA-384, SHA-512 | JWK | False | Generic |

### EddsaVerify

| primitive | curve | cofactored | encoding |
| --- | --- | --- | --- |
| Eddsa | edwards25519 | False | JWK |

### Ecdh

| primitive | curve | encoding |
| --- | --- | --- |
| Ecdh | secp256r1, secp384r1, secp521r1 | DER, JWK |

### RsaPkcs1Verify

| primitive | size | sha | encoding |
| --- | --- | --- | --- |
| RsaSsaPkcs1 | 1024, 1536, 2048, 3072, 4096 | SHA-1, SHA-256, SHA-384, SHA-512 | DER |

### RsaPssVerify

| primitive | size | sha | mgf | mgfSha | saltLen | encoding |
| --- | --- | --- | --- | --- | --- | --- |
| RsaSsaPss | 1024, 1536, 2048, 3072, 4096 | SHA-1, SHA-256, SHA-384, SHA-512 | MGF1 | SHA-1, SHA-256, SHA-384, SHA-512 | 0, 20, 32, 48, 64 | DER |

### RsaEsOaepDecrypt

| primitive | size | sha | mgf | mgfSha |
| --- | --- | --- | --- | --- |
| RsaEsOaep | 1024, 2048, 3072, 4096 | SHA-1, SHA-256, SHA-384, SHA-512 | MGF1 | SHA-1, SHA-256, SHA-384, SHA-512 |

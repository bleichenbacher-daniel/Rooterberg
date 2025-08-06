# node.js

**Language:**
javascript\
**Url:**
[https://nodejs.org/api/crypto.html](https://nodejs.org/api/crypto.html)

## Performed tests

### Aead

| primitive | keySize | ivSize | tagSize |
| --- | --- | --- | --- |
| Chacha20Poly1305 | 256 | 96 | 128 |
| AesGcm | 128, 192, 256 | 64, 96, 128, 256 | 64, 96, 128 |
| AriaGcm | 128, 192, 256 | 96 | 128 |
| AesCcm | 128, 192, 256 | 88, 96, 104 | 64, 96, 128 |
| AriaCcm | 128, 192, 256 | 96, 104 | 64, 128 |
| AesOcb | 128, 192, 256 | 96, 120 | 128 |

### IndCpa

| primitive | keySize | ivSize | cipher | mode | padding | paddingSize | feedback |
| --- | --- | --- | --- | --- | --- | --- | --- |
| AesXts | 256, 512 | 128 | Aes | Xts | | | |
| AesCbcPkcs7 | 128, 192, 256 | 128 | Aes | Cbc | Pkcs7 | 128 | |
| AriaCbcPkcs7 | 128, 192, 256 | 128 | Aria | Cbc | Pkcs7 | 128 | |
| CamelliaCbcPkcs7 | 128, 192, 256 | 128 | Camellia | Cbc | Pkcs7 | 128 | |
| Sm4CbcPkcs7 | 128 | 128 | SM4 | Cbc | Pkcs7 | 128 | |
| AesCfb8 | 128, 192, 256 | 128 | Aes | Cfb | | | 8 |
| AesCfb128 | 128, 192, 256 | 128 | Aes | Cfb | | | 128 |
| AriaCfb8 | 128, 192, 256 | 128 | Aria | Cfb | | | 8 |
| AriaCfb128 | 128, 192, 256 | 128 | Aria | Cfb | | | 128 |
| CamelliaCfb8 | 128, 192, 256 | 128 | Camellia | Cfb | | | 8 |
| CamelliaCfb128 | 128, 192, 256 | 128 | Camellia | Cfb | | | 128 |
| Sm4Cfb128 | 128 | 128 | SM4 | Cfb | | | 128 |
| AesOfb | 128, 192, 256 | 128 | Aes | Ofb | | | |
| AriaOfb | 128, 192, 256 | 128 | Aria | Ofb | | | |
| CamelliaOfb | 128, 192, 256 | 128 | Camellia | Ofb | | | |
| Sm4Ofb | 128 | 128 | SM4 | Ofb | | | |

### EcdsaVerify

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | brainpoolP256r1, brainpoolP256t1, brainpoolP320r1, brainpoolP320t1, brainpoolP384r1, brainpoolP384t1, brainpoolP512r1, brainpoolP512t1, prime192v2, prime239v1, secp160r1, secp192k1, secp192r1, secp224k1, secp224r1, secp256k1, secp256r1, secp384r1, secp521r1 | SHA-224, SHA-256, SHA-384, SHA-512, SHA3-256, SHA3-384, SHA3-512 | DER, JWK, P1363 | False, True | Generic |

### Ecdh

| primitive | curve | encoding |
| --- | --- | --- |
| Ecdh | brainpoolP224r1, brainpoolP224t1, brainpoolP256r1, brainpoolP256t1, brainpoolP320r1, brainpoolP320t1, brainpoolP384r1, brainpoolP384t1, brainpoolP512r1, brainpoolP512t1, secp160r1, secp192r1, secp224r1, secp256k1, secp256r1, secp384r1, secp521r1, sm2 | UNCOMPRESSED |

### KeyWrap

| primitive | keySize |
| --- | --- |
| AesKw | 128, 192, 256 |

### Pbkdf

| primitive | sha |
| --- | --- |
| Pbkdf | SHA-1, SHA-224, SHA-256, SHA-384, SHA-512, SHA3-224, SHA3-256, SHA3-384, SHA3-512 |

### Hkdf

| primitive | sha |
| --- | --- |
| HkdfSha1 | SHA-1 |
| HkdfSha224 | SHA-224 |
| HkdfSha256 | SHA-256 |
| HkdfSha384 | SHA-384 |
| HkdfSha512 | SHA-512 |
| HkdfSha3_224 | SHA3-224 |
| HkdfSha3_256 | SHA3-256 |
| HkdfSha3_384 | SHA3-384 |
| HkdfSha3_512 | SHA3-512 |

### Pkcs8Decrypt

| primitive | sha | cipher |
| --- | --- | --- |
| Pkcs8 | SHA-1, SHA-256 | AES-CBC-128, AES-CBC-192, AES-CBC-256, AES-CFB-128, AES-CFB-192, AES-CFB-256, AES-OFB-128, AES-OFB-192, AES-OFB-256, DES-EDE3-CBC |
| Pkcs8Scrypt | | AES-CBC-128, AES-CBC-192, AES-CBC-256 |

### RsaPkcs1Verify

| primitive | size | sha | encoding |
| --- | --- | --- | --- |
| RsaSsaPkcs1 | 1024, 1536, 2048, 3072, 4096 | SHA-224, SHA-256, SHA-384, SHA-512, SHA3-256, SHA3-384, SHA3-512 | DER |

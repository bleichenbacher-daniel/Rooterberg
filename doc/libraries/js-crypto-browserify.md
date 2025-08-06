# crypto-browserify

**Language:**
javascript\
**Url:**
[https://www.npmjs.com/package/crypto-browserify](https://www.npmjs.com/package/crypto-browserify)

crypto-browserify is a reimplementation of the cryptographic library in node.js.
Using the same interface as node.js simplifies porting implementations from one library to the other.

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
| Ecdsa | secp192r1, secp224r1, secp256k1, secp256r1, secp384r1, secp521r1 | SHA-224, SHA-256, SHA-384, SHA-512 | DER | False | Generic |

### Ecdh

| primitive | curve | encoding |
| --- | --- | --- |
| Ecdh | secp160r1, secp192r1, secp224r1, secp256k1, secp256r1, secp384r1, secp521r1 | UNCOMPRESSED |

### KeyWrap

| primitive | keySize |
| --- | --- |
| AesKw | 128, 192, 256 |

### Pbkdf

| primitive | sha |
| --- | --- |
| Pbkdf | SHA-1, SHA-224, SHA-256, SHA-384, SHA-512, SHA3-224, SHA3-256, SHA3-384, SHA3-512 |

### RsaPkcs1Verify

| primitive | size | sha | encoding |
| --- | --- | --- | --- |
| RsaSsaPkcs1 | 1024, 1536, 2048, 3072, 4096 | SHA-1, SHA-224, SHA-256, SHA-384, SHA-512 | DER |

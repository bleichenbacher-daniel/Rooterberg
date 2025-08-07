# CryptoSwift

**Language:**
swift\
**Url:**
[https://github.com/krzyzanowskim/CryptoSwift](https://github.com/krzyzanowskim/CryptoSwift)

CryptoSwift is a cryptographic library that focusses on symmetric primitives.

## Performed tests

### Aead

| primitive | keySize | ivSize | tagSize |
| --- | --- | --- | --- |
| Chacha20Poly1305 | 256 | 96 | 128 |
| XChacha20Poly1305 | 256 | 192 | 128 |
| AesGcm | 128, 192, 256 | 96 | 96, 128 |
| AesOcb | 128, 192, 256 | 96, 120 | 128 |

### IndCpa

| primitive | keySize | ivSize | cipher | mode | padding | paddingSize | feedback | byteOrder |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| AesCbcPkcs7 | 128, 192, 256 | 128 | Aes | Cbc | Pkcs7 | 128 | | |
| AesCfb8 | 128, 192, 256 | 128 | Aes | Cfb | | | 8 | |
| AesCfb128 | 128, 192, 256 | 128 | Aes | Cfb | | | 128 | |
| AesOfb | 128, 192, 256 | 128 | Aes | Ofb | | | | |
| AesPcbcPkcs7 | 128, 192, 256 | 128 | Aes | Pcbc | Pkcs7 | 128 | | |
| RabbitBigEndian | 128 | 64 | Rabbit | | | | | big |

### Mac

| primitive | keySize | macSize |
| --- | --- | --- |
| AesCmac | 128, 192, 256 | 128 |
| HmacSha256 | | 256 |
| HmacSha384 | | 384 |
| HmacSha512 | | 512 |
| HmacSha3_256 | | 256 |
| HmacSha3_384 | | 384 |
| HmacSha3_512 | | 512 |

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

### RsaPkcs1Verify

| primitive | size | sha | encoding |
| --- | --- | --- | --- |
| RsaSsaPkcs1 | 2048, 3072, 4096 | SHA-224, SHA-256, SHA-384, SHA-512, SHA3-256, SHA3-384, SHA3-512 | DER |

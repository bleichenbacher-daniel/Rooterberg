# SunJCE

**Language:**
java\
**Url:**
[https://docs.oracle.com/en/java/javase/24/security/oracle-providers.html](https://docs.oracle.com/en/java/javase/24/security/oracle-providers.html)\
**Tested version:**
21

## Performed tests

### Aead

| primitive | keySize | ivSize | tagSize |
| --- | --- | --- | --- |
| Chacha20Poly1305 | 256 | 96 | 128 |
| AesGcm | 128, 192, 256 | 64, 96, 128, 256 | 96, 128 |

### IndCpa

| primitive | keySize | ivSize | cipher | mode | padding | paddingSize | feedback |
| --- | --- | --- | --- | --- | --- | --- | --- |
| AesCbcPkcs7 | 128, 192, 256 | 128 | Aes | Cbc | Pkcs7 | 128 | |
| TripleDesCbcPkcs7 | 192 | 64 | TripleDes | Cbc | Pkcs7 | 64 | |
| AesCfb8 | 128, 192, 256 | 128 | Aes | Cfb | | | 8 |
| AesCfb128 | 128, 192, 256 | 128 | Aes | Cfb | | | 128 |
| AesCfb128Pkcs7 | 128, 192, 256 | 128 | Aes | Cfb | Pkcs7 | 128 | 128 |
| TripleDesCfb8 | 192 | 64 | TripleDes | Cfb | | | 8 |
| TripleDesCfb64 | 192 | 64 | TripleDes | Cfb | | | 64 |
| AesOfb | 128, 192, 256 | 128 | Aes | Ofb | | | |
| TripleDesOfb | 192 | 64 | TripleDes | Ofb | | | |
| AesPcbcPkcs7 | 128, 192, 256 | 128 | Aes | Pcbc | Pkcs7 | 128 | |

### BlockCipher

| primitive | keySize |
| --- | --- |
| Aes | 128, 192, 256 |
| Des | 64 |
| TripleDes | 192 |

### KeyWrap

| primitive | keySize |
| --- | --- |
| AesKw | 128, 192, 256 |
| AesKwp | 128, 192, 256 |
| AesKwPkcs7 | 128, 192, 256 |

### Mac

| primitive | macSize |
| --- | --- |
| HmacSha1 | 160 |
| HmacSha224 | 224 |
| HmacSha256 | 256 |
| HmacSha384 | 384 |
| HmacSha512 | 512 |
| HmacSha512_224 | 224 |
| HmacSha512_256 | 256 |
| HmacSha3_224 | 224 |
| HmacSha3_256 | 256 |
| HmacSha3_384 | 384 |
| HmacSha3_512 | 512 |

### Pbkdf

| primitive | sha |
| --- | --- |
| Pbkdf | SHA-1, SHA-224, SHA-256, SHA-384, SHA-512 |

### Pbes2

| primitive | sha | cipher | keySize |
| --- | --- | --- | --- |
| Pbes2 | SHA-1, SHA-224, SHA-256, SHA-384, SHA-512, SHA-512/224, SHA-512/256 | Aes | 128, 256 |

### RsaEsPkcs1Decrypt

| primitive | size |
| --- | --- |
| RsaEsPkcs1 | 1024, 2048, 3072, 4096 |

### RsaEsOaepDecrypt

| primitive | size | sha | mgf | mgfSha |
| --- | --- | --- | --- | --- |
| RsaEsOaep | 1024, 2048, 3072, 4096 | SHA-1, SHA-224, SHA-256, SHA-384, SHA-512, SHA3-224, SHA3-256, SHA3-384, SHA3-512 | MGF1 | SHA-1, SHA-224, SHA-256, SHA-384, SHA-512, SHA3-224, SHA3-256, SHA3-384, SHA3-512 |

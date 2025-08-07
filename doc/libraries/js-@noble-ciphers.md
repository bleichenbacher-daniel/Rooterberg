# @noble/ciphers

**Language:**
javascript\
**Url:**
[https://github.com/paulmillr/noble-ciphers](https://github.com/paulmillr/noble-ciphers)

## Performed tests

### Aead

| primitive | keySize | ivSize | tagSize |
| --- | --- | --- | --- |
| Chacha20Poly1305 | 256 | 96 | 128 |
| XChacha20Poly1305 | 256 | 192 | 128 |
| AesGcm | 128, 192, 256 | 64, 96, 128, 256 | 128 |
| AesGcmSiv | 128, 256 | 96 | 128 |

### IndCpa

| primitive | keySize | ivSize | cipher | mode | padding | paddingSize | feedback |
| --- | --- | --- | --- | --- | --- | --- | --- |
| AesCbcPkcs7 | 128, 192, 256 | 128 | Aes | Cbc | Pkcs7 | 128 | |
| AesCfb128 | 128, 192, 256 | 128 | Aes | Cfb | | | 128 |

### KeyWrap

| primitive | keySize |
| --- | --- |
| AesKw | 128, 192, 256 |
| AesKwp | 128, 192, 256 |

### Fpe

| primitive | radix | keySize |
| --- | --- | --- |
| AesFf1 | 2, 3, 4, 5, 8, 10, 16, 26, 32, 36, 58, 62, 64, 85 | 128, 192, 256 |

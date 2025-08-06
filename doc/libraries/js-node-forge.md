# node-forge

**Language:**
javascript\
**Url:**
[https://www.npmjs.com/package/node-forge](https://www.npmjs.com/package/node-forge)

This library has a high number of vulnerabilities.
Interfaces are not very intuitive.
Type string is often used to represent byte arrays.

## Performed tests

### Aead

| primitive | keySize | ivSize | tagSize |
| --- | --- | --- | --- |
| AesGcm | 128, 192, 256 | 64, 96, 128, 256 | 96, 128 |

### IndCpa

| primitive | keySize | ivSize | cipher | mode | padding | paddingSize | feedback |
| --- | --- | --- | --- | --- | --- | --- | --- |
| AesCbcPkcs7 | 128, 192, 256 | 128 | Aes | Cbc | Pkcs7 | 128 | |
| TripleDesCbcPkcs7 | 192 | 64 | TripleDes | Cbc | Pkcs7 | 64 | |
| AesCfb128 | 128, 192, 256 | 128 | Aes | Cfb | | | 128 |
| AesOfb | 128, 192, 256 | 128 | Aes | Ofb | | | |

### Pbkdf

| primitive | sha |
| --- | --- |
| Pbkdf | SHA-1 |

### RsaPkcs1Verify

| primitive | size | sha | encoding |
| --- | --- | --- | --- |
| RsaSsaPkcs1 | 1024, 1536, 2048, 3072, 4096 | SHA-1, SHA-256, SHA-384, SHA-512 | DER |

### RsaPssVerify

| primitive | size | sha | mgf | mgfSha | saltLen | encoding |
| --- | --- | --- | --- | --- | --- | --- |
| RsaSsaPss | 1024, 1536, 2048, 3072, 4096 | SHA-1, SHA-256, SHA-384, SHA-512 | MGF1 | SHA-1, SHA-256, SHA-384, SHA-512 | 0, 20, 32, 48, 64 | DER |

### RsaEsPkcs1Decrypt

| primitive | size |
| --- | --- |
| RsaEsPkcs1 | 1024, 2048, 3072, 4096 |

### RsaEsOaepDecrypt

| primitive | size | sha | mgf | mgfSha |
| --- | --- | --- | --- | --- |
| RsaEsOaep | 1024, 2048, 3072, 4096 | SHA-1, SHA-256, SHA-384, SHA-512 | MGF1 | SHA-1, SHA-256, SHA-384, SHA-512 |

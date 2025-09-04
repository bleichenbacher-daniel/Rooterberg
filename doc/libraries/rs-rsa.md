# rsa

**Language:**
rust\
**Url:**
[https://docs.rs/rsa/latest/rsa/](https://docs.rs/rsa/latest/rsa/)\
**Tested version:**
0.9.8

## Performed tests

### RsaPkcs1Verify

| primitive | size | sha | encoding |
| --- | --- | --- | --- |
| RsaSsaPkcs1 | 1024, 1536, 2048, 3072, 4096 | SHA-1, SHA-224, SHA-256, SHA-384, SHA-512 | DER |

### RsaEsPkcs1Decrypt

| primitive | size |
| --- | --- |
| RsaEsPkcs1 | 1024, 2048, 3072, 4096 |

### RsaEsOaepDecrypt

| primitive | size | sha | mgf | mgfSha |
| --- | --- | --- | --- | --- |
| RsaEsOaep | 1024, 2048, 3072, 4096 | SHA-1, SHA-224, SHA-256, SHA-384, SHA-512 | MGF1 | SHA-1, SHA-224, SHA-256, SHA-384, SHA-512 |

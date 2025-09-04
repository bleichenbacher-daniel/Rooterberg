# Conscrypt

**Language:**
java\
**Url:**
[https://github.com/google/conscrypt](https://github.com/google/conscrypt)\
**Tested version:**
1.0

## Performed tests

### Aead

| primitive | keySize | ivSize | tagSize |
| --- | --- | --- | --- |
| Chacha20Poly1305 | 256 | 96 | 128 |
| AesGcm | 128, 256 | 96 | 96, 128 |
| AesGcmSiv | 128, 256 | 96 | 128 |

### IndCpa

| primitive | keySize | ivSize | cipher | mode | padding | paddingSize |
| --- | --- | --- | --- | --- | --- | --- |
| AesCbcPkcs7 | 128, 192, 256 | 128 | Aes | Cbc | Pkcs7 | 128 |
| TripleDesCbcPkcs7 | 192 | 64 | TripleDes | Cbc | Pkcs7 | 64 |

### BlockCipher

| primitive | keySize |
| --- | --- |
| Aes | 128, 192, 256 |

### EcdsaVerify

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | secp224r1, secp256r1, secp384r1, secp521r1 | SHA-224, SHA-256, SHA-384, SHA-512 | DER | False | Generic |

### Ecdh

| primitive | curve | encoding |
| --- | --- | --- |
| Ecdh | secp224r1, secp256r1, secp384r1, secp521r1 | DER |

### Hash

| primitive | digestSize |
| --- | --- |
| md5 | 128 |
| sha-1 | 160 |
| sha-224 | 224 |
| sha-256 | 256 |
| sha-384 | 384 |
| sha-512 | 512 |

### Mac

| primitive | macSize |
| --- | --- |
| HmacSha1 | 160 |
| HmacSha224 | 224 |
| HmacSha256 | 256 |
| HmacSha384 | 384 |
| HmacSha512 | 512 |

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

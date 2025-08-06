# crypto-js

**Language:**
javascript\
**Url:**
[https://www.npmjs.com/package/crypto-js](https://www.npmjs.com/package/crypto-js)

This library is no longer maintained.
It mainly supports symmetric primitives.
Encryption modes do not include authenticated ciphers.

## Performed tests

### IndCpa

| primitive | keySize | ivSize | cipher | mode | padding | paddingSize | feedback | byteOrder |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| AesCbcPkcs7 | 128, 192, 256 | 128 | Aes | Cbc | Pkcs7 | 128 | | |
| AesCbcIso7816 | 128, 192, 256 | 128 | Aes | Cbc | Iso7816Padding | 128 | | |
| TripleDesCbcPkcs7 | 192 | 64 | TripleDes | Cbc | Pkcs7 | 64 | | |
| AesCfb128 | 128, 192, 256 | 128 | Aes | Cfb | | | 128 | |
| AesCfb128Pkcs7 | 128, 192, 256 | 128 | Aes | Cfb | Pkcs7 | 128 | 128 | |
| TripleDesCfb64 | 192 | 64 | TripleDes | Cfb | | | 64 | |
| AesOfb | 128, 192, 256 | 128 | Aes | Ofb | | | | |
| TripleDesOfb | 192 | 64 | TripleDes | Ofb | | | | |
| Rabbit | 128 | 64 | Rabbit | | | | | little |

### Hash

| primitive | digestSize |
| --- | --- |
| sha-1 | 160 |
| sha-224 | 224 |
| sha-256 | 256 |
| sha-384 | 384 |
| sha-512 | 512 |
| ripemd160 | 160 |
| keccak224 | 224 |
| keccak256 | 256 |
| keccak384 | 384 |
| keccak512 | 512 |

### Mac

| primitive | macSize |
| --- | --- |
| HmacSha1 | 160 |
| HmacSha224 | 224 |
| HmacSha256 | 256 |
| HmacSha384 | 384 |
| HmacSha512 | 512 |

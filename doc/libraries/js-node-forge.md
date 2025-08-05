# node-forge

**Language:** javascript\
**Url:**
[https://www.npmjs.com/package/node-forge](https://www.npmjs.com/package/node-forge)

This library has a high number of vulnerabilities. Interfaces are not very
intuitive. Type string is often used to represent byte arrays.

## Performed tests

### Aead

**primitive:** AesGcm\
**keySize:** 128, 192, 256\
**ivSize:** 64, 96, 128, 256\
**tagSize:** 96, 128

### IndCpa

**primitive:** AesCbcPkcs7, AesCfb128, AesOfb, TripleDesCbcPkcs7\
**keySize:** 128, 192, 256\
**ivSize:** 64, 128\
**cipher:** Aes, TripleDes\
**mode:** Cbc, Cfb, Ofb\
**padding:** Pkcs7\
**paddingSize:** 64, 128\
**feedback:** 128

### Pbkdf

**primitive:** Pbkdf\
**sha:** SHA-1

### RsaPkcs1Verify

**primitive:** RsaSsaPkcs1\
**size:** 1024, 1536, 2048, 3072, 4096\
**sha:** SHA-1, SHA-256, SHA-384, SHA-512\
**encoding:** DER

### RsaPssVerify

**primitive:** RsaSsaPss\
**size:** 1024, 1536, 2048, 3072, 4096\
**sha:** SHA-1, SHA-256, SHA-384, SHA-512\
**mgf:** MGF1\
**mgfSha:** SHA-1, SHA-256, SHA-384, SHA-512\
**saltLen:** 0, 20, 32, 48, 64\
**encoding:** DER

### RsaEsPkcs1Decrypt

**size:** 1024, 2048, 3072, 4096

### RsaEsOaepDecrypt

**size:** 1024, 2048, 3072, 4096\
**sha:** SHA-1, SHA-256, SHA-384, SHA-512\
**mgf:** MGF1\
**mgfSha:** SHA-1, SHA-256, SHA-384, SHA-512

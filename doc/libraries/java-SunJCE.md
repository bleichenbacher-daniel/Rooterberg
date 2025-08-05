# SunJCE

**Language:** java\
**Url:**
[https://docs.oracle.com/en/java/javase/24/security/oracle-providers.html](https://docs.oracle.com/en/java/javase/24/security/oracle-providers.html)

## Performed tests

### Aead

**primitive:** AesGcm, Chacha20Poly1305\
**keySize:** 128, 192, 256\
**ivSize:** 64, 96, 128, 256\
**tagSize:** 64, 96, 128

### IndCpa

**primitive:** AesCbcPkcs7, AesCfb128, AesCfb128Pkcs7, AesCfb8, AesOfb,
AesPcbcPkcs7, TripleDesCbcPkcs7, TripleDesCfb64, TripleDesCfb8, TripleDesOfb\
**keySize:** 128, 192, 256\
**ivSize:** 64, 128\
**cipher:** Aes, TripleDes\
**mode:** Cbc, Cfb, Ofb, Pcbc\
**padding:** Pkcs7\
**paddingSize:** 64, 128\
**feedback:** 8, 64, 128

### BlockCipher

**primitive:** Aes, Des, TripleDes\
**keySize:** 64, 128, 192, 256

### KeyWrap

**primitive:** AesKw, AesKwPkcs7, AesKwp\
**keySize:** 128, 192, 256

### Mac

**primitive:** HmacSha1, HmacSha224, HmacSha256, HmacSha384, HmacSha3_224,
HmacSha3_256, HmacSha3_384, HmacSha3_512, HmacSha512\
**macSize:** 160, 224, 256, 384, 512

### Pbkdf

**primitive:** Pbkdf\
**sha:** SHA-1, SHA-224, SHA-256, SHA-384, SHA-512

### Pbes2

**primitive:** Pbes2\
**sha:** SHA-1, SHA-224, SHA-256, SHA-384, SHA-512, SHA-512/224, SHA-512/256\
**cipher:** Aes\
**keySize:** 128, 256

### RsaEsPkcs1Decrypt

**size:** 1024, 2048, 3072, 4096

### RsaEsOaepDecrypt

**size:** 1024, 2048, 3072, 4096\
**sha:** SHA-1, SHA-224, SHA-256, SHA-384, SHA-512, SHA3-224, SHA3-256,
SHA3-384, SHA3-512\
**mgf:** MGF1\
**mgfSha:** SHA-1, SHA-224, SHA-256, SHA-384, SHA-512, SHA3-224, SHA3-256,
SHA3-384, SHA3-512

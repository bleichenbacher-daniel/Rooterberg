# Conscrypt

**Language:** java\
**Url:**
[https://github.com/google/conscrypt](https://github.com/google/conscrypt)

## Performed tests

### Aead

**primitive:** AesGcm, AesGcmSiv, Chacha20Poly1305\
**keySize:** 128, 192, 256\
**ivSize:** 64, 96, 128, 256\
**tagSize:** 64, 96, 128

### IndCpa

**primitive:** AesCbcPkcs7, TripleDesCbcPkcs7\
**keySize:** 128, 192, 256\
**ivSize:** 64, 128\
**cipher:** Aes, TripleDes\
**mode:** Cbc\
**padding:** Pkcs7\
**paddingSize:** 64, 128

### BlockCipher

**primitive:** Aes\
**keySize:** 128, 192, 256

### EcdsaVerify

**curve:** secp224r1, secp256r1, secp384r1, secp521r1\
**sha:** SHA-224, SHA-256, SHA-384, SHA-512\
**encoding:** DER\
**normalize:** False\
**signatureGeneration:** Generic

### Ecdh

**primitive:** Ecdh\
**curve:** secp224r1, secp256r1, secp384r1, secp521r1\
**encoding:** DER

### Hash

**primitive:** md5, sha-1, sha-224, sha-256, sha-384, sha-512\
**digestSize:** 128, 160, 224, 256, 384, 512

### Mac

**primitive:** HmacSha1, HmacSha224, HmacSha256, HmacSha384, HmacSha512\
**macSize:** 160, 224, 256, 384, 512

### Pbes2

**primitive:** Pbes2\
**sha:** SHA-1, SHA-224, SHA-256, SHA-384, SHA-512\
**cipher:** Aes\
**keySize:** 128, 256

### RsaPkcs1Verify

**primitive:** RsaSsaPkcs1\
**size:** 1024, 1536, 2048, 3072, 4096\
**sha:** SHA-1, SHA-224, SHA-256, SHA-384, SHA-512\
**encoding:** DER

### RsaEsPkcs1Decrypt

**size:** 1024, 2048, 3072, 4096

### RsaEsOaepDecrypt

**size:** 1024, 2048, 3072, 4096\
**sha:** SHA-1, SHA-224, SHA-256, SHA-384, SHA-512\
**mgf:** MGF1\
**mgfSha:** SHA-1, SHA-224, SHA-256, SHA-384, SHA-512

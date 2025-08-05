# pyca

**Language:** python\
**Url:**
[https://cryptography.io/en/latest/](https://cryptography.io/en/latest/)

The library can be built against different underlying libraries. The tests are
based on the version using 'pip install cryptography'.

## Performed tests

### Aead

**primitive:** AeadAesCmacSiv, AesCcm, AesGcm, AesGcmSiv, AesOcb,
Chacha20Poly1305\
**keySize:** 128, 192, 256, 384, 512\
**ivSize:** 64, 88, 96, 120, 128, 256\
**tagSize:** 128

### Xdh

**primitive:** x25519, x448\
**encoding:** PEM, RAW

### Daead

**primitive:** DaeadAesCmacSiv\
**keySize:** 256, 384, 512\
**tagSize:** 128

### IndCpa

**primitive:** AesCbcPkcs7, AesCfb128, AesCfb128Pkcs7, AesCfb8, AesOfb, AesXts,
CamelliaCbcPkcs7, CamelliaCfb128, CamelliaOfb, Sm4CbcPkcs7, Sm4Cfb128, Sm4Ofb\
**keySize:** 128, 192, 256, 512\
**ivSize:** 128\
**cipher:** Aes, Camellia, SM4\
**mode:** Cbc, Cfb, Ofb, Xts\
**padding:** Pkcs7\
**paddingSize:** 128\
**feedback:** 8, 128

### BlockCipher

**primitive:** Aes, Camellia, Cast128, SM4, Seed, TripleDes\
**keySize:** 128, 192, 256

### DsaVerify

**pLen:** 1024, 2048, 3072\
**qLen:** 160, 224, 256\
**sha:** SHA-1, SHA-224, SHA-256, SHA-512\
**encoding:** DER\
**signatureGeneration:** Generic

### EcdsaVerify

**curve:** brainpoolP256r1, brainpoolP384r1, brainpoolP512r1, secp192r1,
secp224r1, secp256k1, secp256r1, secp384r1, secp521r1, sect233k1, sect283k1\
**sha:** SHA-224, SHA-256, SHA-384, SHA-512, SHA3-256, SHA3-384, SHA3-512,
SHAKE128, SHAKE256\
**encoding:** DER\
**normalize:** False\
**signatureGeneration:** Generic

### EcdsaSign

**curve:** brainpoolP256r1, brainpoolP384r1, brainpoolP512r1, secp192r1,
secp224r1, secp256k1, secp256r1, secp384r1, secp521r1\
**sha:** SHA-224, SHA-256, SHA-384, SHA-512, SHA3-256, SHA3-384, SHA3-512\
**encoding:** DER\
**normalize:** False\
**signatureGeneration:** Rfc6979

### EddsaVerify

**curve:** edwards25519, edwards448\
**cofactored:** False\
**encoding:** RAW

### EddsaSign

**curve:** edwards25519, edwards448\
**cofactored:** False\
**encoding:** RAW

### Ecdh

**primitive:** Ecdh\
**curve:** brainpoolP256r1, brainpoolP384r1, brainpoolP512r1, secp192r1,
secp224r1, secp256k1, secp256r1, secp384r1, secp521r1, sect233k1, sect283k1,
sect409k1, sect571k1\
**encoding:** DER, PEM

### KeyWrap

**primitive:** AesKw, AesKwp, AesSivKw\
**keySize:** 128, 192, 256, 384, 512

### Mac

**primitive:** AesCmac, CamelliaCmac, HmacSha1, HmacSha224, HmacSha256,
HmacSha384, HmacSha3_224, HmacSha3_256, HmacSha3_384, HmacSha3_512, HmacSha512\
**keySize:** 128, 192, 256\
**macSize:** 128, 160, 224, 256, 384, 512

### Pbkdf

**primitive:** Pbkdf\
**sha:** SHA-1, SHA-224, SHA-256, SHA-384, SHA-512, SHA-512/224, SHA-512/256,
SHA3-224, SHA3-256, SHA3-384, SHA3-512

### Scrypt

**primitive:** Pbkdf

### Hkdf

**primitive:** HkdfSha1, HkdfSha224, HkdfSha256, HkdfSha384, HkdfSha3_224,
HkdfSha3_256, HkdfSha3_384, HkdfSha3_512, HkdfSha512, HkdfSha512_224,
HkdfSha512_256\
**sha:** SHA-1, SHA-224, SHA-256, SHA-384, SHA-512, SHA-512/224, SHA-512/256,
SHA3-224, SHA3-256, SHA3-384, SHA3-512

### Pkcs8Decrypt

**primitive:** Pkcs8, Pkcs8Scrypt\
**sha:** SHA-1, SHA-256\
**cipher:** AES-CBC-128, AES-CBC-192, AES-CBC-256, DES-EDE3-CBC

### RsaPkcs1Verify

**primitive:** RsaSsaPkcs1\
**size:** 1024, 1536, 2048, 3072, 4096\
**sha:** SHA-1, SHA-224, SHA-256, SHA-384, SHA-512, SHA3-256, SHA3-384,
SHA3-512\
**encoding:** DER

### RsaPssVerify

**primitive:** RsaSsaPss\
**size:** 1024, 1536, 2048, 3072, 4096\
**sha:** SHA-1, SHA-224, SHA-256, SHA-384, SHA-512\
**mgf:** MGF1\
**mgfSha:** SHA-1, SHA-224, SHA-256, SHA-384, SHA-512\
**saltLen:** 0, 20, 28, 32, 48, 64\
**encoding:** DER

### RsaEsPkcs1Decrypt

**size:** 1024, 2048, 3072, 4096

### RsaEsOaepDecrypt

**size:** 1024, 2048, 3072, 4096\
**sha:** SHA-1, SHA-224, SHA-256, SHA-384, SHA-512\
**mgf:** MGF1\
**mgfSha:** SHA-1, SHA-224, SHA-256, SHA-384, SHA-512

# node.js

**Language:** javascript\
**Url:**
[https://nodejs.org/api/crypto.html](https://nodejs.org/api/crypto.html)

## Performed tests

### Aead

**primitive:** AesCcm, AesGcm, AesOcb, AriaCcm, AriaGcm, Chacha20Poly1305\
**keySize:** 128, 192, 256\
**ivSize:** 64, 88, 96, 104, 120, 128, 256\
**tagSize:** 64, 96, 128

### IndCpa

**primitive:** AesCbcPkcs7, AesCfb128, AesCfb8, AesOfb, AesXts, AriaCbcPkcs7,
AriaCfb128, AriaCfb8, AriaOfb, CamelliaCbcPkcs7, CamelliaCfb128, CamelliaCfb8,
CamelliaOfb, Sm4CbcPkcs7, Sm4Cfb128, Sm4Ofb\
**keySize:** 128, 192, 256, 512\
**ivSize:** 128\
**cipher:** Aes, Aria, Camellia, SM4\
**mode:** Cbc, Cfb, Ofb, Xts\
**padding:** Pkcs7\
**paddingSize:** 128\
**feedback:** 8, 128

### EcdsaVerify

**curve:** brainpoolP256r1, brainpoolP256t1, brainpoolP320r1, brainpoolP320t1,
brainpoolP384r1, brainpoolP384t1, brainpoolP512r1, brainpoolP512t1, prime192v2,
prime239v1, secp160r1, secp192k1, secp192r1, secp224k1, secp224r1, secp256k1,
secp256r1, secp384r1, secp521r1\
**sha:** SHA-224, SHA-256, SHA-384, SHA-512, SHA3-256, SHA3-384, SHA3-512\
**encoding:** DER, JWK, P1363\
**normalize:** False, True\
**signatureGeneration:** Generic

### Ecdh

**primitive:** Ecdh\
**curve:** brainpoolP224r1, brainpoolP224t1, brainpoolP256r1, brainpoolP256t1,
brainpoolP320r1, brainpoolP320t1, brainpoolP384r1, brainpoolP384t1,
brainpoolP512r1, brainpoolP512t1, secp160r1, secp192r1, secp224r1, secp256k1,
secp256r1, secp384r1, secp521r1, sm2\
**encoding:** UNCOMPRESSED

### KeyWrap

**primitive:** AesKw\
**keySize:** 128, 192, 256

### Pbkdf

**primitive:** Pbkdf\
**sha:** SHA-1, SHA-224, SHA-256, SHA-384, SHA-512, SHA3-224, SHA3-256,
SHA3-384, SHA3-512

### Hkdf

**primitive:** HkdfSha1, HkdfSha224, HkdfSha256, HkdfSha384, HkdfSha3_224,
HkdfSha3_256, HkdfSha3_384, HkdfSha3_512, HkdfSha512\
**sha:** SHA-1, SHA-224, SHA-256, SHA-384, SHA-512, SHA3-224, SHA3-256,
SHA3-384, SHA3-512

### Pkcs8Decrypt

**primitive:** Pkcs8, Pkcs8Scrypt\
**sha:** SHA-1, SHA-256\
**cipher:** AES-CBC-128, AES-CBC-192, AES-CBC-256, AES-CFB-128, AES-CFB-192,
AES-CFB-256, AES-OFB-128, AES-OFB-192, AES-OFB-256, DES-EDE3-CBC

### RsaPkcs1Verify

**primitive:** RsaSsaPkcs1\
**size:** 1024, 1536, 2048, 3072, 4096\
**sha:** SHA-224, SHA-256, SHA-384, SHA-512, SHA3-256, SHA3-384, SHA3-512\
**encoding:** DER

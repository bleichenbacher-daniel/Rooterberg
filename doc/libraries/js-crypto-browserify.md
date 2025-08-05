# crypto-browserify

**Language:** javascript\
**Url:**
[https://www.npmjs.com/package/crypto-browserify](https://www.npmjs.com/package/crypto-browserify)

crypto-browserify is a reimplementation of the cryptographic library in node.js.
Using the same interface as node.js simplifies porting implementations from one
library to the other.

## Performed tests

### Aead

**primitive:** AesCcm, AesGcm, AesOcb, AriaCcm, AriaGcm, Chacha20Poly1305\
**keySize:** 128, 192, 256\
**ivSize:** 64, 88, 96, 104, 120, 128, 256\
**tagSize:** 64, 96, 128

### IndCpa

**primitive:** AesCbcPkcs7, AesCfb128, AesCfb8, AesOfb, AriaCbcPkcs7,
AriaCfb128, AriaCfb8, AriaOfb, CamelliaCbcPkcs7, CamelliaCfb128, CamelliaCfb8,
CamelliaOfb, Sm4CbcPkcs7, Sm4Cfb128, Sm4Ofb\
**keySize:** 128, 192, 256\
**ivSize:** 128\
**cipher:** Aes, Aria, Camellia, SM4\
**mode:** Cbc, Cfb, Ofb\
**padding:** Pkcs7\
**paddingSize:** 128\
**feedback:** 8, 128

### EcdsaVerify

**curve:** secp192r1, secp224r1, secp256k1, secp256r1, secp384r1, secp521r1\
**sha:** SHA-224, SHA-256, SHA-384, SHA-512\
**encoding:** DER\
**normalize:** False\
**signatureGeneration:** Generic

### Ecdh

**primitive:** Ecdh\
**curve:** secp160r1, secp192r1, secp224r1, secp256k1, secp256r1, secp384r1,
secp521r1\
**encoding:** UNCOMPRESSED

### KeyWrap

**primitive:** AesKw\
**keySize:** 128, 192, 256

### Pbkdf

**primitive:** Pbkdf\
**sha:** SHA-1, SHA-224, SHA-256, SHA-384, SHA-512, SHA3-224, SHA3-256,
SHA3-384, SHA3-512

### RsaPkcs1Verify

**primitive:** RsaSsaPkcs1\
**size:** 1024, 1536, 2048, 3072, 4096\
**sha:** SHA-1, SHA-224, SHA-256, SHA-384, SHA-512\
**encoding:** DER

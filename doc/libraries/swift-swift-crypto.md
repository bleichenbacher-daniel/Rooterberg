# swift-crypto

**Language:** swift\
**Url:**
[https://github.com/apple/swift-crypto](https://github.com/apple/swift-crypto)

This is a reimplementation of Apple's CryptoKit. Uses BoringSSL as underlying
crypto library.

## Performed tests

### Aead

**primitive:** AesGcm, AesGcmSiv, Chacha20Poly1305\
**keySize:** 128, 192, 256\
**ivSize:** 96, 128, 256\
**tagSize:** 128

### Xdh

**primitive:** x25519\
**encoding:** RAW

### EcdsaVerify

**curve:** secp256r1, secp384r1, secp521r1\
**sha:** SHA-256, SHA-384, SHA-512\
**encoding:** DER\
**normalize:** False\
**signatureGeneration:** Generic

### EddsaVerify

**curve:** edwards25519\
**cofactored:** False\
**encoding:** RAW

### Ecdh

**primitive:** Ecdh\
**curve:** secp256r1, secp384r1, secp521r1\
**encoding:** DER

### KeyWrap

**primitive:** AesKw\
**keySize:** 128, 192, 256

### Mac

**primitive:** HmacSha256, HmacSha384, HmacSha512\
**macSize:** 256, 384, 512

### RsaPssVerify

**primitive:** RsaSsaPss\
**size:** 2048, 3072, 4096\
**sha:** SHA-256\
**mgf:** MGF1\
**mgfSha:** SHA-256\
**saltLen:** 32\
**encoding:** DER

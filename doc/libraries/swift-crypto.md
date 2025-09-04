# swift-crypto

**Language:**
swift\
**Url:**
[https://github.com/apple/swift-crypto](https://github.com/apple/swift-crypto)

This is a reimplementation of Apple's CryptoKit.
Uses BoringSSL as underlying crypto library.

## Performed tests

### Aead

| primitive | keySize | ivSize | tagSize |
| --- | --- | --- | --- |
| Chacha20Poly1305 | 256 | 96 | 128 |
| AesGcm | 128, 192, 256 | 96, 128, 256 | 128 |
| AesGcmSiv | 128, 256 | 96 | 128 |

### Xdh

| primitive | curve | encoding |
| --- | --- | --- |
| x25519 | curve25519 | RAW |

### EcdsaVerify

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | secp256r1, secp384r1, secp521r1 | SHA-256, SHA-384, SHA-512 | DER | False | Generic |

### EddsaVerify

| primitive | curve | cofactored | encoding |
| --- | --- | --- | --- |
| Eddsa | edwards25519 | False | RAW |

### Ecdh

| primitive | curve | encoding |
| --- | --- | --- |
| Ecdh | secp256r1, secp384r1, secp521r1 | DER |

### KeyWrap

| primitive | keySize |
| --- | --- |
| AesKw | 128, 192, 256 |

### RsaPssVerify

| primitive | size | sha | mgf | mgfSha | saltLen | encoding |
| --- | --- | --- | --- | --- | --- | --- |
| RsaSsaPss | 2048, 3072, 4096 | SHA-256 | MGF1 | SHA-256 | 32 | DER |

# cryptography_plus

**Language:**
dart\
**Url:**
[https://pub.dev/packages/cryptography_plus](https://pub.dev/packages/cryptography_plus)

This library is a replacement for the dart cryptography package.

## Security

The library implements insecure primitives.
An example are AES-CTR and AES-CBC with an HMAC.
The HMAC does not include the IV.
As a result, an authentication bypass is possible by simply changing the IV.

## Performed tests

### Aead

| primitive | keySize | ivSize | tagSize |
| --- | --- | --- | --- |
| Chacha20Poly1305 | 256 | 96 | 128 |
| XChacha20Poly1305 | 256 | 192 | 128 |
| AesGcm | 128, 192, 256 | 64, 96, 128, 256 | 128 |

### Hkdf

| primitive | sha |
| --- | --- |
| HkdfSha1 | SHA-1 |
| HkdfSha224 | SHA-224 |
| HkdfSha256 | SHA-256 |
| HkdfSha384 | SHA-384 |
| HkdfSha512 | SHA-512 |

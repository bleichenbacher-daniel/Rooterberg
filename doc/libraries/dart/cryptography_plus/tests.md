# Performed tests for cryptography_plus

## Aead

| primitive | keySize | ivSize | tagSize |
| --- | --- | --- | --- |
| Chacha20Poly1305 | 256 | 96 | 128 |
| XChacha20Poly1305 | 256 | 192 | 128 |
| AesGcm | 128, 192, 256 | 64, 96, 128, 256 | 128 |

## Hkdf

| primitive | sha |
| --- | --- |
| HkdfSha1 | SHA-1 |
| HkdfSha224 | SHA-224 |
| HkdfSha256 | SHA-256 |
| HkdfSha384 | SHA-384 |
| HkdfSha512 | SHA-512 |

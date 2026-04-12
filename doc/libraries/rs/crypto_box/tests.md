# Performed tests for crypto_box

## NaclCryptoBox

| primitive | keyAgreement | curve | kdf | cipher | ivSize |
| --- | --- | --- | --- | --- | --- |
| NaclCryptoBoxCurve25519XSalsa20Poly1305 | x25519 | curve25519 | HSalsa20 | NaclXSalsa20Poly1305 | 192 |
| NaclCryptoBoxCurve25519XChacha20Poly1305 | x25519 | curve25519 | HChacha20 | NaclXChacha20Poly1305 | 192 |

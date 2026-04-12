# Performed tests for tweetnacl

## AuthEnc

| primitive | keySize | ivSize | tagSize |
| --- | --- | --- | --- |
| NaclXSalsa20Poly1305 | 256 | 192 | 128 |

## NaclCryptoBox

| primitive | keyAgreement | curve | kdf | cipher | ivSize |
| --- | --- | --- | --- | --- | --- |
| NaclCryptoBoxCurve25519XSalsa20Poly1305 | x25519 | curve25519 | HSalsa20 | NaclXSalsa20Poly1305 | 192 |

## EddsaVerify

| primitive | curve | cofactored | encoding |
| --- | --- | --- | --- |
| Eddsa | edwards25519 | False | RAW |

## EddsaSign

| primitive | curve | cofactored | encoding |
| --- | --- | --- | --- |
| Eddsa | edwards25519 | False | RAW |

# tweetnacl

**Language:**
javascript\
**Url:**
[https://github.com/dchest/tweetnacl-js](https://github.com/dchest/tweetnacl-js)

The library implements primitives for the NACL protocol.
As a consequence, algorithms like xsalsa20-poly1305 are authenticated, but do not accept AAD.

## Performed tests

### AuthEnc

| primitive | keySize | ivSize | tagSize |
| --- | --- | --- | --- |
| NaclXSalsa20Poly1305 | 256 | 192 | 128 |

### NaclCryptoBox

| primitive | keyAgreement | curve | kdf | cipher | ivSize |
| --- | --- | --- | --- | --- | --- |
| NaclCryptoBoxCurve25519XSalsa20Poly1305 | x25519 | curve25519 | HSalsa20 | NaclXSalsa20Poly1305 | 192 |

### EddsaVerify

| primitive | curve | cofactored | encoding |
| --- | --- | --- | --- |
| Eddsa | edwards25519 | False | RAW |

### EddsaSign

| primitive | curve | cofactored | encoding |
| --- | --- | --- | --- |
| Eddsa | edwards25519 | False | RAW |

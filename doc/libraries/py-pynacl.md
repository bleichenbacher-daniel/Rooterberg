# pynacl

**Language:**
python\
**Url:**
[https://pynacl.readthedocs.io/en/latest/](https://pynacl.readthedocs.io/en/latest/)

Somewhat confusing is the use of uneven interfaces.
nacl.secret.SecretBox implements XSalsa20Poly1305 as defined in the NaCl protocol.
This encryption mode does not allow an AAD.
The default format of the ciphertext is iv || tag || ciphertext.nacl.secret.Aead implements XChaCha20Poly1305 as defined in the IETF draft draft-irtf-cfrg-xchacha.
This default format of ciphertext for this encryption mode is iv || ciphertext || tag.

## Performed tests

### AuthEnc

| primitive | keySize | ivSize | tagSize |
| --- | --- | --- | --- |
| NaclXSalsa20Poly1305 | 256 | 192 | 128 |

### Aead

| primitive | keySize | ivSize | tagSize |
| --- | --- | --- | --- |
| XChacha20Poly1305 | 256 | 192 | 128 |

### NaclCryptoBox

| primitive | keyAgreement | curve | kdf | cipher | ivSize |
| --- | --- | --- | --- | --- | --- |
| NaclCryptoBoxCurve25519XSalsa20Poly1305 | x25519 | curve25519 | HSalsa20 | NaclXSalsa20Poly1305 | 192 |

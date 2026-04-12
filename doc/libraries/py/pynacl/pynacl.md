# pynacl

**Language:** python\
**Url:**
[https://pynacl.readthedocs.io/en/latest/](https://pynacl.readthedocs.io/en/latest/)

Somewhat confusing is the use of uneven interfaces. nacl.secret.SecretBox
implements XSalsa20Poly1305 as defined in the NaCl protocol. This encryption
mode does not allow an AAD. The default format of the ciphertext is iv || tag ||
ciphertext.nacl.secret.Aead implements XChaCha20Poly1305 as defined in the IETF
draft draft-irtf-cfrg-xchacha. The default format of ciphertext for this
encryption mode is iv || ciphertext || tag.

## Tables

[Performed tests](tests.md)\
[Test results](results.json)

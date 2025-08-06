# starkbank-ecdsa

**Language:**
python\
**Url:**
[https://pypi.org/project/starkbank-ecdsa/](https://pypi.org/project/starkbank-ecdsa/)

## Performed tests

### EcdsaVerify

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | secp256k1, secp256r1, secp384r1 | SHA-256, SHA-384 | DER | False | Generic |

The library implements ECDSA over secp256r1 and secp256k1 using SHA-256.
Other curves and other hash functions could in principle be used.
However, this needs to be done carefully, since for example hash truncation is not supported.

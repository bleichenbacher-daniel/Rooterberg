# tiny-secp256k1

**Language:**
javascript\
**Url:**
[https://www.npmjs.com/package/secp256k1](https://www.npmjs.com/package/secp256k1)

## Performed tests

### EcdsaVerify

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | secp256k1 | SHA-256 | P1363 | False, True | Generic |

The library checks whether signatures are normalized if the verification is called with strict=true.

### EcdsaSign

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | secp256k1 | SHA-256 | P1363 | True | Rfc6979 |

ECDSA signatures are generated using RFC 6979.
There appears to be no way to specify the hash function.
The library implicitly assumes that SHA-256 is being used.

### SchnorrVerify

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Schnorr | secp256k1 | SHA-256 | BIP340 | True | Generic |

### SchnorrSign

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Schnorr | secp256k1 | SHA-256 | BIP340 | True | BIP340 |

The library requires that the data signed is 32 bytes long.
This restriction has been lifted in newer versions of BIP 340, which allows data of arbitrary length.
However, the primary user is bitcoinjs, which only uses 32 byte inputs.

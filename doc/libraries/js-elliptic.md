# elliptic

**Language:**
javascript\
**Url:**
[https://www.npmjs.com/package/elliptic](https://www.npmjs.com/package/elliptic)

## Security

This library fixes vulnerabilities very slowly.
An example is CVE-2024-48948, which is an issue found in July, 2024.
The issue was later found to be critical, as it leaks private key in some cases.
Version 6.6.1, is still suceptible to the vulnerability.
Currently (July, 2025) no fixed version is available.
Ecdh, ECDSA and EdDSA are not constant time.

## Performed tests

### EcdsaVerify

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | secp192r1, secp224r1, secp256k1, secp256r1, secp384r1, secp521r1 | SHA-256, SHA-384, SHA-512 | DER | False | Generic |

### EcdsaSign

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | secp192r1, secp224r1, secp256k1, secp256r1, secp384r1, secp521r1 | SHA-256, SHA-384, SHA-512 | DER | False | Rfc6979 |

### EddsaVerify

| primitive | curve | cofactored | encoding |
| --- | --- | --- | --- |
| Eddsa | edwards25519 | False | RAW |

### EddsaSign

| primitive | curve | cofactored | encoding |
| --- | --- | --- | --- |
| Eddsa | edwards25519 | False | RAW |

### Ecdh

| primitive | curve | encoding |
| --- | --- | --- |
| Ecdh | secp192r1, secp224r1, secp256k1, secp256r1, secp384r1, secp521r1 | UNCOMPRESSED |

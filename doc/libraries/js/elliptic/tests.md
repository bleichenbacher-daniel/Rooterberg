# Performed tests for elliptic

## EcdsaVerify

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | secp192r1, secp224r1, secp256k1, secp256r1, secp384r1, secp521r1 | SHA-256, SHA-384, SHA-512 | DER | False | Generic |

## EcdsaSign

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | secp192r1, secp224r1, secp256k1, secp256r1, secp384r1, secp521r1 | SHA-256, SHA-384, SHA-512 | DER | False, True | Rfc6979 |

## EddsaVerify

| primitive | curve | cofactored | encoding |
| --- | --- | --- | --- |
| Eddsa | edwards25519 | False | RAW |

## EddsaSign

| primitive | curve | cofactored | encoding |
| --- | --- | --- | --- |
| Eddsa | edwards25519 | False | RAW |

## Ecdh

| primitive | curve | encoding |
| --- | --- | --- |
| Ecdh | secp192r1, secp224r1, secp256k1, secp256r1, secp384r1, secp521r1 | UNCOMPRESSED |

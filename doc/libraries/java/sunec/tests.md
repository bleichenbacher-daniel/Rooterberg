# Performed tests for SunEC

## Xdh

| primitive | curve | encoding |
| --- | --- | --- |
| x25519 | curve25519 | DER, RAW |
| x448 | curve448 | DER, RAW |

## EcdsaVerify

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | secp256r1, secp384r1, secp521r1 | SHA-256, SHA-384, SHA-512, SHA3-256, SHA3-384, SHA3-512 | DER, P1363 | False | Generic |

## EddsaVerify

| primitive | curve | cofactored | encoding |
| --- | --- | --- | --- |
| Eddsa | edwards25519, edwards448 | False | RAW |

## EddsaSign

| primitive | curve | cofactored | encoding |
| --- | --- | --- | --- |
| Eddsa | edwards25519, edwards448 | False | RAW |

## Ecdh

| primitive | curve | encoding |
| --- | --- | --- |
| Ecdh | secp256r1, secp384r1, secp521r1 | DER |

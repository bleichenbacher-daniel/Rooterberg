# Performed tests for p256

## EcdsaVerify

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | secp256r1 | SHA-256 | P1363 | False | Generic |

## EcdsaSign

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | secp256r1 | SHA-256 | P1363 | False | Rfc6979 |

## Ecdh

| primitive | curve | encoding |
| --- | --- | --- |
| Ecdh | secp256r1 | UNCOMPRESSED |

## KeyPair

| primitive | curve |
| --- | --- |
| key_pair_secp256r1 | secp256r1 |

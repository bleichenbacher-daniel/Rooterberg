# Performed tests for p384

## EcdsaVerify

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | secp384r1 | SHA-384 | P1363 | False | Generic |

## EcdsaSign

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | secp384r1 | SHA-384 | P1363 | False | Rfc6979 |

## Ecdh

| primitive | curve | encoding |
| --- | --- | --- |
| Ecdh | secp384r1 | UNCOMPRESSED |

## KeyPair

| primitive | curve |
| --- | --- |
| key_pair_secp384r1 | secp384r1 |

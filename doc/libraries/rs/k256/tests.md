# Performed tests for k256

## EcdsaVerify

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | secp256k1 | SHA-256 | P1363 | True | Generic |

## EcdsaSign

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | secp256k1 | SHA-256 | P1363 | True | Rfc6979 |

## SchnorrVerify

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Schnorr | secp256k1 | SHA-256 | BIP340 | True | Generic |

## SchnorrSign

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Schnorr | secp256k1 | SHA-256 | BIP340 | True | BIP340 |

## Ecdh

| primitive | curve | encoding |
| --- | --- | --- |
| Ecdh | secp256k1 | UNCOMPRESSED |

## KeyPair

| primitive | curve |
| --- | --- |
| key_pair_secp256k1 | secp256k1 |

# Performed tests for swift-crypto

## Xdh

| primitive | curve | encoding |
| --- | --- | --- |
| x25519 | curve25519 | RAW |

## Aead

| primitive | keySize | ivSize | tagSize |
| --- | --- | --- | --- |
| AesGcm | 128, 192, 256 | 128, 256 | 128 |
| AesGcmSiv | 128, 256 | 96 | 128 |

## EcdsaVerify

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | secp256r1, secp384r1, secp521r1 | SHA-256, SHA-384, SHA-512 | DER | False | Generic |

## EddsaVerify

| primitive | curve | cofactored | encoding |
| --- | --- | --- | --- |
| Eddsa | edwards25519 | False | RAW |

## Ecdh

| primitive | curve | encoding |
| --- | --- | --- |
| Ecdh | secp256r1, secp384r1, secp521r1 | DER |

## KeyWrap

| primitive | keySize |
| --- | --- |
| AesKw | 128, 192, 256 |

## RsaPssVerify

| primitive | size | sha | mgf | mgfSha | saltLen | encoding |
| --- | --- | --- | --- | --- | --- | --- |
| RsaSsaPss | 2048, 3072, 4096 | SHA-256 | MGF1 | SHA-256 | 32 | DER |

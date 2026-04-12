# Performed tests for sjcl

## Aead

| primitive | keySize | ivSize | tagSize |
| --- | --- | --- | --- |
| AesGcm | 128, 192, 256 | 64, 96, 128, 256 | 64, 96, 128 |
| AesCcm | 128, 192, 256 | 88, 96, 104 | 64, 96, 128 |

The library contains an implementation of OCB2.
This is an insecure encryption mode.
[Cryptanalysis of OCB2](https://eprint.iacr.org/2018/1040.pdf)
The implementation of AES-CCM silently truncates nonces when they are too long.

## EcdsaVerify

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | secp192k1, secp192r1, secp224r1, secp256k1, secp256r1, secp384r1 | SHA-256, SHA-512 | P1363 | False | Generic |

## Ecdh

| primitive | curve | encoding |
| --- | --- | --- |
| Ecdh | secp192k1, secp192r1, secp224k1, secp224r1, secp256k1, secp256r1, secp384r1 | UNCOMPRESSED |

## Mac

| primitive | macSize |
| --- | --- |
| HmacSha256 | 256 |
| HmacSha512 | 512 |

## Scrypt

| primitive |
| --- |
| Pbkdf |

# sjcl

**Language:**
javascript\
**Url:**
[https://github.com/bitwiseshiftleft/sjcl](https://github.com/bitwiseshiftleft/sjcl)

The library mainly looks like a research project.
I.e., the code has been written to focus on some specific aspects (such as optimizing AES).
The last update of the library was done in 2019.

## Security

The library is vulnerable to timing attacks.
The function ecdhJavaEc does not validate inputs and hence is susceptible to invalid curve attacks.

## Performed tests

### Aead

| primitive | keySize | ivSize | tagSize |
| --- | --- | --- | --- |
| AesGcm | 128, 192, 256 | 64, 96, 128, 256 | 64, 96, 128 |
| AesCcm | 128, 192, 256 | 88, 96, 104 | 64, 96, 128 |

The library contains an implementation of OCB2.
This is an insecure encryption mode.
[Cryptanalysis of OCB2](https://eprint.iacr.org/2018/1040.pdf)
The implementation of AES-CCM silently truncates nonces when they are too long.

### EcdsaVerify

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | secp192k1, secp192r1, secp224r1, secp256k1, secp256r1, secp384r1 | SHA-256, SHA-512 | P1363 | False | Generic |

### Ecdh

| primitive | curve | encoding |
| --- | --- | --- |
| Ecdh | secp192k1, secp192r1, secp224k1, secp224r1, secp256k1, secp256r1, secp384r1 | UNCOMPRESSED |

### Mac

| primitive | macSize |
| --- | --- |
| HmacSha256 | 256 |
| HmacSha512 | 512 |

### Pbkdf

| primitive | sha |
| --- | --- |
| Pbkdf | SHA-256 |

### Scrypt

| primitive |
| --- |
| Pbkdf |

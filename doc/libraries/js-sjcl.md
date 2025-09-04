# sjcl

**Language:**
javascript\
**Url:**
[https://github.com/bitwiseshiftleft/sjcl](https://github.com/bitwiseshiftleft/sjcl)

The library mainly looks like a research project.
I.e., the code has been written to focus on some specific aspects (such as optimizing AES).

## Security

The library is vulnerable to timing attacks.
The function ecdhJavaEc does not validate inputs and hence is susceptible to invalid curve attacks.

## Performed tests

### EcdsaVerify

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | secp192k1, secp192r1, secp224r1, secp256k1, secp256r1, secp384r1 | SHA-256, SHA-512 | P1363 | False | Generic |

### Ecdh

| primitive | curve | encoding |
| --- | --- | --- |
| Ecdh | secp192r1, secp224r1, secp256k1, secp256r1, secp384r1 | UNCOMPRESSED |

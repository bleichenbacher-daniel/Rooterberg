# SunEC

**Language:**
java\
**Url:**
[https://docs.oracle.com/en/java/javase/24/security/oracle-providers.html](https://docs.oracle.com/en/java/javase/24/security/oracle-providers.html)

## Performed tests

### Xdh

| primitive | encoding |
| --- | --- |
| x25519 | DER, RAW |
| x448 | DER, RAW |

### EcdsaVerify

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | secp256r1, secp384r1, secp521r1 | SHA-256, SHA-384, SHA-512, SHA3-256, SHA3-384, SHA3-512 | DER, P1363 | False | Generic |

### Ecdh

| primitive | curve | encoding |
| --- | --- | --- |
| Ecdh | secp256r1, secp384r1, secp521r1 | DER |

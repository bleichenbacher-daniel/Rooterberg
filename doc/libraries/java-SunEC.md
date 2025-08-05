# SunEC

**Language:** java\
**Url:**
[https://docs.oracle.com/en/java/javase/24/security/oracle-providers.html](https://docs.oracle.com/en/java/javase/24/security/oracle-providers.html)

## Performed tests

### Xdh

**primitive:** x25519, x448\
**encoding:** DER, RAW

### EcdsaVerify

**curve:** secp256r1, secp384r1, secp521r1\
**sha:** SHA-256, SHA-384, SHA-512, SHA3-256, SHA3-384, SHA3-512\
**encoding:** DER, P1363\
**normalize:** False\
**signatureGeneration:** Generic

### Ecdh

**primitive:** Ecdh\
**curve:** secp256r1, secp384r1, secp521r1\
**encoding:** DER

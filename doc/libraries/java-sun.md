# SUN

**Language:**
java\
**Url:**
[https://docs.oracle.com/en/java/javase/24/security/oracle-providers.html](https://docs.oracle.com/en/java/javase/24/security/oracle-providers.html)\
**Tested version:**
21

## Performed tests

### DsaVerify

| primitive | pLen | qLen | sha | encoding | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Dsa | 1024, 2048, 3072 | 160, 224, 256 | SHA-1, SHA-224, SHA-256, SHA-512 | DER, P1363 | Generic |

### Hash

| primitive | digestSize |
| --- | --- |
| md5 | 128 |
| sha-1 | 160 |
| sha-224 | 224 |
| sha-256 | 256 |
| sha-384 | 384 |
| sha-512 | 512 |
| sha-512/224 | 224 |
| sha-512/256 | 256 |
| sha3-224 | 224 |
| sha3-256 | 256 |
| sha3-384 | 384 |
| sha3-512 | 512 |

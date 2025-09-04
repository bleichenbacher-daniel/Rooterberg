# SunRsaSign

**Language:**
java\
**Url:**
[https://docs.oracle.com/en/java/javase/24/security/oracle-providers.html](https://docs.oracle.com/en/java/javase/24/security/oracle-providers.html)\
**Tested version:**
21

## Performed tests

### RsaPkcs1Verify

| primitive | size | sha | encoding |
| --- | --- | --- | --- |
| RsaSsaPkcs1 | 1024, 1536, 2048, 3072, 4096 | SHA-1, SHA-224, SHA-256, SHA-384, SHA-512, SHA3-256, SHA3-384, SHA3-512 | DER |

### RsaPssVerify

| primitive | size | sha | mgf | mgfSha | saltLen | encoding |
| --- | --- | --- | --- | --- | --- | --- |
| RsaSsaPss | 1024, 1536, 2048, 3072, 4096 | SHA-1, SHA-224, SHA-256, SHA-384, SHA-512 | MGF1 | SHA-1, SHA-224, SHA-256, SHA-384, SHA-512 | 0, 20, 28, 32, 48, 64 | DER |

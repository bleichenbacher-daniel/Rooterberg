# SunRsaSign

**Language:** java\
**Url:**
[https://docs.oracle.com/en/java/javase/24/security/oracle-providers.html](https://docs.oracle.com/en/java/javase/24/security/oracle-providers.html)

## Performed tests

### RsaPkcs1Verify

**primitive:** RsaSsaPkcs1\
**size:** 1024, 1536, 2048, 3072, 4096\
**sha:** SHA-1, SHA-224, SHA-256, SHA-384, SHA-512, SHA3-256, SHA3-384,
SHA3-512\
**encoding:** DER

### RsaPssVerify

**primitive:** RsaSsaPss\
**size:** 1024, 1536, 2048, 3072, 4096\
**sha:** SHA-1, SHA-224, SHA-256, SHA-384, SHA-512\
**mgf:** MGF1\
**mgfSha:** SHA-1, SHA-224, SHA-256, SHA-384, SHA-512\
**saltLen:** 0, 20, 28, 32, 48, 64\
**encoding:** DER

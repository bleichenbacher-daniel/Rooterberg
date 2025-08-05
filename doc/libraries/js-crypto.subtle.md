# crypto.subtle

**Language:** javascript\
**Url:**
[https://www.w3.org/TR/2017/REC-WebCryptoAPI-20170126/](https://www.w3.org/TR/2017/REC-WebCryptoAPI-20170126/)

crypto.subtle is an interface and has many independent implementations.
Currently, all tests run against the version built into node.

## Performed tests

### Aead

**primitive:** AesGcm\
**keySize:** 128, 192, 256\
**ivSize:** 96, 128, 256\
**tagSize:** 96, 128

### EcdsaVerify

**curve:** secp256r1, secp384r1, secp521r1\
**sha:** SHA-256, SHA-384, SHA-512\
**encoding:** JWK\
**normalize:** False\
**signatureGeneration:** Generic

### EddsaVerify

**curve:** edwards25519\
**cofactored:** False\
**encoding:** JWK

### Ecdh

**primitive:** Ecdh\
**curve:** brainpoolP224r1, brainpoolP224t1, brainpoolP256r1, brainpoolP256t1,
brainpoolP320r1, brainpoolP320t1, brainpoolP384r1, brainpoolP384t1,
brainpoolP512r1, brainpoolP512t1, secp160r1, secp192r1, secp224r1, secp256k1,
secp256r1, secp384r1, secp521r1, sm2\
**encoding:** DER, JWK, UNCOMPRESSED

### RsaPkcs1Verify

**primitive:** RsaSsaPkcs1\
**size:** 1024, 1536, 2048, 3072, 4096\
**sha:** SHA-1, SHA-256, SHA-384, SHA-512\
**encoding:** DER

### RsaPssVerify

**primitive:** RsaSsaPss\
**size:** 1024, 1536, 2048, 3072, 4096\
**sha:** SHA-1, SHA-256, SHA-384, SHA-512\
**mgf:** MGF1\
**mgfSha:** SHA-1, SHA-256, SHA-384, SHA-512\
**saltLen:** 0, 20, 32, 48, 64\
**encoding:** DER

### RsaEsOaepDecrypt

**size:** 1024, 2048, 3072, 4096\
**sha:** SHA-1, SHA-256, SHA-384, SHA-512\
**mgf:** MGF1\
**mgfSha:** SHA-1, SHA-256, SHA-384, SHA-512

# browserify-sign

**Language:**
javascript\
**Url:**
[https://www.npmjs.com/package/browserify-sign](https://www.npmjs.com/package/browserify-sign)

browserify-sign is a reimplementation of the cryptographic library in node.js.
Using the same interface as node.js simplifies porting implementations from one library to the other.

## Security

browserify-sign is currently using the npm libraries elliptic and bn.js.
Both libraries have are no longer well mainteined.
As a result, vulnerabilities are slowly fixed or not at all.

## Performed tests

### DsaVerify

| primitive | pLen | qLen | sha | encoding | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Dsa | 1024, 2048, 3072 | 160, 224, 256 | SHA-1, SHA-224, SHA-256 | DER | Generic |

### DsaSign

| primitive | pLen | qLen | sha | encoding | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Dsa | 1024, 2048, 3072 | 160, 224, 256 | SHA-1, SHA-224, SHA-256, SHA-512 | DER | Rfc6979 |

### EcdsaVerify

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | secp192r1, secp224r1, secp256k1, secp256r1, secp384r1, secp521r1 | SHA-224, SHA-256, SHA-384, SHA-512 | DER | False | Generic |

### RsaPkcs1Verify

| primitive | size | sha | encoding |
| --- | --- | --- | --- |
| RsaSsaPkcs1 | 1024, 1536, 2048, 3072, 4096 | SHA-1, SHA-224, SHA-256, SHA-384, SHA-512 | DER |

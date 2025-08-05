# elliptic

**Language:** javascript\
**Url:**
[https://www.npmjs.com/package/elliptic](https://www.npmjs.com/package/elliptic)

## Security

This library fixes vulnerabilities very slowly. An example is CVE-2024-48948,
which is an issue found in July, 2024. The issue was later found to be critical,
as it leaks private key in some cases. Version 6.6.1, is still suceptible to the
vulnerability. Currently (July, 2025) no fixed version is available. Ecdh, ECDSA
and EdDSA are not constant time.

## Performed tests

### EcdsaVerify

**curve:** secp192r1, secp224r1, secp256k1, secp256r1, secp384r1, secp521r1\
**sha:** SHA-256, SHA-384, SHA-512\
**encoding:** DER\
**normalize:** False\
**signatureGeneration:** Generic

### EcdsaSign

**curve:** secp192r1, secp224r1, secp256k1, secp256r1, secp384r1, secp521r1\
**sha:** SHA-256, SHA-384, SHA-512\
**encoding:** DER\
**normalize:** False\
**signatureGeneration:** Rfc6979

### EddsaVerify

**curve:** edwards25519\
**cofactored:** False\
**encoding:** RAW

### EddsaSign

**curve:** edwards25519\
**cofactored:** False\
**encoding:** RAW

### Ecdh

**primitive:** Ecdh\
**curve:** secp192r1, secp224r1, secp256k1, secp256r1, secp384r1, secp521r1\
**encoding:** UNCOMPRESSED

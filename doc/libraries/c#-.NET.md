# .NET

**Language:** c#\
**Url:**
[https://learn.microsoft.com/en-us/dotnet/standard/security/cryptography-model](https://learn.microsoft.com/en-us/dotnet/standard/security/cryptography-model)

The .NET cryptography library is a cross-platform library. The availability of
algorithms depends on the operating system it runs on. Currently (2025) all
tests are performed on a Windows OS.

## Performed tests

### Aead

**primitive:** AesCcm, AesGcm\
**keySize:** 128, 192, 256\
**ivSize:** 88, 96, 104\
**tagSize:** 64, 96, 128\
Nonce size for GCM is restricted to 12 bytes. Tag size for GCM must be at least
12 bytes.

### IndCpa

**primitive:** AesCbcPkcs7, AesCfb128Pkcs7, AesCfb8\
**keySize:** 128, 192, 256\
**ivSize:** 128\
**cipher:** Aes\
**mode:** Cbc, Cfb\
**padding:** Pkcs7\
**paddingSize:** 128\
**feedback:** 8, 128\
The library requires that the size of the input for the CFB mode is a multiple
of the feedback size. Because of this CFB with PKCS7 padding is tested, but not
CFB without padding.

### DsaVerify

**pLen:** 1024, 2048, 3072\
**qLen:** 160, 256\
**sha:** SHA-1, SHA-256, SHA-512\
**encoding:** DER, P1363\
**signatureGeneration:** Generic

### EcdsaVerify

**curve:** brainpoolP192r1, brainpoolP192t1, brainpoolP224r1, brainpoolP224t1,
brainpoolP256r1, brainpoolP256t1, brainpoolP320r1, brainpoolP320t1,
brainpoolP384r1, brainpoolP384t1, brainpoolP512r1, brainpoolP512t1, secp256r1,
secp384r1, secp521r1\
**sha:** SHA-256, SHA-384, SHA-512\
**encoding:** DER, P1363\
**normalize:** False\
**signatureGeneration:** Generic\
Support for SHA-3 is platform dependent.

### Ecdh

**primitive:** Ecdh\
**curve:** brainpoolP224r1, brainpoolP224t1, brainpoolP256r1, brainpoolP256t1,
brainpoolP320r1, brainpoolP320t1, brainpoolP384r1, brainpoolP384t1,
brainpoolP512r1, brainpoolP512t1, secp256r1, secp384r1, secp521r1\
**encoding:** UNCOMPRESSED

### Mac

**primitive:** HmacSha1, HmacSha256, HmacSha384, HmacSha512\
**macSize:** 160, 256, 384, 512

### Pbkdf

**primitive:** Pbkdf\
**sha:** SHA-1, SHA-256, SHA-384, SHA-512

### Hkdf

**primitive:** HkdfSha1, HkdfSha256, HkdfSha384, HkdfSha512\
**sha:** SHA-1, SHA-256, SHA-384, SHA-512

### Pkcs8Decrypt

**primitive:** Pkcs8\
**sha:** SHA-1, SHA-256, SHA-512\
**cipher:** AES-CBC-128, AES-CBC-192, AES-CBC-256, DES-EDE3-CBC

### RsaPkcs1Verify

**primitive:** RsaSsaPkcs1\
**size:** 2048, 3072, 4096\
**sha:** SHA-256, SHA-384, SHA-512\
**encoding:** DER

### RsaPssVerify

**primitive:** RsaSsaPss\
**size:** 2048, 3072, 4096\
**sha:** SHA-256, SHA-384, SHA-512\
**mgf:** MGF1\
**mgfSha:** SHA-256, SHA-384, SHA-512\
**saltLen:** 32, 48, 64\
**encoding:** DER

### RsaEsPkcs1Decrypt

**size:** 1024, 2048, 3072, 4096

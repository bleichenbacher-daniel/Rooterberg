# .NET

**Language:**
c#\
**Url:**
[https://learn.microsoft.com/en-us/dotnet/standard/security/cryptography-model](https://learn.microsoft.com/en-us/dotnet/standard/security/cryptography-model)\
**Tested version:**
10.0.0

The .NET cryptography library is a cross-platform library.
The availability of algorithms depends on the operating system it runs on.
Currently (2025) all tests are performed on a Windows OS.

## Performed tests

### Aead

| primitive | keySize | ivSize | tagSize |
| --- | --- | --- | --- |
| AesGcm | 128, 192, 256 | 96 | 96, 128 |
| AesCcm | 128, 192, 256 | 88, 96, 104 | 64, 96, 128 |

Nonce size for GCM is restricted to 12 bytes.
Tag size for GCM must be at least 12 bytes.

### IndCpa

| primitive | keySize | ivSize | cipher | mode | padding | paddingSize | feedback |
| --- | --- | --- | --- | --- | --- | --- | --- |
| AesCbcPkcs7 | 128, 192, 256 | 128 | Aes | Cbc | Pkcs7 | 128 | |
| AesCfb8 | 128, 192, 256 | 128 | Aes | Cfb | | | 8 |
| AesCfb128Pkcs7 | 128, 192, 256 | 128 | Aes | Cfb | Pkcs7 | 128 | 128 |

The library requires that the size of the input for the CFB mode is a multiple of the feedback size.
Because of this CFB with PKCS7 padding is tested, but not CFB without padding.

### DsaVerify

| primitive | pLen | qLen | sha | encoding | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Dsa | 1024, 2048, 3072 | 160, 256 | SHA-1, SHA-256, SHA-512 | DER, P1363 | Generic |

### EcdsaVerify

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | brainpoolP192r1, brainpoolP192t1, brainpoolP224r1, brainpoolP224t1, brainpoolP256r1, brainpoolP256t1, brainpoolP320r1, brainpoolP320t1, brainpoolP384r1, brainpoolP384t1, brainpoolP512r1, brainpoolP512t1, secp256r1, secp384r1, secp521r1 | SHA-256, SHA-384, SHA-512 | DER, P1363 | False | Generic |

Support for SHA-3 is platform dependent.

### Ecdh

| primitive | curve | encoding |
| --- | --- | --- |
| Ecdh | brainpoolP224r1, brainpoolP224t1, brainpoolP256r1, brainpoolP256t1, brainpoolP320r1, brainpoolP320t1, brainpoolP384r1, brainpoolP384t1, brainpoolP512r1, brainpoolP512t1, secp256r1, secp384r1, secp521r1 | UNCOMPRESSED |

### Mac

| primitive | macSize |
| --- | --- |
| HmacSha1 | 160 |
| HmacSha256 | 256 |
| HmacSha384 | 384 |
| HmacSha512 | 512 |

### Pbkdf

| primitive | sha |
| --- | --- |
| Pbkdf | SHA-1, SHA-256, SHA-384, SHA-512 |

### Hkdf

| primitive | sha |
| --- | --- |
| HkdfSha1 | SHA-1 |
| HkdfSha256 | SHA-256 |
| HkdfSha384 | SHA-384 |
| HkdfSha512 | SHA-512 |

### Pkcs8Decrypt

| primitive | sha | cipher |
| --- | --- | --- |
| Pkcs8 | SHA-1, SHA-256, SHA-512 | AES-CBC-128, AES-CBC-192, AES-CBC-256, DES-EDE3-CBC |

### RsaPkcs1Verify

| primitive | size | sha | encoding |
| --- | --- | --- | --- |
| RsaSsaPkcs1 | 2048, 3072, 4096 | SHA-256, SHA-384, SHA-512 | DER |

### RsaPssVerify

| primitive | size | sha | mgf | mgfSha | saltLen | encoding |
| --- | --- | --- | --- | --- | --- | --- |
| RsaSsaPss | 2048, 3072, 4096 | SHA-256, SHA-384, SHA-512 | MGF1 | SHA-256, SHA-384, SHA-512 | 32, 48, 64 | DER |

### RsaEsPkcs1Decrypt

| primitive | size |
| --- | --- |
| RsaEsPkcs1 | 1024, 2048, 3072, 4096 |

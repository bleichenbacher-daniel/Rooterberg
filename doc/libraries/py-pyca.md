# pyca

**Language:**
python\
**Url:**
[https://cryptography.io/en/latest/](https://cryptography.io/en/latest/)

The library can be built against different underlying libraries.
The tests are based on the version using 'pip install cryptography'.

## Performed tests

### Aead

| primitive | keySize | ivSize | tagSize |
| --- | --- | --- | --- |
| AeadAesCmacSiv | 256, 384, 512 | 96, 128 | 128 |
| Chacha20Poly1305 | 256 | 96 | 128 |
| AesGcm | 128, 192, 256 | 64, 96, 128, 256 | 128 |
| AesGcmSiv | 128, 192, 256 | 96 | 128 |
| AesCcm | 128, 192, 256 | 88 | 128 |
| AesOcb | 128, 192, 256 | 96, 120 | 128 |

### Xdh

| primitive | curve | encoding |
| --- | --- | --- |
| x25519 | curve25519 | PEM, RAW |
| x448 | curve448 | PEM, RAW |

### Daead

| primitive | keySize | tagSize |
| --- | --- | --- |
| DaeadAesCmacSiv | 256, 384, 512 | 128 |

### IndCpa

| primitive | keySize | ivSize | cipher | mode | padding | paddingSize | feedback |
| --- | --- | --- | --- | --- | --- | --- | --- |
| AesXts | 256, 512 | 128 | Aes | Xts | | | |
| AesCbcPkcs7 | 128, 192, 256 | 128 | Aes | Cbc | Pkcs7 | 128 | |
| CamelliaCbcPkcs7 | 128, 192, 256 | 128 | Camellia | Cbc | Pkcs7 | 128 | |
| Sm4CbcPkcs7 | 128 | 128 | SM4 | Cbc | Pkcs7 | 128 | |
| AesCfb8 | 128, 192, 256 | 128 | Aes | Cfb | | | 8 |
| AesCfb128 | 128, 192, 256 | 128 | Aes | Cfb | | | 128 |
| AesCfb128Pkcs7 | 128, 192, 256 | 128 | Aes | Cfb | Pkcs7 | 128 | 128 |
| CamelliaCfb128 | 128, 192, 256 | 128 | Camellia | Cfb | | | 128 |
| Sm4Cfb128 | 128 | 128 | SM4 | Cfb | | | 128 |
| AesOfb | 128, 192, 256 | 128 | Aes | Ofb | | | |
| CamelliaOfb | 128, 192, 256 | 128 | Camellia | Ofb | | | |
| Sm4Ofb | 128 | 128 | SM4 | Ofb | | | |

### BlockCipher

| primitive | keySize |
| --- | --- |
| Aes | 128, 192, 256 |
| Camellia | 128, 192, 256 |
| SM4 | 128 |
| Seed | 128 |
| Cast128 | 128 |
| TripleDes | 192 |

### DsaVerify

| primitive | pLen | qLen | sha | encoding | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Dsa | 1024, 2048, 3072 | 160, 224, 256 | SHA-1, SHA-224, SHA-256, SHA-512 | DER | Generic |

### EcdsaVerify

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | brainpoolP256r1, brainpoolP384r1, brainpoolP512r1, secp192r1, secp224r1, secp256k1, secp256r1, secp384r1, secp521r1, sect233k1, sect283k1 | SHA-224, SHA-256, SHA-384, SHA-512, SHA3-256, SHA3-384, SHA3-512, SHAKE128, SHAKE256 | DER | False | Generic |

### EcdsaSign

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | brainpoolP256r1, brainpoolP384r1, brainpoolP512r1, secp192r1, secp224r1, secp256k1, secp256r1, secp384r1, secp521r1 | SHA-224, SHA-256, SHA-384, SHA-512, SHA3-256, SHA3-384, SHA3-512 | DER | False | Rfc6979 |

### EddsaVerify

| primitive | curve | cofactored | encoding |
| --- | --- | --- | --- |
| Eddsa | edwards25519, edwards448 | False | RAW |

### EddsaSign

| primitive | curve | cofactored | encoding |
| --- | --- | --- | --- |
| Eddsa | edwards25519, edwards448 | False | RAW |

### Ecdh

| primitive | curve | encoding |
| --- | --- | --- |
| Ecdh | brainpoolP256r1, brainpoolP384r1, brainpoolP512r1, secp192r1, secp224r1, secp256k1, secp256r1, secp384r1, secp521r1, sect233k1, sect283k1, sect409k1, sect571k1 | DER, PEM |

### KeyWrap

| primitive | keySize |
| --- | --- |
| AesKw | 128, 192, 256 |
| AesKwp | 128, 192, 256 |
| AesSivKw | 256, 384, 512 |

### Mac

| primitive | keySize | macSize |
| --- | --- | --- |
| AesCmac | 128, 192, 256 | 128 |
| CamelliaCmac | 128, 192, 256 | 128 |
| HmacSha1 | | 160 |
| HmacSha224 | | 224 |
| HmacSha256 | | 256 |
| HmacSha384 | | 384 |
| HmacSha512 | | 512 |
| HmacSha3_224 | | 224 |
| HmacSha3_256 | | 256 |
| HmacSha3_384 | | 384 |
| HmacSha3_512 | | 512 |

### Pbkdf

| primitive | sha |
| --- | --- |
| Pbkdf | SHA-1, SHA-224, SHA-256, SHA-384, SHA-512, SHA-512/224, SHA-512/256, SHA3-224, SHA3-256, SHA3-384, SHA3-512 |

### Scrypt

| primitive |
| --- |
| Pbkdf |

### Kdf

| primitive | sha |
| --- | --- |
| X963KdfSha1 | SHA-1 |
| X963KdfSha224 | SHA-224 |
| X963KdfSha256 | SHA-256 |
| X963KdfSha384 | SHA-384 |
| X963KdfSha512 | SHA-512 |

### Hkdf

| primitive | sha |
| --- | --- |
| HkdfSha1 | SHA-1 |
| HkdfSha224 | SHA-224 |
| HkdfSha256 | SHA-256 |
| HkdfSha384 | SHA-384 |
| HkdfSha512 | SHA-512 |
| HkdfSha512_224 | SHA-512/224 |
| HkdfSha512_256 | SHA-512/256 |
| HkdfSha3_224 | SHA3-224 |
| HkdfSha3_256 | SHA3-256 |
| HkdfSha3_384 | SHA3-384 |
| HkdfSha3_512 | SHA3-512 |

### Pkcs8Decrypt

| primitive | sha | cipher |
| --- | --- | --- |
| Pkcs8 | SHA-1, SHA-256 | AES-CBC-128, AES-CBC-192, AES-CBC-256, AES-GCM-128, AES-GCM-192, AES-GCM-256, DES-EDE3-CBC |
| Pkcs8Scrypt | | AES-CBC-128, AES-CBC-192, AES-CBC-256, AES-GCM-128, AES-GCM-192, AES-GCM-256 |

### RsaPkcs1Verify

| primitive | size | sha | encoding |
| --- | --- | --- | --- |
| RsaSsaPkcs1 | 1024, 1536, 2048, 3072, 4096 | SHA-1, SHA-224, SHA-256, SHA-384, SHA-512, SHA3-256, SHA3-384, SHA3-512 | DER |

### RsaPssVerify

| primitive | size | sha | mgf | mgfSha | saltLen | encoding |
| --- | --- | --- | --- | --- | --- | --- |
| RsaSsaPss | 1024, 1536, 2048, 3072, 4096 | SHA-1, SHA-224, SHA-256, SHA-384, SHA-512 | MGF1 | SHA-1, SHA-224, SHA-256, SHA-384, SHA-512 | 0, 20, 28, 32, 48, 64 | DER |

### RsaEsPkcs1Decrypt

| primitive | size |
| --- | --- |
| RsaEsPkcs1 | 1024, 2048, 3072, 4096 |

### RsaEsOaepDecrypt

| primitive | size | sha | mgf | mgfSha |
| --- | --- | --- | --- | --- |
| RsaEsOaep | 1024, 2048, 3072, 4096 | SHA-1, SHA-224, SHA-256, SHA-384, SHA-512 | MGF1 | SHA-1, SHA-224, SHA-256, SHA-384, SHA-512 |

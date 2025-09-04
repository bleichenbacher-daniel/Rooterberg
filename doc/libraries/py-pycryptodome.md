# pycryptodome

**Language:**
python\
**Url:**
[https://pypi.org/project/pycryptodome/](https://pypi.org/project/pycryptodome/)\
**Tested version:**
3.22.0

## Security

Some of the primitives do not have constant time implementations.

## Performed tests

### Aead

| primitive | keySize | ivSize | tagSize |
| --- | --- | --- | --- |
| AeadAesCmacSiv | 256, 384, 512 | 96, 128 | 128 |
| AesGcm | 128, 192, 256 | 64, 96, 128, 256 | 64, 96, 128 |
| AesCcm | 128, 192, 256 | 88, 96, 104 | 64, 96, 128 |
| AesEax | 128, 192, 256 | 128 | 128 |
| AesOcb | 128, 192, 256 | 96, 120 | 64, 96, 128 |

### Xdh

| primitive | curve | encoding |
| --- | --- | --- |
| x25519 | curve25519 | RAW |
| x448 | curve448 | RAW |

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
| Cast128 | 128 |
| Des | 64 |
| TripleDes | 192 |

### DsaVerify

| primitive | pLen | qLen | sha | encoding | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Dsa | 1024, 2048, 3072 | 160, 224, 256 | SHA-1, SHA-224, SHA-256, SHA-512 | P1363 | Generic |

### DsaSign

| primitive | pLen | qLen | sha | encoding | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Dsa | 1024, 2048, 3072 | 160, 224, 256 | SHA-1, SHA-224, SHA-256, SHA-512 | P1363 | Rfc6979 |

### EcdsaVerify

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | secp192r1, secp224r1, secp256r1, secp384r1, secp521r1 | SHA-224, SHA-256, SHA-384, SHA-512, SHA3-256, SHA3-384, SHA3-512 | P1363 | False | Generic |

### EcdsaSign

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | secp192r1, secp224r1, secp256r1, secp384r1, secp521r1 | SHA-224, SHA-256, SHA-384, SHA-512, SHA3-256, SHA3-384, SHA3-512 | P1363 | False | Rfc6979 |

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
| Ecdh | secp192r1, secp224r1, secp256r1, secp384r1, secp521r1 | DER, PEM |

### KeyWrap

| primitive | keySize |
| --- | --- |
| AesKw | 128, 192, 256 |
| AesKwp | 128, 192, 256 |
| AesSivKw | 256, 384, 512 |

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
| ripemd160 | 160 |
| keccak224 | 224 |
| keccak256 | 256 |
| keccak384 | 384 |
| keccak512 | 512 |
| shake128 | 256 |
| shake256 | 512 |
| blake2b | 512 |
| blake2s | 256 |

### Mac

| primitive | keySize | macSize |
| --- | --- | --- |
| AesCmac | 128, 192, 256 | 96, 128 |
| HmacSha1 | | 160 |
| HmacSha224 | | 224 |
| HmacSha256 | | 256 |
| HmacSha384 | | 384 |
| HmacSha512 | | 512 |
| HmacSha3_224 | | 224 |
| HmacSha3_256 | | 256 |
| HmacSha3_384 | | 384 |
| HmacSha3_512 | | 512 |
| Kmac128 | 128 | 128, 256 |
| Kmac256 | 256 | 256, 512 |

### Xof

| primitive |
| --- |
| Shake128 |
| Shake256 |
| KangarooTwelve |

### Pbkdf

| primitive | sha |
| --- | --- |
| Pbkdf | SHA-1, SHA-224, SHA-256, SHA-384, SHA-512, SHA3-224, SHA3-256, SHA3-384, SHA3-512 |

### Scrypt

| primitive |
| --- |
| Pbkdf |

### Hkdf

| primitive | sha |
| --- | --- |
| HkdfSha1 | SHA-1 |
| HkdfSha224 | SHA-224 |
| HkdfSha256 | SHA-256 |
| HkdfSha384 | SHA-384 |
| HkdfSha512 | SHA-512 |
| HkdfSha3_224 | SHA3-224 |
| HkdfSha3_256 | SHA3-256 |
| HkdfSha3_384 | SHA3-384 |
| HkdfSha3_512 | SHA3-512 |

### Pkcs8Decrypt

| primitive | sha | cipher |
| --- | --- | --- |
| Pkcs8 | SHA-1, SHA-256, SHA-512, SHA3-256, SHA3-512 | AES-CBC-128, AES-CBC-192, AES-CBC-256, AES-GCM-128, AES-GCM-192, AES-GCM-256, DES-EDE3-CBC |
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
| RsaEsOaep | 1024, 2048, 3072, 4096 | SHA-1, SHA-224, SHA-256, SHA-384, SHA-512, SHA3-224, SHA3-256, SHA3-384, SHA3-512 | MGF1 | SHA-1, SHA-224, SHA-256, SHA-384, SHA-512, SHA3-224, SHA3-256, SHA3-384, SHA3-512 |

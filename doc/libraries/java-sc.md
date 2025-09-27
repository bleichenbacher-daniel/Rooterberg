# SC

**Language:**
java\
**Url:**
[https://github.com/rtyley/spongycastle](https://github.com/rtyley/spongycastle)\
**Tested version:**
1.58

SpongyCastle is a fork of an old version of BouncyCastle.
The motivation for this fork was to allow applications to use different version of BouncyCastle than the one preinstalled on Android devices.
SpongyCastle is no longer maintained.

## Security

The library contains known bugs and vulnerabilities, since it is no longer updated.
Switching to BouncyCastle or an alternative provider is recommended.

## Performed tests

### Aead

| primitive | keySize | ivSize | tagSize |
| --- | --- | --- | --- |
| AesGcm | 128, 192, 256 | 64, 96, 128, 256 | 64, 96, 128 |
| AriaGcm | 128, 192, 256 | 96 | 128 |
| CamelliaGcm | 128, 192, 256 | 96 | 128 |
| SeedGcm | 128 | 96 | 80, 128 |
| Sm4Gcm | 128 | 96 | 128 |
| SerpentGcm | 128, 256 | 96 | 128 |
| TwofishGcm | 128, 256 | 96 | 128 |
| AesGcmSiv | 128, 256 | 96 | 128 |
| AesCcm | 128, 192, 256 | 88, 96, 104 | 64, 96, 128 |
| CamelliaCcm | 128, 192, 256 | 104 | 64, 80 |
| SeedCcm | 128 | 96 | 80, 128 |
| Sm4Ccm | 128 | 96 | 128 |
| AriaCcm | 128, 192, 256 | 96, 104 | 64, 128 |
| AesEax | 128, 192, 256 | 128 | 64, 128 |
| CamelliaEax | 128, 192, 256 | 128 | 128 |
| TwofishEax | 256 | 128 | 128 |
| AesOcb | 128, 192, 256 | 96, 120 | 64, 96, 128 |
| CamelliaOcb | 128, 192, 256 | 120 | 128 |
| TwofishOcb | 256 | 120 | 128 |
| SerpentOcb | 128, 256 | 120 | 128 |

SpongyCastle implements an old version of AES-GCM-SIV. This version is not compatible with RFC 8452.

### IndCpa

| primitive | keySize | ivSize | cipher | mode | padding | paddingSize | feedback |
| --- | --- | --- | --- | --- | --- | --- | --- |
| AesCbcPkcs7 | 128, 192, 256 | 128 | Aes | Cbc | Pkcs7 | 128 | |
| AriaCbcPkcs7 | 128, 192, 256 | 128 | Aria | Cbc | Pkcs7 | 128 | |
| CamelliaCbcPkcs7 | 128, 192, 256 | 128 | Camellia | Cbc | Pkcs7 | 128 | |
| SeedCbcPkcs7 | 128 | 128 | Seed | Cbc | Pkcs7 | 128 | |
| Sm4CbcPkcs7 | 128 | 128 | SM4 | Cbc | Pkcs7 | 128 | |
| SerpentCbcPkcs7 | 128, 160, 192, 224, 256 | 128 | Serpent | Cbc | Pkcs7 | 128 | |
| TwofishCbcPkcs7 | 128, 192, 256 | 128 | Twofish | Cbc | Pkcs7 | 128 | |
| TripleDesCbcPkcs7 | 192 | 64 | TripleDes | Cbc | Pkcs7 | 64 | |
| AesCbcCs3 | 128, 192, 256 | 128 | Aes | Cs3 | | | |
| Sm4CbcCs3 | 128 | 128 | SM4 | Cs3 | | | |
| AesCfb8 | 128, 192, 256 | 128 | Aes | Cfb | | | 8 |
| AesCfb128 | 128, 192, 256 | 128 | Aes | Cfb | | | 128 |
| AesCfb128Pkcs7 | 128, 192, 256 | 128 | Aes | Cfb | Pkcs7 | 128 | 128 |
| AriaCfb8 | 128, 192, 256 | 128 | Aria | Cfb | | | 8 |
| AriaCfb128 | 128, 192, 256 | 128 | Aria | Cfb | | | 128 |
| CamelliaCfb8 | 128, 192, 256 | 128 | Camellia | Cfb | | | 8 |
| CamelliaCfb128 | 128, 192, 256 | 128 | Camellia | Cfb | | | 128 |
| SeedCfb8 | 128 | 128 | Seed | Cfb | | | 8 |
| SeedCfb128 | 128 | 128 | Seed | Cfb | | | 128 |
| Sm4Cfb8 | 128 | 128 | SM4 | Cfb | | | 8 |
| Sm4Cfb128 | 128 | 128 | SM4 | Cfb | | | 128 |
| SerpentCfb8 | 128, 160, 192, 224, 256 | 128 | Serpent | Cfb | | | 8 |
| SerpentCfb128 | 128, 160, 192, 224, 256 | 128 | Serpent | Cfb | | | 128 |
| TripleDesCfb8 | 192 | 64 | TripleDes | Cfb | | | 8 |
| TripleDesCfb64 | 192 | 64 | TripleDes | Cfb | | | 64 |
| AesOfb | 128, 192, 256 | 128 | Aes | Ofb | | | |
| AriaOfb | 128, 192, 256 | 128 | Aria | Ofb | | | |
| CamelliaOfb | 128, 192, 256 | 128 | Camellia | Ofb | | | |
| Sm4Ofb | 128 | 128 | SM4 | Ofb | | | |
| SeedOfb | 128 | 128 | Seed | Ofb | | | |
| TripleDesOfb | 192 | 64 | TripleDes | Ofb | | | |
| Salsa20 | 256 | 64 | | | | | |
| XSalsa20 | 256 | 192 | | | | | |
| HC256 | 256 | 256 | | | | | |

### BlockCipher

| primitive | keySize |
| --- | --- |
| Aes | 128, 192, 256 |
| Aria | 128, 192, 256 |
| Camellia | 128, 192, 256 |
| SM4 | 128 |
| Seed | 128 |
| Twofish | 128, 192, 256 |
| Serpent | 128, 160, 192, 224, 256 |
| Rc5_32_12_16 | 128 |
| Xtea | 128 |
| Cast128 | 128 |
| Idea | 128 |
| Des | 64 |
| TripleDes | 192 |

### DsaVerify

| primitive | pLen | qLen | sha | encoding | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Dsa | 1024, 2048, 3072 | 160, 224, 256 | SHA-1, SHA-224, SHA-256, SHA-512 | DER | Generic |

### DsaSign

| primitive | pLen | qLen | sha | encoding | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Dsa | 1024, 2048, 3072 | 160, 224, 256 | SHA-1, SHA-224, SHA-256, SHA-512 | DER | Rfc6979 |

### EcdsaVerify

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | brainpoolP192r1, brainpoolP192t1, brainpoolP224r1, brainpoolP224t1, brainpoolP256r1, brainpoolP256t1, brainpoolP320r1, brainpoolP320t1, brainpoolP384r1, brainpoolP384t1, brainpoolP512r1, brainpoolP512t1, frp256v1, prime192v2, prime239v1, secp160r1, secp192k1, secp192r1, secp224k1, secp224r1, secp256k1, secp256r1, secp384r1, secp521r1, sect233k1, sect233r1, sect283k1 | SHA-224, SHA-256, SHA-384, SHA-512, SHA3-256, SHA3-384, SHA3-512 | DER, P1363 | False | Generic |

### EcdsaSign

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | brainpoolP192r1, brainpoolP192t1, brainpoolP224r1, brainpoolP224t1, brainpoolP256r1, brainpoolP256t1, brainpoolP320r1, brainpoolP320t1, brainpoolP384r1, brainpoolP384t1, brainpoolP512r1, brainpoolP512t1, frp256v1, prime192v2, prime239v1, secp160r1, secp192k1, secp192r1, secp224k1, secp224r1, secp256k1, secp256r1, secp384r1, secp521r1 | SHA-224, SHA-256, SHA-384, SHA-512, SHA3-256, SHA3-384, SHA3-512 | DER | False | Rfc6979 |

The signing operation is not constant time.
It has a timing side channel that leaks information about k.
No similar leakage can be observed in new versions of BouncyCastle.

### Ecdh

| primitive | curve | encoding |
| --- | --- | --- |
| Ecdh | brainpoolP192r1, brainpoolP192t1, brainpoolP224r1, brainpoolP224t1, brainpoolP256r1, brainpoolP256t1, brainpoolP320r1, brainpoolP320t1, brainpoolP384r1, brainpoolP384t1, brainpoolP512r1, brainpoolP512t1, frp256v1, prime192v2, prime239v1, secp160r1, secp192k1, secp192r1, secp224k1, secp224r1, secp256k1, secp256r1, secp384r1, secp521r1, sect233k1, sect233r1, sect283k1 | DER |

### KeyWrap

| primitive | keySize |
| --- | --- |
| AesKw | 128, 192, 256 |
| AesKwp | 128, 192, 256 |
| AriaKw | 128, 192, 256 |
| AriaKwp | 128, 192, 256 |
| CamelliaKw | 128, 192, 256 |
| SeedKw | 128 |

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
| sm3 | 256 |
| blake2b | 512 |

### Mac

| primitive | keySize | macSize |
| --- | --- | --- |
| AesCmac | 128, 192, 256 | 128 |
| Sm4Cmac | 128 | 128 |
| SeedCmac | 128 | 128 |
| HmacSha1 | | 160 |
| HmacSha224 | | 224 |
| HmacSha256 | | 256 |
| HmacSha384 | | 384 |
| HmacSha512 | | 512 |
| HmacSha512_224 | | 224 |
| HmacSha512_256 | | 256 |
| HmacSha3_224 | | 224 |
| HmacSha3_256 | | 256 |
| HmacSha3_384 | | 384 |
| HmacSha3_512 | | 512 |
| SipHash24 | 128 | 64 |
| SipHash48 | 128 | 64 |

### Pbkdf

| primitive | sha |
| --- | --- |
| Pbkdf | SHA-1, SHA-224, SHA-256, SHA-384, SHA-512, SHA3-224, SHA3-256, SHA3-384, SHA3-512 |

### Pbes2

| primitive | sha | cipher | keySize |
| --- | --- | --- | --- |
| Pbes2 | SHA-1, SHA-256 | Aes | 128, 192, 256 |

### RsaPkcs1Verify

| primitive | size | sha | encoding |
| --- | --- | --- | --- |
| RsaSsaPkcs1 | 1024, 1536, 2048, 3072, 4096 | SHA-1, SHA-224, SHA-256, SHA-384, SHA-512, SHA3-256, SHA3-384, SHA3-512 | DER |

### RsaPssVerify

| primitive | size | sha | mgf | mgfSha | saltLen | encoding |
| --- | --- | --- | --- | --- | --- | --- |
| RsaSsaPss | 1024, 1536, 2048, 3072, 4096 | SHA-1, SHA-224, SHA-256, SHA-384, SHA-512 | MGF1 | SHA-1, SHA-224, SHA-256, SHA-384, SHA-512 | 0, 20, 28, 32, 48, 64 | DER |

A smaller bug in the verification accepts some invalid signatures.

### RsaEsPkcs1Decrypt

| primitive | size |
| --- | --- |
| RsaEsPkcs1 | 1024, 2048, 3072, 4096 |

### RsaEsOaepDecrypt

| primitive | size | sha | mgf | mgfSha |
| --- | --- | --- | --- | --- |
| RsaEsOaep | 1024, 2048, 3072, 4096 | SHA-1, SHA-224, SHA-256, SHA-384, SHA-512, SHA3-224, SHA3-256, SHA3-384, SHA3-512 | MGF1 | SHA-1, SHA-224, SHA-256, SHA-384, SHA-512, SHA3-224, SHA3-256, SHA3-384, SHA3-512 |

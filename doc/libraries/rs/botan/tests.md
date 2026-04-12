# Performed tests for botan

## Aead

| primitive | keySize | ivSize | tagSize |
| --- | --- | --- | --- |
| AeadAesCmacSiv | 256, 512 | 128 | 128 |
| Chacha20Poly1305 | 256 | 96 | 128 |
| AesGcm | 128, 192, 256 | 64, 96, 128, 256 | 96, 128 |
| AriaGcm | 128, 192, 256 | 96 | 128 |
| CamelliaGcm | 128, 192, 256 | 96 | 128 |
| AesCcm | 128, 192, 256 | 88, 96, 104 | 64, 96 |
| CamelliaCcm | 128, 192, 256 | 104 | 64, 80 |
| SeedCcm | 128 | 96 | 80, 128 |
| Sm4Ccm | 128 | 96 | 128 |
| AriaCcm | 128, 192, 256 | 96, 104 | 64, 128 |
| AesEax | 128, 192, 256 | 128 | 64, 128 |
| CamelliaEax | 128, 192, 256 | 128 | 128 |
| AesOcb | 128, 192, 256 | 96 | 64, 96, 128 |
| CamelliaOcb | 128, 192, 256 | 120 | 128 |
| TwofishOcb | 256 | 120 | 128 |
| SerpentOcb | 128, 256 | 120 | 128 |

## IndCpa

| primitive | keySize | ivSize | cipher | mode | padding | paddingSize | feedback |
| --- | --- | --- | --- | --- | --- | --- | --- |
| AesXts | 256, 384, 512 | 128 | Aes | Xts | | | |
| Sm4Xts | 256 | 128 | SM4 | Xts | | | |
| TwofishXts | 256, 512 | 128 | Twofish | Xts | | | |
| SerpentXts | 256 | 128 | Serpent | Xts | | | |
| CamelliaXts | 256, 512 | 128 | Camellia | Xts | | | |
| AesCbcPkcs7 | 128, 192, 256 | 128 | Aes | Cbc | Pkcs7 | 128 | |
| AesCbcIso7816 | 128, 192, 256 | 128 | Aes | Cbc | Iso7816Padding | 128 | |
| AriaCbcPkcs7 | 128, 192, 256 | 128 | Aria | Cbc | Pkcs7 | 128 | |
| CamelliaCbcPkcs7 | 128, 192, 256 | 128 | Camellia | Cbc | Pkcs7 | 128 | |
| SeedCbcPkcs7 | 128 | 128 | Seed | Cbc | Pkcs7 | 128 | |
| Sm4CbcPkcs7 | 128 | 128 | SM4 | Cbc | Pkcs7 | 128 | |
| SerpentCbcPkcs7 | 128, 192, 256 | 128 | Serpent | Cbc | Pkcs7 | 128 | |
| TwofishCbcPkcs7 | 128, 192, 256 | 128 | Twofish | Cbc | Pkcs7 | 128 | |
| TripleDesCbcPkcs7 | 192 | 64 | TripleDes | Cbc | Pkcs7 | 64 | |
| AesCbcCs3 | 128, 192, 256 | 128 | Aes | Cs3 | | | |
| AesCfb8 | 128, 192, 256 | 128 | Aes | Cfb | | | 8 |
| AesCfb128 | 128, 192, 256 | 128 | Aes | Cfb | | | 128 |
| AriaCfb8 | 128, 192, 256 | 128 | Aria | Cfb | | | 8 |
| AriaCfb128 | 128, 192, 256 | 128 | Aria | Cfb | | | 128 |
| CamelliaCfb8 | 128, 192, 256 | 128 | Camellia | Cfb | | | 8 |
| CamelliaCfb128 | 128, 192, 256 | 128 | Camellia | Cfb | | | 128 |
| SeedCfb8 | 128 | 128 | Seed | Cfb | | | 8 |
| SeedCfb128 | 128 | 128 | Seed | Cfb | | | 128 |
| Sm4Cfb8 | 128 | 128 | SM4 | Cfb | | | 8 |
| Sm4Cfb128 | 128 | 128 | SM4 | Cfb | | | 128 |
| SerpentCfb8 | 128, 192, 256 | 128 | Serpent | Cfb | | | 8 |
| SerpentCfb128 | 128, 192, 256 | 128 | Serpent | Cfb | | | 128 |
| TripleDesCfb8 | 192 | 64 | TripleDes | Cfb | | | 8 |
| TripleDesCfb64 | 192 | 64 | TripleDes | Cfb | | | 64 |
| AesOfb | 128, 192, 256 | 128 | Aes | Ofb | | | |
| AriaOfb | 128, 192, 256 | 128 | Aria | Ofb | | | |
| CamelliaOfb | 128, 192, 256 | 128 | Camellia | Ofb | | | |

## BlockCipher

| primitive | keySize |
| --- | --- |
| Aes | 128, 192, 256 |
| Aria | 128, 192, 256 |
| Camellia | 128, 192, 256 |
| SM4 | 128 |
| Seed | 128 |
| Twofish | 128, 192, 256 |
| Serpent | 128, 192, 256 |
| Kuznyechik | 256 |
| Cast128 | 128 |
| Idea | 128 |
| Des | 64 |
| TripleDes | 192 |
| Threefish512 | 512 |

## EcdsaVerify

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | brainpoolP192r1, brainpoolP224r1, brainpoolP256r1, brainpoolP320r1, brainpoolP384r1, brainpoolP512r1, frp256v1, prime192v2, prime239v1, secp160r1, secp192k1, secp192r1, secp224k1, secp224r1, secp256k1, secp256r1, secp384r1, secp521r1 | KECCAK256, SHA-224, SHA-256, SHA-384, SHA-512, SHA-512/224, SHA-512/256, SHA3-256, SHA3-384, SHA3-512, SHAKE128, SHAKE256 | P1363 | False | Generic |

## KeyWrap

| primitive | keySize |
| --- | --- |
| AesKw | 128, 192, 256 |

## Hash

| primitive | digestSize |
| --- | --- |
| sha-1 | 160 |
| sha-224 | 224 |
| sha-256 | 256 |
| sha-384 | 384 |
| sha-512 | 512 |
| sha-512/256 | 256 |
| sha3-224 | 224 |
| sha3-256 | 256 |
| sha3-384 | 384 |
| sha3-512 | 512 |
| sm3 | 256 |
| ripemd160 | 160 |
| keccak224 | 224 |
| keccak256 | 256 |
| keccak384 | 384 |
| keccak512 | 512 |
| shake128 | 256 |
| shake256 | 512 |
| blake2b | 512 |
| blake2s | 256 |

## Mac

| primitive | keySize | macSize |
| --- | --- | --- |
| AesCmac | 128, 192, 256 | 128 |
| AriaCmac | 128, 192, 256 | 128 |
| CamelliaCmac | 128, 192, 256 | 128 |
| HmacSha1 | | 160 |
| HmacSha224 | | 224 |
| HmacSha256 | | 256 |
| HmacSha384 | | 384 |
| HmacSha512 | | 512 |
| SipHash13 | 128 | 64 |
| SipHash24 | 128 | 64 |
| Kmac128 | 128 | 128, 256 |
| Kmac256 | 256 | 256, 512 |

## RsaPkcs1Verify

| primitive | size | sha | encoding |
| --- | --- | --- | --- |
| RsaSsaPkcs1 | 1024, 1536, 2048, 3072, 4096 | SHA-1, SHA-224, SHA-256, SHA-384, SHA-512, SHA3-256, SHA3-384, SHA3-512 | DER |

## RsaPssVerify

| primitive | size | sha | mgf | mgfSha | saltLen | encoding |
| --- | --- | --- | --- | --- | --- | --- |
| RsaSsaPss | 1024, 1536, 2048, 3072, 4096 | SHA-1, SHA-224, SHA-256, SHA-384, SHA-512 | MGF1 | SHA-1, SHA-224, SHA-256, SHA-384, SHA-512 | 0, 20, 28, 32, 48, 64 | DER |

## RsaEsPkcs1Decrypt

| primitive | size |
| --- | --- |
| RsaEsPkcs1 | 1024, 2048, 3072, 4096 |

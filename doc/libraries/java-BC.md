# BC

**Language:** java\
**Url:** [https://www.bouncycastle.org/](https://www.bouncycastle.org/)

## Performed tests

### Aead

**primitive:** AesCcm, AesEax, AesGcm, AesGcmSiv, AesOcb, AriaCcm, AriaGcm,
CamelliaCcm, CamelliaEax, CamelliaGcm, CamelliaOcb, Chacha20Poly1305, SeedCcm,
SeedGcm, SerpentGcm, SerpentOcb, Sm4Ccm, Sm4Gcm, TwofishEax, TwofishGcm,
TwofishOcb\
**keySize:** 128, 192, 256\
**ivSize:** 64, 88, 96, 104, 120, 128, 256\
**tagSize:** 64, 80, 96, 128

### Xdh

**primitive:** x25519, x448\
**encoding:** DER

### IndCpa

**primitive:** AesCbcCs3, AesCbcPkcs7, AesCfb128, AesCfb128Pkcs7, AesCfb8,
AesOfb, AriaCbcPkcs7, AriaCfb128, AriaCfb8, AriaOfb, CamelliaCbcPkcs7,
CamelliaCfb128, CamelliaCfb8, CamelliaOfb, HC256, Salsa20, SeedCbcPkcs7,
SeedCfb128, SeedCfb8, SeedOfb, SerpentCbcPkcs7, SerpentCfb128, SerpentCfb8,
Sm4CbcCs3, Sm4CbcPkcs7, Sm4Cfb128, Sm4Cfb8, Sm4Ofb, TripleDesCbcPkcs7,
TripleDesCfb64, TripleDesCfb8, TripleDesOfb, TwofishCbcPkcs7, XSalsa20\
**keySize:** 128, 160, 192, 224, 256\
**ivSize:** 64, 128, 192, 256\
**cipher:** Aes, Aria, Camellia, SM4, Seed, Serpent, TripleDes, Twofish\
**mode:** Cbc, Cfb, Cs3, Ofb\
**padding:** Pkcs7\
**paddingSize:** 64, 128\
**feedback:** 8, 64, 128

### BlockCipher

**primitive:** Aes, Aria, Camellia, Cast128, Des, Kuznyechik, Rc5_32_12_16,
Rijndael160, Rijndael192, Rijndael224, Rijndael256, SM4, Seed, Serpent,
Threefish1024, Threefish256, Threefish512, TripleDes, Twofish, Xtea\
**keySize:** 64, 128, 160, 192, 224, 256, 512, 1024\
**tweak:** , 000102030405060708090a0b0c0d0e0f

### DsaVerify

**pLen:** 1024, 2048, 3072\
**qLen:** 160, 224, 256\
**sha:** SHA-1, SHA-224, SHA-256, SHA-512\
**encoding:** DER\
**signatureGeneration:** Generic

### DsaSign

**pLen:** 1024, 2048, 3072\
**qLen:** 160, 224, 256\
**sha:** SHA-1, SHA-224, SHA-256, SHA-512\
**encoding:** DER\
**signatureGeneration:** Rfc6979

### EcdsaVerify

**curve:** brainpoolP192r1, brainpoolP192t1, brainpoolP224r1, brainpoolP224t1,
brainpoolP256r1, brainpoolP256t1, brainpoolP320r1, brainpoolP320t1,
brainpoolP384r1, brainpoolP384t1, brainpoolP512r1, brainpoolP512t1, frp256v1,
prime192v2, prime239v1, secp160r1, secp192k1, secp192r1, secp224k1, secp224r1,
secp256k1, secp256r1, secp384r1, secp521r1, sect233k1, sect233r1, sect283k1\
**sha:** SHA-224, SHA-256, SHA-384, SHA-512, SHA3-256, SHA3-384, SHA3-512,
SHAKE128, SHAKE256\
**encoding:** DER, P1363\
**normalize:** False\
**signatureGeneration:** Generic

### EcdsaSign

**curve:** brainpoolP192r1, brainpoolP192t1, brainpoolP224r1, brainpoolP224t1,
brainpoolP256r1, brainpoolP256t1, brainpoolP320r1, brainpoolP320t1,
brainpoolP384r1, brainpoolP384t1, brainpoolP512r1, brainpoolP512t1, frp256v1,
prime192v2, prime239v1, secp160r1, secp192k1, secp192r1, secp224k1, secp224r1,
secp256k1, secp256r1, secp384r1, secp521r1\
**sha:** SHA-224, SHA-256, SHA-384, SHA-512, SHA3-256, SHA3-384, SHA3-512\
**encoding:** DER\
**normalize:** False\
**signatureGeneration:** Rfc6979

### Ecdh

**primitive:** Ecdh\
**curve:** brainpoolP192r1, brainpoolP192t1, brainpoolP224r1, brainpoolP224t1,
brainpoolP256r1, brainpoolP256t1, brainpoolP320r1, brainpoolP320t1,
brainpoolP384r1, brainpoolP384t1, brainpoolP512r1, brainpoolP512t1, frp256v1,
prime192v2, prime239v1, secp160r1, secp192k1, secp192r1, secp224k1, secp224r1,
secp256k1, secp256r1, secp384r1, secp521r1, sect233k1, sect283k1\
**encoding:** DER

### KeyWrap

**primitive:** AesKw, AesKwp, AriaKw, AriaKwp, CamelliaKw, SeedKw\
**keySize:** 128, 192, 256

### Hash

**primitive:** blake2b, blake2s, md5, sha-1, sha-224, sha-256, sha-384, sha-512,
sha-512/224, sha-512/256, sha3-224, sha3-256, sha3-384, sha3-512, shake128,
shake256, sm3\
**digestSize:** 128, 160, 224, 256, 384, 512

### Mac

**primitive:** AesCmac, HmacSha1, HmacSha224, HmacSha256, HmacSha384,
HmacSha3_224, HmacSha3_256, HmacSha3_384, HmacSha3_512, HmacSha512, Kmac128,
Kmac256, SeedCmac, SipHash128_24, SipHash128_48, SipHash24, SipHash48, Sm4Cmac\
**keySize:** 128, 192, 256\
**macSize:** 64, 128, 160, 224, 256, 384, 512\
**customization:** \`\`

### Pbkdf

**primitive:** Pbkdf\
**sha:** SHA-1, SHA-224, SHA-256, SHA-384, SHA-512, SHA3-224, SHA3-256,
SHA3-384, SHA3-512

### Fpe

**primitive:** AesFf1\
**radix:** 2, 3, 4, 5, 8, 10, 16, 26, 32, 36, 58, 62, 64, 85, 127, 128, 255,
256\
**keySize:** 128, 192, 256

### RsaPkcs1Verify

**primitive:** RsaSsaPkcs1\
**size:** 1024, 1536, 2048, 3072, 4096\
**sha:** SHA-1, SHA-224, SHA-256, SHA-384, SHA-512, SHA3-256, SHA3-384,
SHA3-512\
**encoding:** DER

### RsaPssVerify

**primitive:** RsaSsaPss\
**size:** 1024, 1536, 2048, 3072, 4096\
**sha:** SHA-1, SHA-224, SHA-256, SHA-384, SHA-512, SHAKE128, SHAKE256\
**mgf:** MGF1, SHAKE\
**mgfSha:** SHA-1, SHA-224, SHA-256, SHA-384, SHA-512, SHAKE128, SHAKE256\
**saltLen:** 0, 20, 28, 32, 48, 64\
**encoding:** DER

### RsaEsPkcs1Decrypt

**size:** 1024, 2048, 3072, 4096

### RsaEsOaepDecrypt

**size:** 1024, 2048, 3072, 4096\
**sha:** SHA-1, SHA-224, SHA-256, SHA-384, SHA-512, SHA3-224, SHA3-256,
SHA3-384, SHA3-512\
**mgf:** MGF1\
**mgfSha:** SHA-1, SHA-224, SHA-256, SHA-384, SHA-512, SHA3-224, SHA3-256,
SHA3-384, SHA3-512

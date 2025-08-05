# pycryptodome

**Language:** python\
**Url:**
[https://pypi.org/project/pycryptodome/](https://pypi.org/project/pycryptodome/)

## Security

Some of the primitives do not have constant time implementations.

## Performed tests

### Aead

**primitive:** AeadAesCmacSiv, AesCcm, AesEax, AesGcm, AesOcb\
**keySize:** 128, 192, 256, 384, 512\
**ivSize:** 64, 88, 96, 104, 120, 128, 256\
**tagSize:** 64, 96, 128

### AuthEnc

**primitive:** NaclXSalsa20Poly1305\
**keySize:** 256\
**ivSize:** 192\
**tagSize:** 128

### Xdh

**primitive:** x25519, x448\
**encoding:** RAW

### Daead

**primitive:** DaeadAesCmacSiv\
**keySize:** 256, 384, 512\
**tagSize:** 128

### IndCpa

**primitive:** AesCbcPkcs7, AesCfb128, AesCfb128Pkcs7, AesCfb8, AesOfb, AesXts,
CamelliaCbcPkcs7, CamelliaCfb128, CamelliaOfb, Sm4CbcPkcs7, Sm4Cfb128, Sm4Ofb\
**keySize:** 128, 192, 256, 512\
**ivSize:** 128\
**cipher:** Aes, Camellia, SM4\
**mode:** Cbc, Cfb, Ofb, Xts\
**padding:** Pkcs7\
**paddingSize:** 128\
**feedback:** 8, 128

### BlockCipher

**primitive:** Aes, Cast128, Des, TripleDes\
**keySize:** 64, 128, 192, 256

### DsaVerify

**pLen:** 1024, 2048, 3072\
**qLen:** 160, 224, 256\
**sha:** SHA-1, SHA-224, SHA-256, SHA-512\
**encoding:** P1363\
**signatureGeneration:** Generic

### DsaSign

**pLen:** 1024, 2048, 3072\
**qLen:** 160, 224, 256\
**sha:** SHA-1, SHA-224, SHA-256, SHA-512\
**encoding:** P1363\
**signatureGeneration:** Rfc6979

### EcdsaVerify

**curve:** brainpoolP256r1, brainpoolP384r1, brainpoolP512r1, secp192r1,
secp224r1, secp256k1, secp256r1, secp384r1, secp521r1\
**sha:** SHA-224, SHA-256, SHA-384, SHA-512, SHA3-256, SHA3-384, SHA3-512\
**encoding:** P1363\
**normalize:** False\
**signatureGeneration:** Generic

### EcdsaSign

**curve:** brainpoolP256r1, brainpoolP384r1, brainpoolP512r1, secp192r1,
secp224r1, secp256k1, secp256r1, secp384r1, secp521r1\
**sha:** SHA-224, SHA-256, SHA-384, SHA-512, SHA3-256, SHA3-384, SHA3-512\
**encoding:** P1363\
**normalize:** False\
**signatureGeneration:** Rfc6979

### EddsaVerify

**curve:** edwards25519, edwards448\
**cofactored:** False\
**encoding:** RAW

### EddsaSign

**curve:** edwards25519, edwards448\
**cofactored:** False\
**encoding:** RAW

### Ecdh

**primitive:** Ecdh\
**curve:** secp192r1, secp224r1, secp256r1, secp384r1, secp521r1\
**encoding:** DER, PEM

### KeyWrap

**primitive:** AesKw, AesKwp, AesSivKw\
**keySize:** 128, 192, 256, 384, 512

### Hash

**primitive:** blake2b, blake2s, keccak224, keccak256, keccak384, keccak512,
md5, ripemd160, sha-1, sha-224, sha-256, sha-384, sha-512, sha-512/224,
sha-512/256, sha3-224, sha3-256, sha3-384, sha3-512, shake128, shake256\
**digestSize:** 128, 160, 224, 256, 384, 512

### Mac

**primitive:** AesCmac, HmacSha1, HmacSha224, HmacSha256, HmacSha384,
HmacSha3_224, HmacSha3_256, HmacSha3_384, HmacSha3_512, HmacSha512, Kmac128,
Kmac256\
**keySize:** 128, 192, 256\
**macSize:** 96, 128, 160, 224, 256, 384, 512\
**customization:** \`\`, `4d794170706c69636174696f6e`

### Xof

**primitive:** KangarooTwelve, Shake128, Shake256\
**customization:** \`\`, `4d794170706c69636174696f6e`

### Pbkdf

**primitive:** Pbkdf\
**sha:** SHA-1, SHA-224, SHA-256, SHA-384, SHA-512, SHA3-224, SHA3-256,
SHA3-384, SHA3-512

### Pbes2

**primitive:** Pbes2\
**sha:** SHA-1\
**cipher:** Aes\
**keySize:** 128

### Scrypt

**primitive:** Pbkdf

### Hkdf

**primitive:** HkdfSha1, HkdfSha224, HkdfSha256, HkdfSha384, HkdfSha3_224,
HkdfSha3_256, HkdfSha3_384, HkdfSha3_512, HkdfSha512\
**sha:** SHA-1, SHA-224, SHA-256, SHA-384, SHA-512, SHA3-224, SHA3-256,
SHA3-384, SHA3-512

### Pkcs8Decrypt

**primitive:** Pkcs8, Pkcs8Scrypt\
**sha:** SHA-1, SHA-256, SHA-512, SHA3-256, SHA3-512\
**cipher:** AES-CBC-128, AES-CBC-192, AES-CBC-256, DES-EDE3-CBC

### RsaPkcs1Verify

**primitive:** RsaSsaPkcs1\
**size:** 1024, 1536, 2048, 3072, 4096\
**sha:** SHA-1, SHA-224, SHA-256, SHA-384, SHA-512, SHA3-256, SHA3-384,
SHA3-512\
**encoding:** DER

### RsaPssVerify

**primitive:** RsaSsaPss\
**size:** 1024, 1536, 2048, 3072, 4096\
**sha:** SHA-1, SHA-224, SHA-256, SHA-384, SHA-512\
**mgf:** MGF1\
**mgfSha:** SHA-1, SHA-224, SHA-256, SHA-384, SHA-512\
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

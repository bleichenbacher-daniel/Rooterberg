# crypto-js

**Language:** javascript\
**Url:**
[https://www.npmjs.com/package/crypto-js](https://www.npmjs.com/package/crypto-js)

This library is no longer maintained. It mainly supports symmetric primitives.
Encryption modes do not include authenticated ciphers.

## Performed tests

### IndCpa

**primitive:** AesCbcIso7816, AesCbcPkcs7, AesCfb128, AesCfb128Pkcs7, AesOfb,
Rabbit, TripleDesCbcPkcs7, TripleDesCfb64, TripleDesOfb\
**keySize:** 128, 192, 256\
**ivSize:** 64, 128\
**cipher:** Aes, Rabbit, TripleDes\
**mode:** Cbc, Cfb, Ofb\
**padding:** Iso7816Padding, Pkcs7\
**paddingSize:** 64, 128\
**feedback:** 64, 128\
**byteOrder:** little

### Hash

**primitive:** keccak224, keccak256, keccak384, keccak512, ripemd160, sha-1,
sha-224, sha-256, sha-384, sha-512\
**digestSize:** 160, 224, 256, 384, 512

### Mac

**primitive:** HmacSha1, HmacSha224, HmacSha256, HmacSha384, HmacSha512\
**macSize:** 160, 224, 256, 384, 512

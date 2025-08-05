# aes_gcm

**Language:** rust\
**Url:**
[https://docs.rs/aes_gcm/latest/aes_gcm/](https://docs.rs/aes_gcm/latest/aes_gcm/)

Contrary to the name, this crate contains a generic GCM implementation. It is
possible to use this crate with other 128-bit block ciphers.

## Performed tests

### Aead

**primitive:** AesGcm, AriaGcm, CamelliaGcm, SeedGcm, SerpentGcm, Sm4Gcm,
TwofishGcm\
**keySize:** 128, 192, 256\
**ivSize:** 64, 96, 128, 256\
**tagSize:** 96, 128

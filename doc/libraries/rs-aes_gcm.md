# aes_gcm

**Language:**
rust\
**Url:**
[https://docs.rs/aes_gcm/latest/aes_gcm/](https://docs.rs/aes_gcm/latest/aes_gcm/)

Contrary to the name, this crate contains a generic GCM implementation.
It is possible to use this crate with other 128-bit block ciphers.

## Performed tests

### Aead

| primitive | keySize | ivSize | tagSize |
| --- | --- | --- | --- |
| AesGcm | 128, 192, 256 | 64, 96, 128, 256 | 96, 128 |
| AriaGcm | 128, 256 | 96 | 128 |
| CamelliaGcm | 128, 192, 256 | 96 | 128 |
| SeedGcm | 128 | 96 | 128 |
| Sm4Gcm | 128 | 96 | 128 |
| SerpentGcm | 128 | 96 | 128 |
| TwofishGcm | 256 | 96 | 128 |

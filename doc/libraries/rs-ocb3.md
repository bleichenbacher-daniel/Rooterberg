# ocb3

**Language:**
rust\
**Url:**
[https://docs.rs/ocb3/latest/ocb3/](https://docs.rs/ocb3/latest/ocb3/)

## Performed tests

### Aead

| primitive | keySize | ivSize | tagSize |
| --- | --- | --- | --- |
| AesOcb | 128, 192, 256 | 96 | 64, 96, 128 |
| CamelliaOcb | 128, 192, 256 | 120 | 128 |
| TwofishOcb | 256 | 120 | 128 |
| SerpentOcb | 128 | 120 | 128 |

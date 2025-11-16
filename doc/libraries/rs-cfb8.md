# cfb8

**Language:**
rust\
**Url:**
[https://docs.rs/cfb8/latest/cfb8/](https://docs.rs/cfb8/latest/cfb8/)\
**Tested version:**
0.8.1

## Performed tests

### IndCpa

| primitive | keySize | ivSize | cipher | mode | feedback |
| --- | --- | --- | --- | --- | --- |
| AesCfb8 | 128, 192, 256 | 128 | Aes | Cfb | 8 |
| AriaCfb8 | 128, 192, 256 | 128 | Aria | Cfb | 8 |
| CamelliaCfb8 | 128, 192, 256 | 128 | Camellia | Cfb | 8 |
| SeedCfb8 | 128 | 128 | Seed | Cfb | 8 |
| Sm4Cfb8 | 128 | 128 | SM4 | Cfb | 8 |
| SerpentCfb8 | 128, 160, 192, 224, 256 | 128 | Serpent | Cfb | 8 |

# ccm

**Language:**
rust\
**Url:**
[https://docs.rs/ccm/latest/ccm/](https://docs.rs/ccm/latest/ccm/)\
**Tested version:**
0.5.0

## Performed tests

### Aead

| primitive | keySize | ivSize | tagSize |
| --- | --- | --- | --- |
| AesCcm | 128, 192, 256 | 88, 96, 104 | 64, 96 |
| CamelliaCcm | 128, 192, 256 | 104 | 64, 80 |
| SeedCcm | 128 | 96 | 80, 128 |
| Sm4Ccm | 128 | 96 | 128 |
| AriaCcm | 128, 192, 256 | 96, 104 | 64, 128 |

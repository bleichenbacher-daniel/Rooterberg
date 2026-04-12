# Performed tests for ccm

## Aead

| primitive | keySize | ivSize | tagSize |
| --- | --- | --- | --- |
| AesCcm | 128, 192, 256 | 88, 96, 104 | 64, 96 |
| CamelliaCcm | 128, 192, 256 | 104 | 64, 80 |
| SeedCcm | 128 | 96 | 80, 128 |
| Sm4Ccm | 128 | 96 | 128 |
| AriaCcm | 128, 192, 256 | 96, 104 | 64, 128 |

The library supports all valid IV and tag sizes.
Tests tests that are performed mainly cover common use cases.

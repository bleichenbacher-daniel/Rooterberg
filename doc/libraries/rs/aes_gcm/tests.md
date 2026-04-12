# Performed tests for aes_gcm

## Aead

| primitive | keySize | ivSize | tagSize |
| --- | --- | --- | --- |
| AesGcm | 128, 192, 256 | 64, 96, 128, 256 | 96, 128 |
| AriaGcm | 128, 256 | 96 | 128 |
| CamelliaGcm | 128, 192, 256 | 96 | 128 |
| SeedGcm | 128 | 96 | 128 |
| Sm4Gcm | 128 | 96 | 128 |
| SerpentGcm | 128 | 96 | 128 |
| TwofishGcm | 256 | 96 | 128 |

# Performed tests for ocb3

## Aead

| primitive | keySize | ivSize | tagSize |
| --- | --- | --- | --- |
| AesOcb | 128, 192, 256 | 96 | 64, 96, 128 |
| CamelliaOcb | 128, 192, 256 | 120 | 128 |
| TwofishOcb | 256 | 120 | 128 |
| SerpentOcb | 128 | 120 | 128 |

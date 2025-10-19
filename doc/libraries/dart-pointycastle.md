# pointycastle

**Language:**
dart\
**Url:**
[https://pub.dev/packages/pointycastle](https://pub.dev/packages/pointycastle)

## Performed tests

### Aead

| primitive | keySize | ivSize | tagSize |
| --- | --- | --- | --- |
| AesGcm | 128, 192, 256 | 64, 96, 128, 256 | 128 |
| CamelliaGcm | 128, 192, 256 | 96 | 128 |
| TwofishGcm | 128, 256 | 96 | 128 |
| AesCcm | 128, 192, 256 | 88, 96, 104 | 64, 96, 128 |
| CamelliaCcm | 128, 192, 256 | 104 | 64, 80 |

### Mac

| primitive | keySize | macSize |
| --- | --- | --- |
| AesCmac | 128 | 96, 128 |
| HmacSha1 | | 160 |
| HmacSha224 | | 224 |
| HmacSha256 | | 256 |
| HmacSha384 | | 384 |
| HmacSha512 | | 512 |
| HmacSha3_224 | | 224 |
| HmacSha3_256 | | 256 |
| HmacSha3_384 | | 384 |
| HmacSha3_512 | | 512 |

### Hkdf

| primitive | sha |
| --- | --- |
| HkdfSha1 | SHA-1 |
| HkdfSha224 | SHA-224 |
| HkdfSha256 | SHA-256 |
| HkdfSha384 | SHA-384 |
| HkdfSha512 | SHA-512 |

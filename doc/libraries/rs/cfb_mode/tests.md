# Performed tests for cfb_mode

## IndCpa

| primitive | keySize | ivSize | cipher | mode | feedback | padding | paddingSize |
| --- | --- | --- | --- | --- | --- | --- | --- |
| AesCfb128 | 128, 192, 256 | 128 | Aes | Cfb | 128 | | |
| AesCfb128Pkcs7 | 128 | 128 | Aes | Cfb | 128 | Pkcs7 | 128 |
| AriaCfb128 | 128, 192, 256 | 128 | Aria | Cfb | 128 | | |
| CamelliaCfb128 | 128, 192, 256 | 128 | Camellia | Cfb | 128 | | |
| SeedCfb128 | 128 | 128 | Seed | Cfb | 128 | | |
| Sm4Cfb128 | 128 | 128 | SM4 | Cfb | 128 | | |
| SerpentCfb128 | 128, 160, 192, 224, 256 | 128 | Serpent | Cfb | 128 | | |

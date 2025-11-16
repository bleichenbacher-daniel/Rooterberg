# cbc

**Language:**
rust\
**Url:**
[https://docs.rs/cbc/latest/cbc/](https://docs.rs/cbc/latest/cbc/)\
**Tested version:**
0.1.2

## Performed tests

### IndCpa

| primitive | keySize | ivSize | cipher | mode | padding | paddingSize |
| --- | --- | --- | --- | --- | --- | --- |
| AesCbcPkcs7 | 128, 192, 256 | 128 | Aes | Cbc | Pkcs7 | 128 |
| AesCbcIso7816 | 128, 192, 256 | 128 | Aes | Cbc | Iso7816Padding | 128 |
| AriaCbcPkcs7 | 128, 192, 256 | 128 | Aria | Cbc | Pkcs7 | 128 |
| CamelliaCbcPkcs7 | 128, 192, 256 | 128 | Camellia | Cbc | Pkcs7 | 128 |
| SeedCbcPkcs7 | 128 | 128 | Seed | Cbc | Pkcs7 | 128 |
| Sm4CbcPkcs7 | 128 | 128 | SM4 | Cbc | Pkcs7 | 128 |
| SerpentCbcPkcs7 | 128, 160, 192, 224, 256 | 128 | Serpent | Cbc | Pkcs7 | 128 |
| TwofishCbcPkcs7 | 128, 192, 256 | 128 | Twofish | Cbc | Pkcs7 | 128 |

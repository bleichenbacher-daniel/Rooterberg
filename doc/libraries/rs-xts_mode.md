# xts_mode

**Language:**
rust\
**Url:**
[https://docs.rs/xts-mode/latest/xts_mode/](https://docs.rs/xts-mode/latest/xts_mode/)

## Performed tests

### IndCpa

| primitive | keySize | ivSize | cipher | mode |
| --- | --- | --- | --- | --- |
| AesXts | 256, 384, 512 | 128 | Aes | Xts |
| Sm4Xts | 256 | 128 | SM4 | Xts |
| TwofishXts | 256, 512 | 128 | Twofish | Xts |
| SerpentXts | 256, 512 | 128 | Serpent | Xts |
| CamelliaXts | 256, 512 | 128 | Camellia | Xts |

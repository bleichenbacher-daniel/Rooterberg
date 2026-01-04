# tiny_keccak

**Language:**
rust\
**Url:**
[https://docs.rs/tiny-keccak/latest/tiny_keccak/](https://docs.rs/tiny-keccak/latest/tiny_keccak/)

## Performed tests

### Hash

| primitive | digestSize |
| --- | --- |
| sha3-224 | 224 |
| sha3-256 | 256 |
| sha3-384 | 384 |
| sha3-512 | 512 |
| keccak224 | 224 |
| keccak256 | 256 |
| keccak384 | 384 |
| keccak512 | 512 |

### Mac

| primitive | keySize | macSize |
| --- | --- | --- |
| Kmac128 | 128 | 128, 256 |
| Kmac256 | 256 | 256, 512 |

### Xof

| primitive |
| --- |
| Shake128 |
| Shake256 |
| KangarooTwelve |

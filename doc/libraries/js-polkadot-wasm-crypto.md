# @polkadot/wasm-crypto

**Language:**
javascript\
**Url:**
[https://github.com/polkadot-js/wasm](https://github.com/polkadot-js/wasm)\
**Tested version:**
7.4.1, 7.5.1

## Performed tests

### EcdsaVerify

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | secp256k1 | SHA-256 | BITCOIN | True | Generic |

### EcdsaSign

| primitive | curve | sha | encoding | normalize | signatureGeneration |
| --- | --- | --- | --- | --- | --- |
| Ecdsa | secp256k1 | SHA-256 | P1363 | True | Rfc6979 |

### EddsaVerify

| primitive | curve | cofactored | encoding |
| --- | --- | --- | --- |
| Eddsa | edwards25519 | False | RAW |

### EddsaSign

| primitive | curve | cofactored | encoding |
| --- | --- | --- | --- |
| Eddsa | edwards25519 | False | RAW |

### Hash

| primitive | digestSize |
| --- | --- |
| sha-256 | 256 |
| sha-512 | 512 |
| keccak256 | 256 |
| keccak512 | 512 |

### Mac

| primitive | macSize |
| --- | --- |
| HmacSha256 | 256 |
| HmacSha512 | 512 |

### Pbkdf

| primitive | sha |
| --- | --- |
| Pbkdf | SHA-512 |

### Scrypt

| primitive |
| --- |
| Pbkdf |

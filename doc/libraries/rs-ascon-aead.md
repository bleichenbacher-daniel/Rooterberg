# ascon-aead

**Language:**
rust\
**Url:**
[https://docs.rs/ascon-aead/latest/ascon_aead/](https://docs.rs/ascon-aead/latest/ascon_aead/)\
**Tested version:**
0.5.1

Old versions of the library implement Ascon128, Ascon128a and Ascon80pq.
These algorithms have been deprecated in favor of the NIST version AsconAead128.

## Performed tests

### Aead

| primitive | keySize | ivSize | tagSize |
| --- | --- | --- | --- |
| AsconAead128 | 128 | 128 | 128 |

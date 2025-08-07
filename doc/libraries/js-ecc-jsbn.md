# ecc-jsbn

**Language:**
javascript\
**Url:**
[https://www.npmjs.com/package/ecc-jsbn](https://www.npmjs.com/package/ecc-jsbn)

ecc-jsbn is a Javascript library that implement elliptic curve primites and basic ECDH.

## Security

The ECDH primitve does not check that points are on the curve and hence is susceptible to invalid curve attacks.
Point multiplication is not constant time and in fact has a significant timing side channel.

## Performed tests

### Ecdh

| primitive | curve | encoding |
| --- | --- | --- |
| Ecdh | secp192k1, secp192r1, secp224r1, secp256r1 | UNCOMPRESSED |

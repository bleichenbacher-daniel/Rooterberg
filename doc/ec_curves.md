# Supported curves

This page contains a list of supported elliptic curves as well as the tests that use each curve.
Additional curves and tests will be added depending on use cases and library support.

| name | type | size | oid | testType |
| --- | --- | --- | --- | --- |
| secp128r1 | prime | 128 | 1.3.132.0.28 | |
| secp128r2 | prime | 128 | 1.3.132.0.29 | |
| secp160k1 | prime | 160 | 1.3.132.0.9 | |
| secp160r1 | prime | 160 | 1.3.132.0.8 | Ecdh, EcdsaSign, EcdsaVerify, KeyPair |
| secp160r2 | prime | 160 | 1.3.132.0.30 | |
| secp192k1 | prime | 192 | 1.3.132.0.31 | Ecdh, EcdsaSign, EcdsaVerify |
| secp192r1 | prime | 192 | 1.2.840.10045.3.1.1 | Ecdh, EcdsaSign, EcdsaVerify, KeyPair |
| prime192v2 | prime | 192 | 1.2.840.10045.3.1.2 | Ecdh, EcdsaSign, EcdsaVerify |
| secp224r1 | prime | 224 | 1.3.132.0.33 | Ecdh, EcdsaSign, EcdsaVerify, KeyPair |
| secp224k1 | prime | 224 | 1.3.132.0.32 | Ecdh, EcdsaSign, EcdsaVerify |
| secp256r1 | prime | 256 | 1.2.840.10045.3.1.7 | Ecdh, EcdsaSign, EcdsaVerify, KeyPair |
| secp256k1 | prime | 256 | 1.3.132.0.10 | Ecdh, EcdsaSign, EcdsaVerify, KeyPair, SchnorrSign, SchnorrVerify |
| secp384r1 | prime | 384 | 1.3.132.0.34 | Ecdh, EcdsaSign, EcdsaVerify, KeyPair |
| secp521r1 | prime | 521 | 1.3.132.0.35 | Ecdh, EcdsaSign, EcdsaVerify, KeyPair |
| prime239v1 | prime | 239 | 1.2.840.10045.3.1.4 | Ecdh, EcdsaSign, EcdsaVerify |
| brainpoolP192r1 | prime | 192 | 1.3.36.3.3.2.8.1.1.3 | Ecdh, EcdsaSign, EcdsaVerify |
| brainpoolP192t1 | prime | 192 | 1.3.36.3.3.2.8.1.1.4 | Ecdh, EcdsaSign, EcdsaVerify |
| brainpoolP224r1 | prime | 224 | 1.3.36.3.3.2.8.1.1.5 | Ecdh, EcdsaSign, EcdsaVerify, KeyPair |
| brainpoolP224t1 | prime | 224 | 1.3.36.3.3.2.8.1.1.6 | Ecdh, EcdsaSign, EcdsaVerify |
| brainpoolP256r1 | prime | 256 | 1.3.36.3.3.2.8.1.1.7 | Ecdh, EcdsaSign, EcdsaVerify, KeyPair |
| brainpoolP256t1 | prime | 256 | 1.3.36.3.3.2.8.1.1.8 | Ecdh, EcdsaSign, EcdsaVerify, KeyPair |
| brainpoolP320r1 | prime | 320 | 1.3.36.3.3.2.8.1.1.9 | Ecdh, EcdsaSign, EcdsaVerify |
| brainpoolP320t1 | prime | 320 | 1.3.36.3.3.2.8.1.1.10 | Ecdh, EcdsaSign, EcdsaVerify |
| brainpoolP384r1 | prime | 384 | 1.3.36.3.3.2.8.1.1.11 | Ecdh, EcdsaSign, EcdsaVerify, KeyPair |
| brainpoolP384t1 | prime | 384 | 1.3.36.3.3.2.8.1.1.12 | Ecdh, EcdsaSign, EcdsaVerify, KeyPair |
| brainpoolP512r1 | prime | 512 | 1.3.36.3.3.2.8.1.1.13 | Ecdh, EcdsaSign, EcdsaVerify, KeyPair |
| brainpoolP512t1 | prime | 512 | 1.3.36.3.3.2.8.1.1.14 | Ecdh, EcdsaSign, EcdsaVerify, KeyPair |
| starknet | prime | 252 | | Ecdh, KeyPair |
| frp256v1 | prime | 256 | 1.2.250.1.223.101.256.1 | Ecdh, EcdsaSign, EcdsaVerify |
| sm2 | prime | 256 | 1.2.156.10197.1.301 | Ecdh, KeyPair |
| bls12_377_g1 | prime | 377 | | KeyPair, PointMult |
| bls12_381_g1 | prime | 381 | | KeyPair, PointMult |
| bn254b_g1 | prime | 254 | | KeyPair, PointMult |
| alt_bn128_g1 | prime | 254 | | KeyPair, PointMult |
| bn462_g1 | prime | 462 | | KeyPair, PointMult |
| pallas | prime | 255 | | |
| vesta | prime | 255 | | |
| bandersnatch | prime | 255 | | |
| curve25519 | prime | 255 | | NaclCryptoBox, Xdh |
| curve448 | prime | 448 | | Xdh |
| ecc_frog512ck2 | prime | 512 | | |
| edwards25519 | prime | 255 | | EddsaSign, EddsaVerify |
| edwards448 | prime | 448 | | EddsaSign, EddsaVerify |
| edwardsBls377 | prime | 253 | | |
| JubJub | prime | 255 | | |
| Bandersnatch | prime | 255 | | |
| sect233r1 | binary | 233 | 1.3.132.0.27 | EcdsaVerify |
| sect233k1 | binary | 233 | 1.3.132.0.26 | Ecdh, EcdsaVerify |
| sect283k1 | binary | 283 | 1.3.132.0.16 | Ecdh, EcdsaVerify |
| sect409k1 | binary | 409 | 1.3.132.0.36 | Ecdh |
| sect571k1 | binary | 571 | 1.3.132.0.38 | Ecdh |

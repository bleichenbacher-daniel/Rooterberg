# Tested libraries

This page lists the libraries that are currently tested.
The main focus at this point is determining compatibility with standards.
Frequently, libraries do not specify all the algorithm parameters that are being used.
At this point no test results are being included.

## C\#

| Name | Url | Tests |
| --- | --- | --- |
| [.NET](libraries/cs-dotnet.md) | [https://learn.microsoft.com/en-us/dotnet/standard/security/cryptography-model](https://learn.microsoft.com/en-us/dotnet/standard/security/cryptography-model) | 113 |
| [BC_CSHARP](libraries/cs-bc_csharp.md) | [https://github.com/bcgit/bc-csharp](https://github.com/bcgit/bc-csharp) | 658 |

## Java

| Name | Url | Tests |
| --- | --- | --- |
| [BC](libraries/java-bc.md) | [https://www.bouncycastle.org/](https://www.bouncycastle.org/) | 623 |
| [Conscrypt](libraries/java-conscrypt.md) | [https://github.com/google/conscrypt](https://github.com/google/conscrypt) | 104 |
| [SUN](libraries/java-sun.md) | [https://docs.oracle.com/en/java/javase/24/security/oracle-providers.html](https://docs.oracle.com/en/java/javase/24/security/oracle-providers.html) | 30 |
| [SunEC](libraries/java-sunec.md) | [https://docs.oracle.com/en/java/javase/24/security/oracle-providers.html](https://docs.oracle.com/en/java/javase/24/security/oracle-providers.html) | 31 |
| [SunJCE](libraries/java-sunjce.md) | [https://docs.oracle.com/en/java/javase/24/security/oracle-providers.html](https://docs.oracle.com/en/java/javase/24/security/oracle-providers.html) | 109 |
| [SunRsaSign](libraries/java-sunrsasign.md) | [https://docs.oracle.com/en/java/javase/24/security/oracle-providers.html](https://docs.oracle.com/en/java/javase/24/security/oracle-providers.html) | 67 |

## Javascript

| Name | Url | Tests |
| --- | --- | --- |
| [@noble/ciphers](libraries/js-noble-ciphers.md) | [https://github.com/paulmillr/noble-ciphers](https://github.com/paulmillr/noble-ciphers) | 70 |
| [@noble/curves](libraries/js-noble-curves.md) | [https://github.com/paulmillr/noble-curves](https://github.com/paulmillr/noble-curves) | 44 |
| [@polkadot/wasm-crypto](libraries/js-polkadot-wasm-crypto.md) | [https://github.com/polkadot-js/wasm](https://github.com/polkadot-js/wasm) | 12 |
| blakejs | [https://www.npmjs.com/package/blakejs](https://www.npmjs.com/package/blakejs) | 2 |
| [crypto-browserify](libraries/js-crypto-browserify.md) | [https://www.npmjs.com/package/crypto-browserify](https://www.npmjs.com/package/crypto-browserify) | 141 |
| [crypto-js](libraries/js-crypto-js.md) | [https://www.npmjs.com/package/crypto-js](https://www.npmjs.com/package/crypto-js) | 35 |
| [crypto.subtle](libraries/js-crypto.subtle.md) | [https://www.w3.org/TR/2017/REC-WebCryptoAPI-20170126/](https://www.w3.org/TR/2017/REC-WebCryptoAPI-20170126/) | 76 |
| [ecc-jsbn](libraries/js-ecc-jsbn.md) | [https://www.npmjs.com/package/ecc-jsbn](https://www.npmjs.com/package/ecc-jsbn) | 4 |
| [elliptic](libraries/js-elliptic.md) | [https://www.npmjs.com/package/elliptic](https://www.npmjs.com/package/elliptic) | 32 |
| [js-ascon](libraries/js-ascon.md) | [https://github.com/brainfoolong/js-ascon](https://github.com/brainfoolong/js-ascon) | 2 |
| keccak | [https://www.npmjs.com/package/keccak](https://www.npmjs.com/package/keccak) | 8 |
| [miscreant](libraries/js-miscreant.md) | [https://www.npmjs.com/package/miscreant](https://www.npmjs.com/package/miscreant) | 12 |
| [node-forge](libraries/js-node-forge.md) | [https://www.npmjs.com/package/node-forge](https://www.npmjs.com/package/node-forge) | 83 |
| [node.js](libraries/js-node.js.md) | [https://nodejs.org/api/crypto.html](https://nodejs.org/api/crypto.html) | 278 |
| [secp256k1](libraries/js-secp256k1.md) | [https://www.npmjs.com/package/secp256k1](https://www.npmjs.com/package/secp256k1) | 2 |
| [sjcl](libraries/js-sjcl.md) | [https://github.com/bitwiseshiftleft/sjcl](https://github.com/bitwiseshiftleft/sjcl) | 13 |
| sshpk | [https://www.npmjs.com/package/sshpk](https://www.npmjs.com/package/sshpk) | 12 |
| [tweetnacl](libraries/js-tweetnacl.md) | [https://github.com/dchest/tweetnacl-js](https://github.com/dchest/tweetnacl-js) | 4 |

## Python

| Name | Url | Tests |
| --- | --- | --- |
| [pyca](libraries/py-pyca.md) | [https://cryptography.io/en/latest/](https://cryptography.io/en/latest/) | 327 |
| [pycryptodome](libraries/py-pycryptodome.md) | [https://pypi.org/project/pycryptodome/](https://pypi.org/project/pycryptodome/) | 353 |
| [pyjwt](libraries/py-pyjwt.md) | [https://pyjwt.readthedocs.io/](https://pyjwt.readthedocs.io/) | 15 |
| [pynacl](libraries/py-pynacl.md) | [https://pynacl.readthedocs.io/en/latest/](https://pynacl.readthedocs.io/en/latest/) | 3 |

## Rust

| Name | Url | Tests |
| --- | --- | --- |
| [aegis](libraries/rs-aegis.md) | [https://docs.rs/aegis/latest/aegis/](https://docs.rs/aegis/latest/aegis/) | 4 |
| [aes](libraries/rs-aes.md) | [https://docs.rs/aes/latest/aes/](https://docs.rs/aes/latest/aes/) | 3 |
| [aes_gcm](libraries/rs-aes_gcm.md) | [https://docs.rs/aes_gcm/latest/aes_gcm/](https://docs.rs/aes_gcm/latest/aes_gcm/) | 24 |
| aes_gcm_siv | [https://docs.rs/aes_gcm_siv/latest/aes_gcm_siv/](https://docs.rs/aes_gcm_siv/latest/aes_gcm_siv/) | 2 |
| [aes_kw](libraries/rs-aes_kw.md) | [https://docs.rs/aes_kw/latest/aes_kw/](https://docs.rs/aes_kw/latest/aes_kw/) | 16 |
| aes_siv | [https://docs.rs/aes_siv/latest/aes_siv/](https://docs.rs/aes_siv/latest/aes_siv/) | 4 |
| aria | [https://docs.rs/aria/latest/aria/](https://docs.rs/aria/latest/aria/) | 3 |
| [ascon-aead](libraries/rs-ascon-aead.md) | [https://docs.rs/ascon-aead/latest/ascon_aead/](https://docs.rs/ascon-aead/latest/ascon_aead/) | 1 |
| [ascon-hash](libraries/rs-ascon-hash.md) | [https://docs.rs/ascon-hash/latest/ascon_hash/](https://docs.rs/ascon-hash/latest/ascon_hash/) | 1 |
| blake2 | [https://docs.rs/blake2/latest/blake2/](https://docs.rs/blake2/latest/blake2/) | 2 |
| bls12_381 | [https://docs.rs/bls12_381/latest/bls12_381/](https://docs.rs/bls12_381/latest/bls12_381/) | 2 |
| bn254 | [https://docs.rs/bn254/latest/bn254/](https://docs.rs/bn254/latest/bn254/) | 1 |
| camellia | [https://docs.rs/camellia/latest/camellia/](https://docs.rs/camellia/latest/camellia/) | 3 |
| cast5 | [https://docs.rs/cast5/latest/cast5/](https://docs.rs/cast5/latest/cast5/) | 1 |
| cbc | [https://docs.rs/cbc/latest/cbc/](https://docs.rs/cbc/latest/cbc/) | 22 |
| [ccm](libraries/rs-ccm.md) | [https://docs.rs/ccm/latest/ccm/](https://docs.rs/ccm/latest/ccm/) | 27 |
| cfb8 | [https://docs.rs/cfb8/latest/cfb8/](https://docs.rs/cfb8/latest/cfb8/) | 16 |
| cfb_mode | [https://docs.rs/cfb_mode/latest/cfb_mode/](https://docs.rs/cfb_mode/latest/cfb_mode/) | 17 |
| chacha20poly1305 | [https://docs.rs/chacha20poly1305/latest/chacha20poly1305/](https://docs.rs/chacha20poly1305/latest/chacha20poly1305/) | 2 |
| cmac | [https://docs.rs/cmac/latest/cmac/](https://docs.rs/cmac/latest/cmac/) | 9 |
| crypto_box | [https://docs.rs/crypto_box/latest/crypto_box/](https://docs.rs/crypto_box/latest/crypto_box/) | 2 |
| [crypto_secretbox](libraries/rs-crypto_secretbox.md) | [https://docs.rs/crypto_secretbox/latest/crypto_secretbox/](https://docs.rs/crypto_secretbox/latest/crypto_secretbox/) | 1 |
| [cts](libraries/rs-cts.md) | [https://docs.rs/cts/latest/cts/](https://docs.rs/cts/latest/cts/) | 9 |
| des | [https://docs.rs/des/latest/des/](https://docs.rs/des/latest/des/) | 5 |
| dsa | [https://docs.rs/dsa/latest/dsa/](https://docs.rs/dsa/latest/dsa/) | 9 |
| [eax](libraries/rs-eax.md) | [https://docs.rs/eax/latest/eax/](https://docs.rs/eax/latest/eax/) | 9 |
| [fpe](libraries/rs-fpe.md) | [https://docs.rs/fpe/latest/fpe/](https://docs.rs/fpe/latest/fpe/) | 108 |
| hc_256 | [https://docs.rs/hc_256/latest/hc_256/](https://docs.rs/hc_256/latest/hc_256/) | 1 |
| hkdf | [https://docs.rs/hkdf/latest/hkdf/](https://docs.rs/hkdf/latest/hkdf/) | 11 |
| [hmac](libraries/rs-hmac.md) | [https://docs.rs/hmac/latest/hmac/](https://docs.rs/hmac/latest/hmac/) | 11 |
| idea | [https://docs.rs/idea/latest/idea](https://docs.rs/idea/latest/idea) | 1 |
| [k256](libraries/rs-k256.md) | [https://docs.rs/k256/latest/k256/](https://docs.rs/k256/latest/k256/) | 6 |
| kangarootwelve | [https://docs.rs/kangarootwelve/latest/kangarootwelve/](https://docs.rs/kangarootwelve/latest/kangarootwelve/) | 1 |
| kisaseed | [https://docs.rs/kisaseed/latest/kisaseed/](https://docs.rs/kisaseed/latest/kisaseed/) | 1 |
| [ocb3](libraries/rs-ocb3.md) | [https://docs.rs/ocb3/latest/ocb3/](https://docs.rs/ocb3/latest/ocb3/) | 14 |
| ofb | [https://docs.rs/ofb/latest/ofb/](https://docs.rs/ofb/latest/ofb/) | 9 |
| p192 | [https://docs.rs/p192/latest/p192/](https://docs.rs/p192/latest/p192/) | 1 |
| [p224](libraries/rs-p224.md) | [https://docs.rs/p224/latest/p224/](https://docs.rs/p224/latest/p224/) | 4 |
| [p256](libraries/rs-p256.md) | [https://docs.rs/p256/latest/p256/](https://docs.rs/p256/latest/p256/) | 4 |
| [p384](libraries/rs-p384.md) | [https://docs.rs/p384/latest/p384/](https://docs.rs/p384/latest/p384/) | 4 |
| [p521](libraries/rs-p521.md) | [https://docs.rs/p521/latest/p521/](https://docs.rs/p521/latest/p521/) | 4 |
| pbkdf2 | [https://docs.rs/pbkdf2/latest/pbkdf2/](https://docs.rs/pbkdf2/latest/pbkdf2/) | 11 |
| pcbc | [https://docs.rs/pcbc/latest/pcbc/](https://docs.rs/pcbc/latest/pcbc/) | 3 |
| pkcs8 | [https://docs.rs/pkcs8/latest/pkcs8/](https://docs.rs/pkcs8/latest/pkcs8/) | 11 |
| pmac | [https://docs.rs/pmac/latest/pmac/](https://docs.rs/pmac/latest/pmac/) | 3 |
| poly1305 | [https://docs.rs/poly1305/latest/poly1305/](https://docs.rs/poly1305/latest/poly1305/) | 1 |
| [rabbit](libraries/rs-rabbit.md) | [https://docs.rs/rabbit/latest/rabbit/](https://docs.rs/rabbit/latest/rabbit/) | 1 |
| rc5 | [https://docs.rs/rc5/latest/rc5/](https://docs.rs/rc5/latest/rc5/) | 3 |
| [ring_compat](libraries/rs-ring_compat.md) | [https://docs.rs/ring-compat/latest/ring_compat/](https://docs.rs/ring-compat/latest/ring_compat/) | 2 |
| ripemd | [https://docs.rs/ripemd/latest/ripemd/](https://docs.rs/ripemd/latest/ripemd/) | 1 |
| [rsa](libraries/rs-rsa.md) | [https://docs.rs/rsa/latest/rsa/](https://docs.rs/rsa/latest/rsa/) | 35 |
| salsa20 | [https://docs.rs/salsa20/latest/salsa20/](https://docs.rs/salsa20/latest/salsa20/) | 2 |
| [serpent](libraries/rs-serpent.md) | [https://docs.rs/serpent/latest/serpent/](https://docs.rs/serpent/latest/serpent/) | 5 |
| sha1 | [https://docs.rs/sha1/latest/sha1/](https://docs.rs/sha1/latest/sha1/) | 1 |
| sha2 | [https://docs.rs/sha2/latest/sha2/](https://docs.rs/sha2/latest/sha2/) | 6 |
| sha3 | [https://docs.rs/sha3/latest/sha3/](https://docs.rs/sha3/latest/sha3/) | 8 |
| [siphasher](libraries/rs-siphasher.md) | [https://docs.rs/siphasher/latest/siphasher/](https://docs.rs/siphasher/latest/siphasher/) | 4 |
| sm2 | [https://docs.rs/sm2/latest/sm2/](https://docs.rs/sm2/latest/sm2/) | 2 |
| sm3 | [https://docs.rs/sm3/latest/sm3/](https://docs.rs/sm3/latest/sm3/) | 1 |
| sm4 | [https://docs.rs/sm4/latest/sm4/](https://docs.rs/sm4/latest/sm4/) | 1 |
| [speck_cipher](libraries/rs-speck_cipher.md) | [https://docs.rs/speck_cipher/latest/speck_cipher/](https://docs.rs/speck_cipher/latest/speck_cipher/) | 7 |
| threefish | [https://docs.rs/threefish/latest/threefish/](https://docs.rs/threefish/latest/threefish/) | 3 |
| [twofish](libraries/rs-twofish.md) | [https://docs.rs/twofish/latest/twofish/](https://docs.rs/twofish/latest/twofish/) | 3 |
| [x25519_dalek](libraries/rs-x25519_dalek.md) | [https://docs.rs/x25519_dalek/latest/x25519_dalek/](https://docs.rs/x25519_dalek/latest/x25519_dalek/) | 1 |
| [x448](libraries/rs-x448.md) | [https://docs.rs/x448/latest/x448/](https://docs.rs/x448/latest/x448/) | 1 |
| [xts_mode](libraries/rs-xts_mode.md) | [https://docs.rs/xts-mode/latest/xts_mode/](https://docs.rs/xts-mode/latest/xts_mode/) | 10 |

## Swift

| Name | Url | Tests |
| --- | --- | --- |
| [CryptoSwift](libraries/swift-cryptoswift.md) | [https://github.com/krzyzanowskim/CryptoSwift](https://github.com/krzyzanowskim/CryptoSwift) | 78 |
| [swift-crypto](libraries/swift-crypto.md) | [https://github.com/apple/swift-crypto](https://github.com/apple/swift-crypto) | 29 |

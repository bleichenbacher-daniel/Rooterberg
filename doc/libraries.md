# Tested libraries
## Javascript
[@noble/ciphers](https://github.com/paulmillr/noble-ciphers)  
[@noble/curves](https://github.com/paulmillr/noble-curves)  
[@polkadot/wasm-crypto](https://github.com/polkadot-js/wasm)  
[blakejs](https://www.npmjs.com/package/blakejs)  
[crypto-browserify](https://www.npmjs.com/package/crypto-browserify)
Uses the same interface as node.js  
[crypto-js](https://www.npmjs.com/package/crypto-js)
This library is no longer maintained.
It mainly supports symmetric primitives.
Encryption modes do not include authenticated ciphers.  
[crypto.subtle](https://www.w3.org/TR/2017/REC-WebCryptoAPI-20170126/)
crypto.subtle is an interface and has many independent implementations.
Currently, all tests run against the version built into node.  
[ecc-jsbn](https://www.npmjs.com/package/ecc-jsbn)  
[elliptic](https://www.npmjs.com/package/elliptic)
This library fixes vulnerabilities very slowly.
An example is CVE-2024-48948, which is an issue found in July, 2024.
The issue was later found to be critical, as it leaks private key in some cases.
Version 6.6.1, is still suceptible to the vulnerability.
Currently (July, 2025) no fixed version is available.
Ecdh, ECDSA and EdDSA are not constant time.  
[keccak](https://www.npmjs.com/package/keccak)  
[miscreant](https://www.npmjs.com/package/miscreant)  
[node-forge](https://www.npmjs.com/package/node-forge)
This library has a high number of vulnerabilities.
Interfaces are not very intuitive.
Type string is often used to represent byte arrays.  
[node.js](https://nodejs.org/api/crypto.html)  
[secp256k1](https://www.npmjs.com/package/secp256k1)  
[sshpk](https://www.npmjs.com/package/sshpk)  
[tweetnacl](https://github.com/dchest/tweetnacl-js)  
## Python
[pyca](https://cryptography.io/en/latest/)
The library can be built against different underlying libraries.
The tests are based on the version using 'pip install cryptography'.  
[pycryptodome](https://pypi.org/project/pycryptodome/)
Some of the primitives do not have constant time implementations.  
[pyjwt](https://pyjwt.readthedocs.io/)  
[pynacl](https://pynacl.readthedocs.io/en/latest/)  
starkbank  
[starkbank-ecdsa](https://pypi.org/project/starkbank-ecdsa/)
The library implements ECDSA over secp256r1 and secp256k1 using SHA-256.
Other curves and other hash functions could in principle be used.
However, this needs to be done carefully, since for example hash truncation is not supported.  
## Rust
[aegis](https://docs.rs/aegis/latest/aegis/)  
[aes](https://docs.rs/aes/latest/aes/)  
[aes_gcm](https://docs.rs/aes_gcm/latest/aes_gcm/)
Contrary to the name, this crate contains a generic GCM implementation.
It is possible to use this crate with other 128-bit block ciphers.  
[aes_gcm_siv](https://docs.rs/aes_gcm_siv/latest/aes_gcm_siv/)  
[aes_kw](https://docs.rs/aes_kw/latest/aes_kw/)  
[aes_siv](https://docs.rs/aes_siv/latest/aes_siv/)  
[aria](https://docs.rs/aria/latest/aria/)  
[blake2](https://docs.rs/blake2/latest/blake2/)  
[bls12_381](https://docs.rs/bls12_381/latest/bls12_381/)  
[bn254](https://docs.rs/bn254/latest/bn254/)  
[camellia](https://docs.rs/camellia/latest/camellia/)  
[cast5](https://docs.rs/cast5/latest/cast5/)  
[cbc](https://docs.rs/cbc/latest/cbc/)  
[ccm](https://docs.rs/ccm/latest/ccm/)  
[cfb8](https://docs.rs/cfb8/latest/cfb8/)  
[cfb_mode](https://docs.rs/cfb_mode/latest/cfb_mode/)  
[chacha20poly1305](https://docs.rs/chacha20poly1305/latest/chacha20poly1305/)  
[cmac](https://docs.rs/cmac/latest/cmac/)  
[crypto_box](https://docs.rs/crypto_box/latest/crypto_box/)  
[crypto_secretbox](https://docs.rs/crypto_secretbox/latest/crypto_secretbox/)  
[cts](https://docs.rs/cts/latest/cts/)  
[des](https://docs.rs/des/latest/des/)  
[dsa](https://docs.rs/dsa/latest/dsa/)  
[eax](https://docs.rs/eax/latest/eax/)  
[ed25519_dalek](https://docs.rs/ed25519_dalek/latest/ed25519_dalek/)  
[fpe](https://docs.rs/fpe/latest/fpe/)  
[hc_256](https://docs.rs/hc_256/latest/hc_256/)  
[hkdf](https://docs.rs/hkdf/latest/hkdf/)  
[hmac](https://docs.rs/hmac/latest/hmac/)  
[k256](https://docs.rs/k256/latest/k256/)
k256::ecdsa implements and requires normalized signatures.
This is contrary to other crates, which generate and accept signatures where 0 < s < n.  
[kisaseed](https://docs.rs/kisaseed/latest/kisaseed/)  
[ocb3](https://docs.rs/ocb3/latest/ocb3/)  
[ofb](https://docs.rs/ofb/latest/ofb/)  
[p192](https://docs.rs/p192/latest/p192/)  
[p224](https://docs.rs/p224/latest/p224/)  
[p256](https://docs.rs/p256/latest/p256/)  
[p384](https://docs.rs/p384/latest/p384/)  
[p521](https://docs.rs/p521/latest/p521/)  
[pbkdf2](https://docs.rs/pbkdf2/latest/pbkdf2/)  
[pcbc](https://docs.rs/pcbc/latest/pcbc/)  
[pkcs8](https://docs.rs/pkcs8/latest/pkcs8/)  
[pmac](https://docs.rs/pmac/latest/pmac/)  
[poly1305](https://docs.rs/poly1305/latest/poly1305/)  
[rabbit](https://docs.rs/rabbit/latest/rabbit/)
This implementation uses little endian byte order.  
[rc5](https://docs.rs/rc5/latest/rc5/)  
[ring_compat](https://docs.rs/ring-compat/latest/ring_compat/)
This library is essentially a wrapper around some rust crypto primitives.  
[ripemd](https://docs.rs/ripemd/latest/ripemd/)  
[rsa](https://docs.rs/rsa/latest/rsa/)  
[salsa20](https://docs.rs/salsa20/latest/salsa20/)  
[serpent](https://docs.rs/serpent/latest/serpent/)
Serpent is only tested with 128-bit keys using most encryption modes CBC, CFB, ...
There is unfortunately no documentation explaining, how to use other key sizes.  
[sha1](https://docs.rs/sha1/latest/sha1/)  
[sha2](https://docs.rs/sha2/latest/sha2/)  
[sha3](https://docs.rs/sha3/latest/sha3/)  
[siphasher](https://docs.rs/siphasher/latest/siphasher/)  
[sm2](https://docs.rs/sm2/latest/sm2/)  
[sm3](https://docs.rs/sm3/latest/sm3/)  
[sm4](https://docs.rs/sm4/latest/sm4/)  
[speck_cipher](https://docs.rs/speck_cipher/latest/speck_cipher/)  
[twofish](https://docs.rs/twofish/latest/twofish/)
Twofish is only tested with 256-bit keys using most encryption modes CBC, CFB, ...
There is no documentation for specifying alternative key sizes with these modes.  
[x25519_dalek](https://docs.rs/x25519_dalek/latest/x25519_dalek/)  
[x448](https://docs.rs/x448/latest/x448/)  
[xts_mode](https://docs.rs/xts-mode/latest/xts_mode/)  
## Java
[BC](https://www.bouncycastle.org/)  
[Conscrypt](https://github.com/google/conscrypt)  
[SUN](https://docs.oracle.com/en/java/javase/24/security/oracle-providers.html)  
[SunEC](https://docs.oracle.com/en/java/javase/24/security/oracle-providers.html)  
[SunJCE](https://docs.oracle.com/en/java/javase/24/security/oracle-providers.html)  
[SunRsaSign](https://docs.oracle.com/en/java/javase/24/security/oracle-providers.html)  
## C#
[.NET](https://learn.microsoft.com/en-us/dotnet/standard/security/cryptography-model)  
[BC_CSHARP](https://github.com/bcgit/bc-csharp)  
## Swift
[CryptoSwift](https://github.com/krzyzanowskim/CryptoSwift)  
[swift-crypto](https://github.com/apple/swift-crypto)
This is a reimplementation of Apple's CryptoKit.
Uses BoringSSL as underlying crypto library.  

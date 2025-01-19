# Rooterberg

This project contains test vectors, similar to Project Wycheproof. The test vectors here are experimental.
Their format may change. Often the test vectors are not well tested. Likely, I will add these test vectors to
Project Wycheproof, once this project is in a more stable state.

The goal is to receive early feedback on the test vectors, determine if the format is useful, find algorithms and
algorithm parameters that should be covered.

## Recent changes
2024/4/5: Added two files with raw ECDSA signatures. The signatures in these files are triples (r, s, id), where
r,s are the two scalars of the ECDSA signature and id is the recovery_id that can be used to recover the public key. 

2024/9/14, v. 0.48:
* Added preliminary files with test vectors. 
* About 66% of the files have been tested against independent libraries.
* tables/all_tests.json is a file that contains the current status.

2024/9/22, v. 0.49: 
* Changed the directory structure. 
* Updated the test vectors.
* Adding a small number of tests for RSA-OAEP.

2024/9/29, v. 0.50: 
* Renamed field *publicKeyPkcs8* to *publicKeySpki* to reflect that the field contains a DER encoding of a *SubjectPublicKeyInfo* structure. 
* Minor updates of some test vector files.

2024/10/11, v. 0.51 
* Added more tests for ECDSA.

2024/10/26, v. 0.52 
* Added support for more EC curves.
* Added test vectors for ECDH with JWK keys.
* Added test vectors edge cases during CRT computation of RSA-OAEP.
* Added test vectors for SPECK.

2024/11/10, v. 0.53
* Added more test vectors for RFC 6979 based signatures.

2024/11/24 v. 0.54
* Updated the test setup.
* Added more pseudorandom test vectors (npm elliptic previously failed only one test vector even
  though 1 out of every 256 signatures was incorrect).

2024/12/8 v. 0.55
* Added test vectors for the Rabbit stream cipher (RFC 4503).
  One open question is the endianness of key, iv and data.
  While RFC 4503 uses big endian encoding, all implementations I've tested use little endian encoding.
  Hence the test vectors use little endian encoding too.
* Added test vectors for GCM-SST (draft-mattsson-cfrg-aes-gcm-sst-07)

2024/12/22 v. 0.56
* Added invalid test cases to IND-CPA ciphers with padding.
* Changed test vector format for IND-CPA ciphers. They now include a boolean field "valid".
* Added test vectors for DSA verification
* Added test vectors for HC-256
* Improved comments of RSA-PKCS #1 test vectors.
* Added tests against pycryptodome. 

2025/1/5 v. 0.57
* Simplified and unified test vectors for public key crypto primitives. Tests that do not target
  the encoding of the keys can contain the keys in multiple formats. Public keys typically use
  the encodings "PublicKeySpki": the DER-encoding of the SubjectPublicKeyInfo (in hexadecimal),
  and "PublicKeyPem": the PEM-encoding of the public key. Private keys are typically encoded
  as "PrivateKeyPkcs8": the DER-encoding of the private key and "PrivateKeyPem". In some files
  this information is still missing. They will be added when needed (i.e. when there are tests
  that can verify the correctness of the encoding.)
* Added test cases for PKCS #8 decryption. The format for the test vectors will very likely
  change, since there are a number of open questions. For example, the field "key_type" was added
  because some libraries require the knowledge of the key type of the encrypted key before parsing.
  It is also unclear to what degree a test can expect a key validation of the decrypted key.
  Stricter tests could be addded if a full key validation could be assumed. The test vector are
  are sorted by the symmetric algorithm. This should allow adding additional symmetric encryption
  schemes without affecting existing tests. 
* Added edge cases for RSA PKCS #1 decryption. Most of the new test vectors test edge cases that
  occur when the decryption uses CRT.
* Added test vectors for XSalsa20-Poly1305. Only authenticated encryption with no AAD is supported.
* Added flags to test vectors with weak DES keys. Some libraries reject such test vectors.
  All test vectors have been changed so that the key bytes have odd parity.
* Rewrote the ASN.1 module. Hopefully this did not change the test vectors.
* Added more fuzzing for ASN.1 encoding. 

2025/1/19 v. 0.58
* Added test vectors for NaCl specific algorithms
* Added two Aegis variants
* Added more flags for EdDSA public keys.
* Added more flags to Xdh keys.
# Change log

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
  Stricter tests could be added if a full key validation could be assumed. The test vector are
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

2025/2/2 v. 0.59
* Added more Ecdsa tests.
* Added more tests for Schnorr signatures.
* Added more tests for Nacl specific algorithms.
* Changed the format for testing decryption of PKCS8 ciphertexts.
  The test vectors now contain two results: *privateKeyInfo* contains the full PKCS8 encoding of
  the encrypted private key. *privateKey* contains only the wrapped private key. This addition has
  been done for convenience, since some implementations already parse the wrapped key.

2025/3/16 v. 0.60
* Added some test vectors for JWT signatures.
* Replaced some ECDSA signatures that didn't test the intended edge case.
* Added more ECDSA signatures for arithmetic errors.
* Added ECDH test vector using PKCS8/SPKI format for keys. So far all the keys use DER encoding.
  Keys with BER encoding will be added in a later version, as it is unclear if such tests should be 
  put into separate files.
* Added a file with test results, sorted by library.
* Cleanup of EC keys in JWT format.
  EC key in JWT format can now have either a "use" field or a "key_ops" field.

2025/4 v. 0.61
* Adding ECDH test vectors for more curves.
* Adding DSA signatures using RFC 6979.
* Adding test vectors for CMAC with alternative block ciphers.
* Adding PBKDF test vectors using different character sets. Implementations of PBKDF
  frequently have the property that the inputs are restricted to byte arrays that
  represent UTF-8 encoded strings or ASCII-encoded string, etc. To simplify testing
  such implementations, test vectors have been added that use restricted character sets.
  Flags have been added to describe the type of the inputs.
* Adding test vectors for RC5/64/12 with 128 bit keys.
* Adding more test vectors for RSA-PKCS 1.5 signatures. 
* added more fuzzing to OID encodings.
* improved flags for RSA-ES-OAEP and  RSA-ES-PKCS1 to distinguish padding modifications from other invalid ciphertexts.
* added test results against some Java providers.

Format changes:
* changed the fields mgf_sha to mgfSha, salt_len to saltLen  in the algorithm description of RSA-PSS and RSA-OAEP.
* changed the fields iter_count to iterCount and dk_len to dkLen for PBKDF.

2025/5 v. 0.62
* Adding test vectors for XDH with ASN.1 and PEM encoded keys.
* Adding PEM encoded keys as an alternative. Some Javascript libraries have incomplete documentation,
  and it is frequently difficult to determine acceptable key formats are. 
  Generally, when key validation is not part of the test (e.g. signature validation) then
  a test vector file can contain multiple key formats for convenience. If key validation
  is part of the test (e.g. ECDH, XDH) then multiple files are generated for multiple formats.
* Adding test vectors with special case private keys to ECDSA tests.
* Adding test vectors for secp256k1 with normalized signatures.
* Adding more tests against Javascript libraries.

2025/7 v. 0.63
* Changing tag sizes for AES-GCM-SST to match draft-mattsson-cfrg-aes-gcm-sst-15.
* Adding more flags to test vectors for PKCS #8. This is done to make a better selection
  depending on the implementation. 
* Test results now contain a list of flags, which describe the tests vectors that were
  skipped in the test. The main purpose of these flags is to describe restrictions of the
  implementation. (A typical example is the limitation of some libraries to passwords that
  are valid UTF-8 strings.)
* Additional languages: Testing is now done also against libraries in C# and Swift
* Additional curves: There a more test vectors for legacy curves using less then 256-bits.
  While these curves are hopefully no longer in wide use, they sometimes have unusual
  properties and hence have bugs that are not present in other curves.
* Additional test vector for BER/DER encoding based on old CVEs.
* Added tests against Javascript, Swift and C# libraries.
# Rooterberg

This project contains test vectors, similar to Project Wycheproof. The test vectors here are experimental.
Their format may change. Often the test vectors are not well tested. Likely, I will add these test vectors to
Project Wycheproof, once this project is in a more stable state.

The goal is to receive early feedback on the test vectors, determine if the format is useful, find algorithms and
algorithm parameters that should be covered.

## Recent changes
2024/4/5: Added two files with raw ECDSA signatures. The signatures in these files are triples (r, s, id), where
r,s are the two scalars of the ECDSA signature and id is the recovery_id that can be used to recover the public key. 

2024/9/14, v. 0.48; Added preliminary files with test vectors. About 66% of the files have been tested against independent libraries.
tables/all_tests.json is a file that contains the current status.

2024/9/22, v. 0.49: Changed the directory structure. Updated the test vectors. Adding a small number of tests for RSA-OAEP.

2024/9/29, v. 0.50: Renamed field *publicKeyPkcs8* to *publicKeySpki* to reflect that the field contains a DER encoding of a
*SubjectPublicKeyInfo*.
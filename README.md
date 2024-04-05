# Rooterberg

This project contains test vectors, similar to Project Wycheproof. The test vectors here are experimental.
Their format may change. Often the test vectors are not well tested. Likely, I will add these test vectors to
Project Wycheproof, once this project is in a more stable state.

The goal is to receive early feedback on the test vectors, determine if the format is useful, find algorithms and
algorithm parameters that should be covered.

## Recent changes
2024/4/5: Added two files with raw ECDSA signatures. The signatures in these files are triples (r, s, id), where
r,s are the two scalars of the ECDSA signature and id is the recovery_id that can be used to recover the public key. 
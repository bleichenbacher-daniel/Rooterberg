# Format of the test vectors

Rooterberg is an experimental repo that contains new versions of test vectors for project
Wycheproof. The format for the new test vectors is still work in progress and may change 
in the future. A number of changes are made to simplify testing. The main changes are:
 
* The *TestGroup* has been removed. Previously all the test vectors had a hierarchical structure,
  where test vectors were colleced into groups with similar parameters. This structure tended
  to complicate testing and has therefore been removed.
* The test vectors are now split by algorithms. Previously, test vector files contained
  test vectors for multiple sets of algorithm parameters. For example, files with test vectors
  for symmetric primitives contained vectors for all possible key sizes (typically, 128-bit, 192-bit
  and 256-bit). If a crypto library only supports 128-bit and 256-bit keys then the tester has
  to filter out unwanted test vectors.
  The new version of the test vectors use seperate files for test vectors with distinct algorithm
  parameters. This simplifies testing, especially for libraries that require compile time constants
  for algorithm parameters. A large number of Rust crates have this behaviour.
* The test vectors now use more descriptive field names for values that have multiple different
  formats. Especially, public keys and private keys are represented in many different ways: PEM, ASN,
  JWK, raw bytes, etc.


  
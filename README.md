# Rooterberg

This project contains test vectors, that are an extension of the test vectors from project Wycheproof.
The new format should eventually replace the old format from Wycheproof.
Rooterberg is at this point work in progress. The test vectors here are experimental and their format may change.
A main focus is on simplifying the test vector format to allow simpler testing. A secondary focus is
to obtain insight in to what algorithms are supported be different libraries. All too often libraries
do not clearly state the range of algorithm parameters that are supported. Hence an implementer may
run into incompatibility problems, because libraries may have undocumented differences.

The goal is to receive early feedback on the test vectors, determine if the format is useful, find algorithms and
algorithm parameters that should be covered.

[Recent changes](doc/changes.md):
New test vectors are released about once per months. However, there is no fixed schedule.

[Test vector format](doc/test_vector_format.md):
The format for the test vectors has been slightly changed from Wychproof to simplify testing. The current format is still
work in progress and may change.

[Libraries](doc/libraries.md): The test vectors are tested against a number of libraries. The document contains a list
of these libraries.

[Tables](tables/README.md):  Test results are given here. The main intent behind the tests is to check
formats. Frequently, libraries do not specify all the algorithm parameters of their primitives.
No failing tests are included in these lists.


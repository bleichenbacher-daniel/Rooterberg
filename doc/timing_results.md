# Results from the timing tests

Below are some results from running the tests against a number of libraries.
Some of the tests depend on additional libraries. In particular, tests 
against JavaScript implementations often depend on whether they run in
a browser or using node.js, since often different implementations of the
cryptographic primitives are being used. At the moment I don't have
a setup that allows to run the tests on multiple platforms. All JavaScript
tests were done under node.js.

## Test failures

The list below includes libraries and primitives, where testing
observed a significant correlation between timing and secrets.
The tests look for information leakage. They do not determine
if the leakage is exploitable.

All the tests take as input a list of timings, select a fraction
of these timings with the fastest times. If the implementation has
no timing side channel then the selection should be random.
However, when the implementation has a timing side channel then
selecting the signatures with the fastest timing can lead to a
set of signatures with biased $k$ and hence leak information.
There are a number of tests checking for such a bias in the most
significant bits, the least significant bits and the bit length of the
values $k$. Test failures have a p-value $< 10^{-9}$. If a test fails
with a larger p-value then the test is typically repeated with larger sample.
This removes the risk of false positives.

The timing difference is a rough approximation of the difference between
different types of signatures on a 3Ghz CPU (e.g. signatures where k has 6 leading zero
bits and random signatures).

| Language  | Library      | Primitive       | Failing tests        | Timing difference |
| -------   | ------------ | --------------- | -------------------- |-------------------|
| Javascript| bip-schnorr  | Schnorr         | msb, lsb, bit_length | 200 $\mu s$       |
|           | browserify-sign | Dsa 2048/256 | msb, lsb, bit_length | 700 $\mu s$       |
|           | ecc-jsbn     | Ecdh secp224r1  | msb, lsb, bit_length | 250 $\mu s$       |
|           | ecc-jsbn     | Ecdh secp256r1  | msb, lsb, bit_length | 400 $\mu s$       |
|           | ecurve       | Ecdh secp256k1  | msb, lsb, bit_length | 300 $\mu s$       |
|           | ecurve       | Ecdh secp256r1  | msb, lsb, bit_length | 300 $\mu s$       |
|           | elliptic     | Ecdh secp256r1  | msb, lsb, bit_length |  80 $\mu s$       |
|           | elliptic     | Ecdsa secp192r1 | msb, lsb, bit_length |  20 $\mu s$       |
|           | elliptic     | Ecdsa secp256k1 | msb, lsb, bit_length |  10 $\mu s$       |
|           | elliptic     | Ecdsa secp256r1 | msb, lsb, bit_length |  20 $\mu s$       |
|           | elliptic     | Ecdsa secp384r1 | msb, lsb, bit_length |  90 $\mu s$       |
|           | elliptic     | Ed25519         | msb, lsb             |  10 $\mu s$       |
|           | noble        | Ecdsa secp256k1 | msb, bit_length      |  <2 $\mu s$       |
|           | noble        | Ecdsa secp256r1 | msb, bit_length      |  <2 $\mu s$       |
|           | noble        | Ecdsa secp384r1 | msb, bit_length      |  <2 $\mu s$       |
|           | noble        | Ed25519         | lsb                  |  <2 $\mu s$       |
|           | sjcl         | Ecdsa secp256r1 | msb, lsb, bit_length | 150 $\mu s$       |
|           | sjcl         | Ecdsa secp256k1 | msb, lsb, bit_length | 150 $\mu s$       |
| Java      | spongycastle | Ecdsa secp256k1 | msg, lsb, bit_length |  <2 $\mu s$       |
| Python    | pycryptodome | Ecdsa secp256r1 | msb, lsb, bit_length |   3 $\mu s$       |
|           | pycryptodome | Ed25519         | msb, lsb, bit_length |   4 $\mu s$       |
|           | pycryptodome | Dsa (2048 bit)  | msb, bit_length      |  20 $\mu s$       |
|           | starkbank    | Ecdsa secp256k1 | msb, lsb, bit_length | 150 $\mu s$       |
| Dart      | cryptography_plus | Ed25519    | msb, lsb, bit_count  |  20 $\mu s$       |

## Bias

In those cases where the timing correlates with the most significant bits it is
possible to estimate the seriousness of the timing leak. This is done by selecting
a subset of the fastest measurements and computing the bias of the samples
selected that way. This bias can be used a 
[metric to assess its severity](timing.md#vulnerability-assessment).


| Language  | Library      | Primitive         | Samples           | Bias | Status              |
| --------- | ------------ | ---------------   | ----------------  | ---- |---------------------|
| Javascript| bip-schnorr  | Schnorr secp256k1 | 3'907 / 500'000   | 0.32 | (underlying lib)    |
|           | browserify-sign | Dsa            | 1'000 / 200'000   | 0.86 | reported (Dec 2025) |
|           | ecc-jsbn     | Ecdh secp224r1    | 3'125 /  50'000   | 0.33 | reported (Aug 2025) |
|           | ecc-jsbn     | Ecdh secp256r1    | 3'125 /  50'000   | 0.32 | reported (Aug 2025) |
|           | ecurve       | Ecdh secp256k1    | 3'125 / 200'000   | 0.38 | reported (Aug 2025) |
|           | ecurve       | Ecdh secp256r1    | 3'125 / 200'000   | 0.41 | reported (Aug 2025) |
|           | elliptic     | Ecdh secp256r1    | 3'913 / 500'000   | 0.40 | reported (Aug 2025) |
|           | elliptic     | Ecdsa secp192r1   | 7'835 / 500'000   | 0.19 | "                   |
|           | elliptic     | Ecdsa secp224r1   | 7'812 / 500'000   | 0.19 | "                   |
|           | elliptic     | Ecdsa secp256k1   | 3'958 / 500'000   | 0.22 | "                   |
|           | elliptic     | Ecdsa secp256k1   | 3'933 / 500'000   | 0.19 | "                   |
|           | elliptic     | Ecdsa secp384r1   | 3'908 / 500'000   | 0.16 | "                   |
|           | elliptic     | Ed25519           | 3'922 / 500'000   | 0.18 | "                   |
|           | sjcl         | Ecdsa secp256r1   |                   | 0.99 | [known since 2023](https://github.com/bitwiseshiftleft/sjcl/issues/438) |
|           | sjcl         | Ecdsa secp256k1   |                   | 0.99 | "                   |
| Java      | bouncycastle | Ecdh brainpool256r1 | 1'567 / 200'000 | 0.50 |                     |
| Python    | pycryptodome | Ed25519           | 2'533 / 5'000'000 | 0.99 | reported (June 2025) |
|           | pycryptodome | Ed448             |                   | 0.99 | "                   |
|           | pycryptodome | Ecdsa secp256r1   | 2'619 / 5'000'000 | 0.28 | "                   |
|           | starkbank    | Ecdsa secp256k1   | 3'907 / 500'000   | 0.29 | reported (Aug 2025) |
| Dart      | cryptography_plus | Ed25519      | 1'101 / 1'000'000 | 0.12 |                     |

Interestingly, the python library *ecdsa* generates signatures, where the timing leaks
information with a bias of about 0.17 using the same methodology as the measurements above.
This library was not written for production use and does not include any countermeasures against
timing attacks. Many of the libraries tested above have a bias that is much larger than the 
unprotected implementation. The reason appears to be that incomplete countermeasures often
leak just one type of information (e.g. the bit-length of *k*) and that as a result this
type of information is easier to determine.



<!--
noble/curves contains a timing channel, that can be reliably detected (i.e. p-value < 1e-9).
However, the timing difference is rather small, which makes it difficult to determine
the bias that this side channel generates.
| noble        | Ecdsa secp256k1   | 3'973 / 500'000   | 0.10 | v. 1.3.x        |
| noble        | Ecdsa secp256r1   | 7'815 / 500'000   | 0.07 | v. 1.3.x        |
| noble        | Ecdsa secp384r1   | 15'642 / 500'000  | 0.05 | v. 1.3.x        |

| noble        | Ecdsa secp256k1   | 15'779 / 1'000'000 | 0.04 | v. 2.0.1       |
| noble        | Ecdsa secp256r1   | 15'683 / 1'000'000 | 0.03 | v. 2.0.1       |
| noble        | Ecdsa secp384r1   | 15'778 / 1'000'000 | 0.04 | v. 2.0.1       |

| pycryptodome | Dsa 2048/256 | 64 / 2'000'000 | 0.99 | reported (Jan 2026) |

No longer relevant:
Java needs more testing. Tests against SpongyCastle only show a small bias, but the library
is so old that I'd expect a bigger bias.

| spongycastle | Ecdsa secp256r1   | 36'654 / 500'000  | 0.03 | known flaw          |

--> 

## Libraries where no timing side channels were detected

Below is a list of libraries where no timing side channels were detected.
Similarly to the results above, these results were obtained by actually measuring
the underlying primitives. The tests don't catch differences smaller than 1 $\mu s$.
Code reviews or static code analysis are much better suited for such issues.
Hence, an absence of a result does not imply an absence of a side channel.

| language     | Library       | Primitive  | Parameters     | Samples |
| ------------ | ------------- | -----------| -------------- | ------- |
| Javascript   | elliptic      | Ecdh       | secp256k1      | 500'000 |
|              | node.js       | Ecdsa      | secp256r1      | 200'000 |
|              | secp256k1     | Ecdsa      | secp256k1      | 200'000 |
|              | subtle_crypto | Ecdsa      | secp256r1, secp384r1, secp521r1  | 500'000 |
|              | tweetnacl     | Ed25519    |                | 500'000 |
|              | wasm-crypto   | Ecdsa      | secp256k1      | 500'000 |
|              | sshpk         | Ecdsa      | secp256k1, secp384k1 | 200'000 |
|              | bitcoinjs-lib-v5 | Ecdsa   | secp256k1      | 500'000 |
| Java         | BouncyCastle  | Ecdsa      | secp256r1      | 500'000 |
|              | SunEC         | Ecdsa      | secp256r1      | 500'000 |
| Python       | PyCa          | Ecdsa      | secp256r1, Ed25519   | 200'000 |
| Swift        | swift-crypto  | Ecdsa      | secp256r1      | 200'000 |
| Rust         | p224          | Ecdsa      | secp224r1      | 200'000 |
|              | p256          | Ecdsa      | secp256r1      | 200'000 |
|              | p384          | Ecdsa      | secp384r1      | 200'000 |
|              | p521          | Ecdsa      | secp521r1      | 200'000 |
|              | ed25519_dalek | Ed25519    |                | 200'000 |
|              | botan         | Ecdsa      |                | 500'000 |


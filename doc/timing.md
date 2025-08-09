# Timing attacks against cryptographic primitives

<-! Intro ->
One set of tests check for side-channels in implementations of cryptographic primitives.
The primary side-channels analyzed here are timing differences that allow to gain information
about secret data used in the computation of the primitive. The primary focus at this
point is to develop simple tests that allow to evaluate a large number of libraries efficiently.

## Tested primitives

Currently the project focuses on elliptic curve primitives: ECDSA, ECDH and EdDSA.
For ECDSA and EdDSA the main concern is that the side-channels allows to gain information
about the secret blinding factor *k*. A side-channel can leak for example the bit-length of
*k*, its Hamming weight, the length of an addition chain or information about the 
least or most significant bits of *k*. Collecting such information may be used to determine
the private keys used by the primitive. Typically, for attacks against ECDSA and EdDSA the
attacker simply observes the time it takes to generate a signature. When the primitive
is deterministic then chosen message attacks could be useful to repeat the generation of
a signature with the same input in order to increase the precision of the measurement.

## Description of the tests

The tests are performed by running implementations of cryptographic libraries on different
platforms. This typically means that the results are somewhat noisy and that small
timing differences (i.e. smaller than a microsecond) are difficult or impossible to
observe. The current setup typically allows to detect implementations with a non-constant
number of arithmetic operations and implementations that use a non-constant time
biginteger library.

<-! Setup ->
The general setup of the tests allows to perform the measurement and the respective
analysis of the result on separate platforms. The timing measurements are written
to a JSON file, which is being analyzed later.

<-! general strategy ->
The general strategy behind the analysis of the test results is to minimize the
number of false positives. The reason for such a strategy is that it allows the
tests to be run as part of a continuous test.

An important observation here is that it is quite easy to collect millions of 
measurements. When the sample size is large enough then the statistical tests
detecting an information leakage through a side-channel typically fail with
very small p-values.

Statistical tests are selected so that abnormal timing data does not lead to
a false positive. One strategy that easily allows to avoid false positives is
to select subsets of the measurements (e.g. the fastest n% of the timings),
and then to check if the corresponding secret values have distinguishable
characteristics than the original values. 


## Test failure

A test failure is a measurement that exposes information about secret values
and leads to at least a theoretical attack with complexity smaller than the
security strength of the primitive.

For ECDSA any measurable correlation between the timing (or other side channels)
and the value *k* used to generate the signature leads to a theoretical attack.
The amount of information leaked determines the severity of the issue and is 
discussed below.

For ECDH leaking information about the bit-length or the most significant bits
of the private key is not an exploitable vulnerability (assuming only a few
bits are leaked.). However, the underlying scalar multiplication is often
used by third parties to implement other primitives such as ECDSA. For that
reason we determine the severity of a side channel in the same way as for
ECDH as for ECDSA.

It is also important to note that measurements depend heavily on the environment
under which the tests are performed. Small noise reductions and more precise
timings can have a large impact on the exploitability of information leakage.


## Bias
One of the main statistic is the computation of the bias of a sample of values.
Especially for DSA or Schnorr-type signatures determining the bias of the
secret values *k*, allows to estimate the seriousness of a side-channel leak.

<-! Maybe \mbox needs to be written as \text ->
The bias of a random variable $X$ over $Z/(nZ)$ is defined as
$$\mbox{bias}_n(X)=e^{2\pi i X/n}.$$
Thus the bias of a sample $S = [s_1, ..., s_m]$ over $Z/(nZ)$ is computed as
$$\mbox{bias}_n(S)=\sum_{i=1}^m e^{2\pi i s_i / n} / m.$$
Hence the bias is a complex value with norm <= 1. A uniformly distributed sample has
a bias of 0.

## Hidden number problem
A hidden number problem for a secret value *x* is a list of tuples (a_i, b_i)
such that the values $a_i x + b_i \mod n$ are biased. A main question is wether
the secret value *x* can be recovered from the tuples (a_i, b_i).

More concretely we define a  hidden number problem with parameters (N, b, C)
to be a list of N tuples $(a_i, b_i)$ with the property that $a_i \in [0, C)$
and the distribution of $a_i x + b_i \mod n$ has a bias *b*.

If the value *C* is small enough then it is possible to find the most significant
bits of *x* by using an FFT. In particular, a (N, b, C) hidden number problem
can be solved via FFT in time $O(C \log(N))$ and space $O(N)$ if 
$N = \Omega(b^{-2})$. 

In order to derive a hidden number problem with small *C* from a hidden number
problem with large *C* we may use the conversions described below. Generally
the discussion below assume that the values in the hidden number problem are
close to uniformly distributed. Such distributions are generally obtained when
analyzing primitives such as ECDSA. 

**Selection:**
A (N, b, C) hidden number problem can be converted into a (N/m, b, C/m) hidden
number problem. Heuristically one can simply select the tuples with $0 < a_i < C/m$.

**Collision search:**
A (N, b, C) hidden number problem can be converted into a (N^2/m, b^2, C/m) hidden
number problem. 

**Shamir-Schroeppel:**
A (N, b, C) hidden number problem can be converted into a (N, b^4, C/(TN)) hidden
number problem in time $O(T)$ and space $O(N)$.

**Substitution:**
A (N, b, c) hidden number problem for a secret value *x* can be 
transformed into a (N, b, c) hidden number problem for *kx*.
I.e., if a list of N tuples $(a_i, b_i)$ defines a (N, b, c) hidden number problem
then $(a_i k^{-1}, b_i)$ is a  (N, b, c) hidden number problem for *kx*.


## Vulnerability assessment

Estimating the severity of a bias caused by a side-channel is difficult.
The precision of the measurements have a large influence on the bias.
Additionally, relatively small changes in the bias can greatly affect
the exploitability of the side-channel. At this point we use the following
rule of thump:

| abs(bias)   | severity |
| ----------  | -------- |
| < 0.2       | low      |
| 0.2 .. 0.45 | medium   |
| > 0.45      | high     |

A bias of $b > 0.45$ was chosen as limit here, since it allows to apply the
Shamir-Schroeppel transformation twice. The resulting hidden number problem
has a bias of $b^{16} > 2^{-18.5}$, which means that the FFT step can be performed
with $2^{40}$ or less samples.

A bias of 0.2 or larger is likely exploitable with 160-bit curves.
Exploiting a timing channel for larger curves likely requires a bias of 0.45 or
larger.

The severity of a vulnerability generally tries to answer two distinct questions:
* How exploitable is the issue?
* How important is it to fix the issue?
The two questions are not always in sync. In the case of side channel leakage there
is a large amount of uncertainty. Changing the environment in which the code is
executed can have a significant impact. Hence, we strongly recommend to address
even small side channel leakages.

## Testing for uniformity

Additional tests against the uniformity of the secret values are performed in
our tests. The process is the same as above: given a set S of measurements the
analysis selects a fraction of those measurements with the fastest timings.
The expectation is that this selection has the same distribution of secret
values as a correctly implemented primitive. 

Currently the following statistics are tested:
* The distribution of the most significant bits. E.g., for ECDSA over a curve
  with an order close to a power of 2, the test expects that the most significant
  bits of the values *k* are uniformly distributed.
* The distribution of the least significant bits of secret values.
* The bit-length of the secret values. E.g., the number of point additions
  in careless implementations of a point multiplication sometimes depends
  on the bit-length of the scalar.


<-! Key recovery attacks ->
## LLL based attacks 
LLL-based key recovery attacks require the knowledge of about 3 most significant
bits. This corresponds to a bias with norm of about 0.97 or more. A one-bit leakage
corresponds to a bias with norm of 0.64. Such a bias should be relatively easy to exploit
on a single work station. 

## FFT based attacks
My analysis of the DSA algorithm in an old version of the DSS used the observation that the 
proposed signature generation had a bias with norm of about 0.2. This result was obtained for
a 160-bit range for *k*'s used in DSA.
Exploiting a similar bias for 256-bit ranges is more complex. We use a heuristic assumption
that at least two rounds of Shamir-Shroeppel are necessary. This assumption is the basis for
the threshold of 0.45 for the bias. 


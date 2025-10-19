# Motivation and goals of the project

## Motivation
* Vulnerabilities in cryptographic libraries often repeat.
* Research papers often do not reach the right audience.
* CVEs often contain not enough information to understand the 
  underlying issues. Frequently it is necessary to track
  causes and effects of past vulnerabilities by analyzing
  source code changes. In some cases there may not even be enough
  information available to reproduce a vulnerability.
* A large number of bugs in cryptographic applications stem from
  unclear specifications. Often it is unclear what types of
  modifications the receiver side should accept. Cryptographic
  libraries frequently do not specify all the algorithm parameters.

## Goals
The project has a number of goals:

* **Organizing knowledge about vulnerabilities:**
  A big issue with known vulnerabilities is that the are often described
  in research papers that are difficult to find. Developers of cryptographic
  libraries may not have enough time to read and understand such papers, and
  may not be in a situation to determine which papers are relevant.

* **Developing tests for known vulnerabilities:**
  An important goal is to generalize known vulnerabilites and develop
  tests that catch these issues in a wide range of situations.

* **Generating test vectors**
  Whenever possible we try to convert tests for vulnerabilites into sets
  of test vectors. Test vectors have a big advantage in that they are
  easy to deploy against a large variaty of libraries.

* **Running tests against common libraries**
  Having a larger number of tests that run against a number of common
  cryptographic libraries allows to get some feedback about the usefullness
  and correctness of the tests and test vectors.
  Implementations sometimes slightly deviate from standards and standards
  themselves frequently contain ambiguous or undefined behavior. Running
  tests help a lot to identify such cases.

  By comparing libraries it is also possible to document tests and test vectors,
  so that the cause of a test failure can be identified more easily.

* **Analyzing test results**
  One of the goals of the project is to be able to give some feedback
  on the severity of test failures.

* **Distribution of test results**
  A major issue with security issues is that it is often difficult to
  get a good overview over the quality of a library. The reason is that
  often vulnerabilites are not fixed in a timely manner and issues are
  ignored for a long period of time.

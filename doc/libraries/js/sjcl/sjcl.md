# sjcl

**Language:** javascript\
**Url:**
[https://github.com/bitwiseshiftleft/sjcl](https://github.com/bitwiseshiftleft/sjcl)

The library mainly looks like a research project. I.e., the code has been
written to focus on some specific aspects (such as optimizing AES). The library
is still being used in a number of project, even though it has been deprecated.

## Security

The library is vulnerable to timing attacks. The function ecdhJavaEc does not
validate inputs and hence is susceptible to invalid curve attacks.

## Tables

[Performed tests](tests.md)\
[Test results](results.json)

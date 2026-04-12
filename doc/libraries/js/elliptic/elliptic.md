# elliptic

**Language:** javascript\
**Url:**
[https://www.npmjs.com/package/elliptic](https://www.npmjs.com/package/elliptic)\
**Tested version:** 6.6.1

## Security

This library fixes vulnerabilities very slowly. An example is CVE-2025-14505,
which was reported in 2024. The issue is severe as it leaks private keys in some
cases. Version 6.6.1, is still suceptible to the vulnerability. Currently
(March, 2026) no fixed version is available. The library is susceptible to
timing attacks. In particular neither Ecdh, ECDSA nor EdDSA have constant time
implementations.

## Tables

[Performed tests](tests.md)\
[Test results](results.json)

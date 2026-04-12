# browserify-sign

**Language:** javascript\
**Url:**
[https://www.npmjs.com/package/browserify-sign](https://www.npmjs.com/package/browserify-sign)

browserify-sign is a reimplementation of some of the primitives from node.js.

## Security

The library depends on elliptic and bn.js. As a result it suffers from some
unpatched vulnerabilities and has a large potential for timing attacks. It has
been verified experimentally, that DSA private keys can be recovered from timing
information.

## Tables

[Performed tests](tests.md)\
[Test results](results.json)

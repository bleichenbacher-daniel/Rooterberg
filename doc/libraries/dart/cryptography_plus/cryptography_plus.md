# cryptography_plus

**Language:** dart\
**Url:**
[https://pub.dev/packages/cryptography_plus](https://pub.dev/packages/cryptography_plus)

This library is a replacement for the dart cryptography package.

## Security

The library implements insecure primitives. An example are AES-CTR and AES-CBC
with an HMAC. The HMAC does not include the IV. As a result, an authentication
bypass is possible by simply changing the IV.

## Tables

[Performed tests](tests.md)\
[Test results](results.json)

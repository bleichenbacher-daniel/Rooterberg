# BC

**Language:** java\
**Url:** [https://www.bouncycastle.org/](https://www.bouncycastle.org/)\
**Tested version:** 1.81

BouncyCastle can either be used through the JCA interface or by calling the
underlying BouncyCastle classes directly. Our tests use the JCA interface
whenever possible. This results in provider independent test code. However, in a
number of cases there is no JCA interface available and tests specifically
written for BouncyCastle is being used.

## Tables

[Performed tests](tests.md)\
[Test results](results.json)

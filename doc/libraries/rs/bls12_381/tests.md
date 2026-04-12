# Performed tests for bls12_381

## PointMult

| primitive | curve | encoding |
| --- | --- | --- |
| PointMult | bls12_381_g1, bls12_381_g2 | PFC_COMPRESSED |

BLS12-381 has a large cofactor.
Because of this cofactor many of the edge cases for the field arithmetic use points that are on the curve, but not in the subgroup.
To perform these tests the function from_bytes_unchecked is being used.

# Performed tests for miscreant

## Aead

| primitive | keySize | ivSize | tagSize |
| --- | --- | --- | --- |
| AeadAesCmacSiv | 256, 512 | 96, 128 | 128 |
| AeadAesPmacSiv | 256, 512 | 96, 128 | 128 |

## Daead

| primitive | keySize | tagSize |
| --- | --- | --- |
| DaeadAesCmacSiv | 256, 512 | 128 |
| DaeadAesPmacSiv | 256, 512 | 128 |

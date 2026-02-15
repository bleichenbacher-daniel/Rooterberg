# PKCS8

<!- ->

Encryption using PKCS #8 is defined in RFC 5208.
The main goal of the test vectors is to test the decryption of PKCS #8 encrypted ciphertexts.

The test vectors have the following format:
* The encrypted plaintext is a valid ASN encoded private key.

The test result make the following assumptions:
* The test assumes that resulting key is parsed and that invalid formats are recognized
* The ASN encoding of the HMAC algorithm contains a NULL parameter. The flag *MissingNull*
  marks such test cases.
* DER encoded as well as BER encoded ciphertexts are valid. The flag *BerEncoding* marks test
  cases that are valid BER encoding, but not valid DER encoding.
* It is assumed that decryption has an upper limit on the iteration count to prevent
  DOS attacks. 

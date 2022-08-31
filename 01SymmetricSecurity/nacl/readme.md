## NaCl

[NaCl](https://nacl.cr.yp.to) is the Networking and Cryptography library that has a symmetric library (secretbox) and an asymmetric library (box), and was designed by Daniel J. Bernstein. The additional Go cryptography packages contain an implementation of NaCl. It uses a 32-byte key and 24-byte nonces. A nonce is a number used once: a nonce should never be reused in a set of messages encrypted with the same key, or else a compromise may occur. In some cases, a randomly generated nonce is suitable. In other cases, it will be part of a stateful system; perhaps it is a message counter or sequence number.

The secretbox system uses a stream cipher called “XSalsa20” to provide confidentiality, and a MAC called “Poly1305”. The package uses the data types *[32]byte for the key and *[24]byte for the nonce. Working with these data types may be a bit unfamiliar; the code below demonstrates generating a random key and a random nonce and how to interoperate with functions that expect a []byte.




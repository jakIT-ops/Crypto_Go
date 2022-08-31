Symmetric cryptography is the simplest form of cryptography: all parties share the same key. It also tends to be the fastest type of cryptography. Fundamentally, the key used by a symmetric algorithm is a sequence of bytes that are used as the input to a transformation algorithm that operates on bits. Key distribution with symmetric cryptography is more difficult than with asymmetric cryptography as the transmission of sensitive key material requires a secure channel. In the next chapter, we’ll look at means of exchanging keys.

There are two components to symmetric encryption: the algorithm that provides confidentiality (which is a block or stream cipher), and the component that provides integrity and authenticity (the MAC algorithm). Most ciphers do not provide both in the same algorithm, but those that do are called Authenticated Encryption (AE), or Authenticated Encryption with Additional Data (AEAD), ciphers. In this chapter, we’ll consider four `ciphersuites`: NaCl, AES-GCM, AES-CTR with an HMAC, and AES-CBC with an HMAC; a ciphersuite is a selection of algorithms that we’ll use to provide security. The code from this chapter can be found in the chapter3 package in the example code.

The packages here:

nacl: XSalsa20 / Poly1305
aesgcm: AES-256-GCM
aesctr: AES-256-CTR with HMAC-SHA-384
aescbc: AES-256-CBC with HMAC-SHA-384 and PKCS #7 padding

This also includes an example of using additional data with an AEAD in the `aesgcmad` package.


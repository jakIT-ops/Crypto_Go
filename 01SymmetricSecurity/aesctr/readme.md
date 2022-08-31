### AES-CTR with HMAC

The last options you should consider, if you have a choice, are AES-CTR and AES-CBC with an HMAC. In these ciphersuites, data is first encrypted with AES in the appropriate mode, then an HMAC is appended. In this book, we assume the use of these ciphersuites only when required as part of a specification or for compatibility.

CTR also uses a nonce; again, the nonce must be only ever used once with the same key. Reusing a nonce can be catastrophic, and will leak information about the message; the system will now fail the indistinguishability requirements and therefore becomes insecure. If there is any question as to whether a nonce is unique, a random nonce should be generated. If this is being used for compatibility with an existing system, you’ll need to consider how that system handles nonces.

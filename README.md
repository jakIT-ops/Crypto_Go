# Practical Cryptography With Go

## Introduction

The foundation of cryptographic security are the three goals of `confidentiality`, `integrity`, and authenticity.

Confidentiality is the requirement that only the intended party can read a given message; `integrity` is the requirement that a message’s contents cannot be tampered with; and `authenticity` is the requirement that the provenance (or origin) of a message can be trusted.

In order to discuss cryptography, a baseline vocabulary is needed. The following terms have specific meanings:

* The `plaintext` is the original message.

* The `ciphertext` is traditionally a message that has been transformed to provide confidentiality.

* A `cipher` is a cryptographic transformation that is used to encrypt or decrypt a message.

* A `message authentication code` (or `MAC`) is a piece of data that provides authenticity and integrity. A MAC algorithm is used both to generate and validate this code.

* To `encrypt` a message is to apply a confidentiality transformation, but is often used to describe a transformation that satisfies all three goals. 

* To `decrypt` a message to reverse the confidentiality transformation, and often indicates that the other two properties have been verified.

* A `hash` or `digest algorithm` transforms some arbitrary message into a fixed-size output, also called a digest or hash. A cryptographic hash is such an algorithm that satisfies some specific security goals.

* A `peer` or `party` describes an entity involved in the communication process. It might be a person or another machine.

## Engineering concerns and platform security

### Basic security

Security should provide `authentication`, `authorisation`, and `auditing`. Authentication means that the system verifies the identity of parties interacting with the system; authorisation verifies that they should be allowed to carry out this interaction; and auditing creates a log of security events that can be verified and checked to ensure the system is providing security. The end goal is some `assurance` that the system is secure.









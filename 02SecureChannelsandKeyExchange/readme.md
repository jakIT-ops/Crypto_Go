### Secure channel

The goal of this chapter is to set up a `secure channel` between two peers: one in which an attacker cannot eavesdrop or forge messages. Typically, we’ll use symmetric security to provide a secure channel, and some key exchange mechanism to set up the initial keys. This channel will be established in two directions, which means that there should be a separate set of keys (the combined encryption and authentication keys) for communications in both directions.

What does the secure channel look like? It’ll be message-oriented, for the same reasons described in the previous chapter. It will be built on top of an insecure channel, like the Internet, that can’t be trusted. An attacker might be able to disrupt or manipulate this insecure channel, for example; we also can’t hide how large messages are or who is talking. Ideally, messages will not be replayable or have their order changed (and that it will be apparent when either occurs).

The easiest way to prevent a replay is to keep track of message numbers; this number might be serialised as part of the message. For example, a message might be considered as the pairing of a message number and some message contents. We’ll track numbers for both sent and received messages.

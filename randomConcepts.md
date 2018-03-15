# Client - Server interactions
## HTTPS Handshake

Brief overview of process

1. Client sends a hello message with SSL version details, and cipherSuites supported by client. A random byte string is included and it will be used in all future communications from client

1. Server responds with cipherSuite chosen by server from the list sent by the client, session ID and another random byte string. The digital certificate is sent. 

1. Client verifies server certificate

1. client sends the server a random byte string that was encrypted from the server public key. this string will be used to encrypt all further communications between server and client. 

1. If the server sends a cert request, the client will respond with a key created from server's key and the clients private key, or a no cert message.

1. Server verifies client cert.

1. Client sends finished message

1. Server sends finished message

1. Now both client and server can send messages that are encrypted with the same secret key. 

## HTTP Handshake

to be filled in later...

# Coercion

two types: explicit, implicit

## Explicit

```
let a = 42;
let val = String( a ) || a.toString(); // "42"

```

## Implicit

```
let a = 42;
let val = a + ""; // "42"
```

## coercion weirdness

```
String(null) // "null"
String(undefined) // "undefined"

```

## This Keyword

parse [this](https://codeburst.io/javascript-the-keyword-this-for-beginners-fb5238d99f85) later.. then add more?
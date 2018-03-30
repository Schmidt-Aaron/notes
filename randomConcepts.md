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

Unary operator: attempts to convert the operand to a number

```
let numVal = +val // 42
+"3"  returns 3
```

## Coercion Weirdness

```
String(null) // "null"
String(undefined) // "undefined"

```

## This Keyword

Value of ```this``` typically determined by a function execution context.

In the Global Scope, ```this``` refers to the global object (window object)

When using a constructor (new _____) ```this``` refers to the new object bring created

```this``` can be explicitly bound with ```call()```, ```bind()```, and ```apply()```

*Note* that arrow functions do not bind ```this```. When using an arrow function ```this``` refers to the orginating context.

Add examples..

## Using ES6 to enforce required parameters

This nifty trick uses ES6 default values to make parameters required. It works by defining the default value for the parameters you want to be required to throw an error if called. That way, if the parameter is not included on the function call an error will be automatically thrown. Neat.

``` 
const required = () => {throw new Error('Missing parameter')};

// if either a, or b is not present when the function is called an error will be thrown
const add = (a = required(), b = required()) => a + b;

add (1, 2) // 3
add (1) // Error: Missing Parameter
```

## Using Reduce to count duplicates in an array.

```
const food = ['sammy', 'crackers', 'sammy', 'burger', 'burger'];

const foodObj = food.reduce((obj, name) => {
  obj[name] = obj[name] ? ++obj[name] : 1;
  return obj;
}, {}); // {sammy: 2, crackers: 1, burger: 2}
```

## Remove duplicates with Sets

Sets only allow unique values to be stores so...


```
let arr = [1, 1, 2, 2, 3, 4, 5, 4, 7];
let uniques = [...new Set(arr)] // [1,2, 3, 4, 5, 7]
```
Note that Sets default as objects so the [...] turns it into an array. 

## Swap values in an Array

```
let a = 5;
let b = 10;
console.log(`before a:${a}, b:${b}`); //before a:5, b:10

[a, b] = [b, a];
console.log(`after a:${a}, b:${b}`); //after a:10, b:5
```

## Use Promise.all and destructuring to recieve and assign multiple values

```
async function getFullPost(){
  return await Promise.all({
    fetch('/post'),
    fetch('/comments')
  });
}

const [post, comments] = getFullPost()
```

## Call, Apply, bind

can only be applied to functions;
allow the explicit binding of "this"; the first argument passed using one of the above methods will always be "this".

Call, and apply invoke the function immediately, while bind does not invoke the function. 

Call vs apply; the only difference is the parameters passed. 

call(this, a, b, c, d, ...) loose parameters -- no limit in number
apply(this, [a,b,c,d, ...]) // only two params
bind(this, a, b, c, d, ...)

when applied do not invoke the original function.
eg. obj.randomfn.apply(newThis) // like this 
obj.randomfn().apply(newThis) // nope!
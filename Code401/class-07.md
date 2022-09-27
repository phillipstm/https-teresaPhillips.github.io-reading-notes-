# Bearer Authorization

Intro to JWT

<https://jwt.io/introduction/>

1.What is a JSON Web Token (JWT)?

JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object.

This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA.

2.When should we use JSON Web Tokens?

**Authorization:** This is the most common scenario for using JWT. Once the user is logged in, each subsequent request will include the JWT, allowing the user to access routes, services, and resources that are permitted with that token. Single Sign On is a feature that widely uses JWT nowadays, because of its small overhead and its ability to be easily used across different domains.

**Information Exchange:** JSON Web Tokens are a good way of securely transmitting information between parties. Because JWTs can be signed—for example, using public/private key pairs—you can be sure the senders are who they say they are. Additionally, as the signature is calculated using the header and the payload, you can also verify that the content hasn't been tampered with.

3.Claims are expected in which structural component of a JWT?

**Payload-**  There are three types of claims: registered, public, and private claims.

**Registered claims:** These are a set of predefined claims which are not mandatory but recommended, to provide a set of useful, interoperable claims. Some of them are: iss (issuer), exp (expiration time), sub (subject), aud (audience), and others.

**Public claims:** These can be defined at will by those using JWTs. But to avoid collisions they should be defined in the IANA JSON Web Token Registry or be defined as a URI that contains a collision resistant namespace.

**Private claims:** These are the custom claims created to share information between parties that agree on using them and are neither registered or public claims.

## Are JWTs Secure?

<https://stackoverflow.com/questions/27301557/if-you-can-decode-jwt-how-are-they-secure>

1.If I get a JWT and I can decode the payload, how can we call that secure?

Because it is encrypted and only the players know the secret.

2.If sending a JWT, what must sender and receiver both know? Hint, it’s appended in the signature.

The secret.

3.Explain how concatenated content and secret can be sent and received securely to a non-technical recruiter.

Once someone has an authentification token. They are able to send and recieve data because all the parts are encrypted and the secret string is stored on a server which is sent back to the client and stored as either a cookie or in local storage. It is a unique key given to an individual that then allows access to data much like a social security number.

## JWTs Explained

<https://www.youtube.com/watch?v=926mknSW9Lo>

1.Why use JWT?

It is used to securely transfer information between any to entities. It is digitally signed, verified and trusted.

2.JWT is Compact and self-contained. Describe how this is useful to a non-technical friend.

It is useful because it is very fast and easy to transmit in a simple URL and it's self contained.

3.What are the three components (the structure) of a JWT signature?

Header
Payload
Signature

## Bookmark and Review

npm jsonwebtoken docs <https://www.npmjs.com/package/jsonwebtoken>

### Things I want to know more about

JWT Handbook for free <https://auth0.com/resources/ebooks/jwt-handbook?_ga=2.129222028.1647428752.1664280966-414631623.1664280966>

### Notes

In its compact form, JSON Web Tokens consist of three parts separated by dots (.), which are:

Header
Payload
Signature

**Install**
$ npm install jsonwebtoken

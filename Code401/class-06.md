# Authentication

## Securing Passwords

<https://thehackernews.com/2014/04/securing-passwords-with-bcrypt-hashing.html>

**Explain to a non-technical friend how you would safely hash and store a password.**

The benefit of hashing is that if someone steals the database with hashed passwords, they only make off with the hashes and not the actual plaintext passwords.

Cryptographic hash algorithms MD5, SHA1, SHA256, SHA512, SHA-3 are general purpose hash functions, designed to calculate a digest of huge amounts of data in as short a time as possible. Hashing is the greatest way for protecting passwords and considered to be pretty safe for ensuring the integrity of data or password.

**What is Bcrypt?**

An algorithm that uses a key stretching technique to fortify passwords. It's an adaptive hash function on the Blowfish symmetric block cipher cryptographic algorithm that adds a work factor(security), that allows a user to determine how expensive the hash function will be.

This work factor value determines how slow the hash function will be, means different work factor will generate different hash values in different time span, which makes it extremely resistant to brute force attacks. When computers become faster next year we can increase the work factor to balance it out i.e. to make the attack slower.

**Why might you use something like Bcrypt?**

A hacker would spend too much time, effort trying to break the password and would likely move on.

## Basic Auth

<https://en.wikipedia.org/wiki/Basic_access_authentication>

**What is Basic Authentication?**

HTTP Basic authentication (BA) implementation is the simplest technique for enforcing access controls to web resources because it does not require cookies, session identifiers, or login pages; rather, HTTP Basic authentication uses standard fields in the HTTP header.

HTTP Basic authentication (BA) implementation is the simplest technique for enforcing access controls to web resources because it does not require cookies, session identifiers, or login pages; rather, HTTP Basic authentication uses standard fields in the HTTP header.

A method for an HTTP user agent (e.g. a web browser) to provide a user name and password when making a request. In basic HTTP authentication, a request contains a header field in the form of Authorization: Basic <credentials>, where credentials is the Base64 encoding of ID and password joined by a single colon :.

Microsoft Internet Explorer <https://en.wikipedia.org/wiki/Internet_Explorer>
<  script>document.execCommand('ClearAuthenticationCache');</script>/

**What properties are necessary in the header of a Basic Auth request?**

**Server side**-

The WWW-Authenticate header field for basic authentication is constructed as following:

WWW-Authenticate: Basic realm="User Visible Realm"

The server may choose to include the charset parameter from RFC 7617:[3]Stack Overflow.

WWW-Authenticate: Basic realm="User Visible Realm", charset="UTF-8"

This parameter indicates that the server expects the client to use UTF-8 for encoding username and password (see below).

**Client side**-

When the user agent wants to send authentication credentials to the server, it may use the Authorization header field.

The Authorization header field is constructed as follows:[9]

1.The username and password are combined with a single colon (:). This means that the username itself cannot contain a colon.

2.The resulting string is encoded into an octet sequence. The character set to use for this encoding is by default unspecified, as long as it is compatible with US-ASCII, but the server may suggest use of UTF-8 by sending the charset parameter.[9],[Reschke, Julian. "The 'Basic' HTTP Authentication Scheme". tools.ietf.org.]
3.The resulting string is encoded using a variant of Base64 (+/ and with padding).
4.The authorization method and a space (e.g. "Basic ") is then prepended to the encoded string.

For example, if the browser uses Aladdin as the username and open sesame as the password, then the field's value is the Base64 encoding of Aladdin:open sesame, or QWxhZGRpbjpvcGVuIHNlc2FtZQ==. Then the Authorization header field will appear as:

Authorization: Basic QWxhZGRpbjpvcGVuIHNlc2FtZQ==

**How are username:password in Basic Auth encoded?**

As stated above.

## OWASP auth cheatsheet---!!!!! Everything Passwords

<https://www.owasp.org/index.php/Authentication_Cheat_Sheet>

**Define the authentication process to a non-technical recruiter.**

A process of verifying a person, website, or entity is who they say they are.

**How should your error messaging respond (both HTTP and HTML)? Why?**

Incorrectly implemented error messages in the case of authentication functionality can be used for the purposes of user ID and password enumeration.

**quick exit** Good example pseudo-code
IF USER_EXISTS(username) THEN
    password_hash=HASH(password)
    IS_VALID=LOOKUP_CREDENTIALS_IN_STORE(username, password_hash)
    IF NOT IS_VALID THEN
        RETURN Error("Invalid Username or Password!")
    ENDIF
ELSE
   RETURN Error("Invalid Username or Password!")
ENDIF

**Better** It doesn't give away which one errored to potential hacker.
password_hash=HASH(password)
IS_VALID=LOOKUP_CREDENTIALS_IN_STORE(username, password_hash)
IF NOT IS_VALID THEN
   RETURN Error("Invalid Username or Password!")
ENDIF



**Bookmark this link also and consider OWASP fundamentals any time you interact with authentication. Applications developed with security in mind from inception have fewer vulnerabilities throughout their lifecycle.**

### Bookmark and Review

**bcrypt docs**
<https://www.npmjs.com/package/bcrypt>

**Session Management Cheat Sheet** contains further guidance on the best practices in this area.
<https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html>

**Email address as a User ID**<https://cheatsheetseries.owasp.org/cheatsheets/Input_Validation_Cheat_Sheet.html#email-address-validation>

**Password Storage Cheat Sheet**<https://cheatsheetseries.owasp.org/cheatsheets/Password_Storage_Cheat_Sheet.html#maximum-password-lengths>

**Multifactor Authentication Cheat Sheet**<https://cheatsheetseries.owasp.org/cheatsheets/Multifactor_Authentication_Cheat_Sheet.html>


## Things I want to know more about

**Pwned Passwords**<> is a service where passwords can be checked against previously breached passwords. You can host it yourself or use the API.

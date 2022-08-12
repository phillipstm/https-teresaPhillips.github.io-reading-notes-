# Authentication

## What is OAuth

<https://www.csoonline.com/article/3216404/what-is-oauth-how-the-open-authorization-framework-works.html>

**What is OAuth?**

OAuth is an open-standard authorization protocol or framework that describes how unrelated servers and services can safely allow authenticated access to their assets without actually sharing the initial, related, single logon credential. In authentication parlance, this is known as secure, third-party, user-agent, delegated authorization.

**Give an example of what using OAuth would look like.**

OAuth scenario could be a user sending cloud-stored files to another user via email, when the cloud storage and email systems are otherwise unrelated other than supporting the OAuth framework (e.g., Google Gmail and Microsoft OneDrive). When the end-user attaches the files to their email and browses to select the files to attach, OAuth could be used behind the scenes to allow the email system to seamlessly authenticate and browse to the protected files without requiring a second logon to the file storage system.

**How does OAuth work? What are the steps that it takes to authenticate the user?**

_The first website connects to the second website on behalf of the user, using OAuth, providing the user’s verified identity.

-The second site generates a one-time token and a one-time secret unique to the transaction and parties involved.

-The first site gives this token and secret to the initiating user’s client software.

-The client’s software presents the request token and secret to their authorization provider (which may or may not be the second site).

-If not already authenticated to the authorization provider, the client may be asked to authenticate. After authentication, the client is asked to approve the authorization transaction to the second website.

-The user approves (or their software silently approves) a particular transaction type at the first website.

-The user is given an approved access token (notice it’s no longer a request token).

-The user gives the approved access token to the first website.

-The first website gives the access token to the second website as proof of authentication on behalf of the user.

-The second website lets the first website access their site on behalf of the user.

-The user sees a successfully completed transaction occurring.
OAuth is not the first authentication/authorization system to work this way on behalf of the end-user. In fact, many authentication systems, notably Kerberos, work similarly. What is special about OAuth is its ability to work across the web and its wide adoption. It succeeded with adoption rates where previous attempts failed (for various reasons).


**What is OpenID?**

StackOverflow pithily put it: "OpenID is for humans logging into machines, OAuth is for machines logging into machines on behalf of humans."

## Authorization and Authentication flows

<https://auth0.com/docs/flows>

**What is the difference between authorization and authentication?**

Authorization is the process of letting a subject access resources after a successful authentication.

**What is Authorization Code Flow?**

Because regular web apps are server-side apps where the source code is not publicly exposed, they can use the Authorization Code Flow (defined in OAuth 2.0 RFC 6749, section 4.1), which exchanges an Authorization Code for a token. Your app must be server-side because during this exchange, you must also pass along your application's Client Secret, which must always be kept secure, and you will have to store it in your client.

**What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?**

The PKCE-enhanced Authorization Code Flow introduces a secret created by the calling application that can be verified by the authorization server; this secret is called the Code Verifier. Additionally, the calling app creates a transform value of the Code Verifier called the Code Challenge and sends this value over HTTPS to retrieve an Authorization Code. This way, a malicious attacker can only intercept the Authorization Code, and they cannot exchange it for a token without the Code Verifier.

**What is Implicit Flow with Form Post?**

Implicit Flow with Form Post flow uses OpenID Connect (OIDC) to implement web sign-in that is very similar to the way SAML and WS-Federation operates. The web app requests and obtains tokens through the front channel, without the need for secrets or extra backend calls. With this method, you don’t need to obtain, maintain, use, and protect a secret in your application.

**What is Client Credentials Flow?**

With machine-to-machine (M2M) applications, such as CLIs, daemons, or services running on your back-end, the system authenticates and authorizes the app rather than a user.

**What is Device Authorization Flow?**

With input-constrained devices that connect to the internet, rather than authenticate the user directly, the device asks the user to go to a link on their computer or smartphone and authorize the device.

**What is Resource Owner Password Flow?**

Though we do not recommend it, highly-trusted applications can use the Resource Owner Password Flow (defined in OAuth 2.0 RFC 6749, section 4.3), which requests that users provide credentials (username and password), typically using an interactive form. Because credentials are sent to the backend and can be stored for future use before being exchanged for an Access Token, it is imperative that the application is absolutely trusted with this information.

## Videos

### Auth0 for single page apps

<https://auth0.com/docs/libraries/auth0-react>

The Auth0 React SDK handles grant and protocol details, token expiration and renewal, as well as token storage and caching. Under the hood, it implements Universal Login and the Authorization Code Grant Flow with PKCE.


Auth0 React SDK for Single Page Apps
The Auth0 React SDK (auth0-react.js) is a JavaScript library for implementing authentication and authorization in React apps with Auth0. It provides a custom React hook and other Higher Order Components so you can secure React apps using best practices while writing less code.

The Auth0 React SDK handles grant and protocol details, token expiration and renewal, as well as token storage and caching. Under the hood, it implements Universal Login and the Authorization Code Grant Flow with PKCE.

The library is hosted on GitHub where you can read more about the API.

**Installation**
You have a few options for using auth0-react.js in your project.

**From the CDN:** <"https://cdn.auth0.com/js/auth0-react/1.2.0/auth0-react.min.js">>[</script>]

**From npm:**

npm install @auth0/auth0-react

**From yarn:** yarn add @auth0/auth0-react

import React from 'react';
    import ReactDOM from 'react-dom';
    **import { Auth0Provider } from '@auth0/auth0-react';**
    import App from './App';
    ReactDOM.render(
      <Auth0Provider
        domain="YOUR_DOMAIN"
        clientId="YOUR_CLIENT_ID"
        redirectUri={window.location.origin}
    >
      <App />
    </Auth0Provider>,
    document.getElementById('app')
 );

## Things I want to know more about

GOOD RESOURCE TO SET UP AUTH0
**<https://auth0.com/docs/libraries/auth0-react>**

How to determine the best authorization option when setting up a website.

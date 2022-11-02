# < Login /> and < Auth />

## What is Role Based Access Control (RBAC)?

<https://digitalguardian.com/blog/what-role-based-access-control-rbac-examples-benefits-and-more>

**What is Role Based Access Control (RBAC)?**
    Role-based access control (RBAC) restricts network access based on a person's role within an organization and has become one of the main methods for advanced access control. The roles in RBAC refer to the levels of access that employees have to the network.

**Share some an example of RBAC including all possible CRUD operations and correlating roles.**
    Management role scope – it limits what objects the role group is allowed to manage.
    Management role group – you can add and remove members.
    Management role – these are the types of tasks that can be performed by a specific role group.
    Management role assignment – this links a role to a role group.

    Primary – the primary contact for a specific account or role.
    Billing – access for one end-user to the billing account.
    Technical – assigned to users that perform technical tasks.
    Administrative – access for users that perform administrative tasks.

**What are the Benefits of RBAC?**
    An RBAC system can ensure the company's information meets privacy and confidentiality regulations. Furthermore, it can secure key business processes, including access to IP, that affect the business from a competitive standpoint.

## Compare and Contrast the following two Libraries

**react-cookie library**
<https://www.npmjs.com/package/react-cookie>

**react-cookies component**
<https://www.npmjs.com/package/react-cookies>

**Describe some react-cookie features.**
    Library features
    universal-cookie - Universal cookies for JavaScript
    universal-cookie-express - Hook cookies get/set on Express for server-rendering

    **npm install react-cookie**

    **<CookiesProvider />**
    Set the user cookies

    On the server, the cookies props must be set using req.universalCookies or new Cookie(cookieHeader)

    **useCookies([dependencies])**
    Access and modify cookies using React hooks.

    const [cookies, setCookie, removeCookie] = useCookies(['cookie-name']);
    dependencies (optional)
    Let you optionally specify a list of cookie names your component depend on or that should trigger a re-render. If unspecified, it will render on every cookie change.

    **cookies**
    Javascript object with all your cookies. The key is the cookie name.

    **setCookie(name, value, [options])**
    Set a cookie value

    name (string): cookie name
    value (string|object): save the value and stringify the object if needed
    options (object): Support all the cookie options from RFC 6265
    path (string): cookie path, use / as the path if you want your cookie to be accessible on all pages
    expires (Date): absolute expiration date for the cookie
    maxAge (number): relative max age of the cookie from when the client receives it in seconds
    domain (string): domain for the cookie (sub.domain.com or .allsubdomains.com)
    secure (boolean): Is only accessible through HTTPS?
    httpOnly (boolean): Can only the server access the cookie? Note: You cannot get or set httpOnly cookies from the browser, only the server.
    sameSite (boolean|none|lax|strict): Strict or Lax enforcement
    **removeCookie(name, [options])**

    **React-cookie components**
    $ npm install react-cookies --save

    Isomorphic cookies!
    To be able to access user cookies while doing server-rendering, you can use plugToRequest or setRawCookie.

    API
    load(name, [doNotParse])-load cookie value.

    .loadAll()-Load all available cookies. Returns an object containing all cookies.

    .select([regex])-Find all the cookies with a name that match the regex. Returns an object with the cookie name as the key.

    .save(name, value, [options])-Set a cookie.

    path-Cookie path. Use / as the path if you want your cookie to be accessible on all pages.

    expires-Absolute expiration date for the cookie.

    maxAge-Relative max age of the cookie from when the client receives it in seconds.

    domain-Domain for the cookie. Use https://*.yourdomain.com if you want to access the cookie in all your subdomains.

    secure-If set true it will only be accessible through https.

    httpOnly-If set true it will only be accessible on the server.

    .remove(name, [options])-Remove a cookie.

    .plugToRequest(req, res): unplug()-Load the user cookies so you can do server-rendering and match the same result.
    Also send back to the user the new cookies.
    Work with connect or express.js by using the cookieParser middleware first.
    Use const unplug = plugToRequest(req, res) just before your renderToString.
    Returns unplug() function so it stops setting cookies on the response.

    .setRawCookie(cookies)-Load the user cookies so you can do server-rendering and match the same result.
    Use setRawCookie(headers.cookie) just before your renderToString.
    Make sure it is the raw string from the request headers.

**Describe some react-cookies features.**
    Cookies
    get(name, [options])
    getAll([options])
    set(name, value, [options])
    remove(name, [options])

**Which library would you prefer would you prefer? Why?**

I think it would depend on what it is being used for.

## Things I want to know more about

How to best determine which one to use.

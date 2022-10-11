# Interface: NextAuthOptions

[index](../modules/index.md).NextAuthOptions

Configure your NextAuth instance

[Documentation](https://next-auth.js.org/configuration/options#options)

## Table of contents

### Properties

- [providers](index.NextAuthOptions.md#providers)
- [adapter](index.NextAuthOptions.md#adapter)
- [callbacks](index.NextAuthOptions.md#callbacks)
- [cookies](index.NextAuthOptions.md#cookies)
- [debug](index.NextAuthOptions.md#debug)
- [events](index.NextAuthOptions.md#events)
- [jwt](index.NextAuthOptions.md#jwt)
- [logger](index.NextAuthOptions.md#logger)
- [pages](index.NextAuthOptions.md#pages)
- [secret](index.NextAuthOptions.md#secret)
- [session](index.NextAuthOptions.md#session)
- [theme](index.NextAuthOptions.md#theme)
- [useSecureCookies](index.NextAuthOptions.md#usesecurecookies)

## Properties

### providers

• **providers**: `Provider`[]

An array of authentication providers for signing in
(e.g. Google, Facebook, Twitter, GitHub, Email, etc) in any order.
This can be one of the built-in providers or an object with a custom provider.
* **Default value**: `[]`
* **Required**: *Yes*

[Documentation](https://next-auth.js.org/configuration/options#providers) | [Providers documentation](https://next-auth.js.org/configuration/providers)

___

### adapter

• `Optional` **adapter**: [`Adapter`](../types/adapters.Adapter.md)<`boolean`\>

You can use the adapter option to pass in your database adapter.

* **Required**: *No*

[Documentation](https://next-auth.js.org/configuration/options#adapter) |
[Adapters Overview](https://next-auth.js.org/adapters/overview)

___

### callbacks

• `Optional` **callbacks**: `Partial`<[`CallbacksOptions`](index.CallbacksOptions.md)<[`Profile`](index.Profile.md), [`Account`](index.Account.md)\>\>

Callbacks are asynchronous functions you can use to control what happens when an action is performed.
Callbacks are *extremely powerful*, especially in scenarios involving JSON Web Tokens
as they **allow you to implement access controls without a database** and to **integrate with external databases or APIs**.
* **Default value**: See the Callbacks documentation
* **Required**: *No*

[Documentation](https://next-auth.js.org/configuration/options#callbacks) | [Callbacks documentation](https://next-auth.js.org/configuration/callbacks)

___

### cookies

• `Optional` **cookies**: `Partial`<[`CookiesOptions`](index.CookiesOptions.md)\>

You can override the default cookie names and options for any of the cookies used by NextAuth.js.
You can specify one or more cookies with custom properties,
but if you specify custom options for a cookie you must provide all the options for that cookie.
If you use this feature, you will likely want to create conditional behavior
to support setting different cookies policies in development and production builds,
as you will be opting out of the built-in dynamic policy.
* **Default value**: `{}`
* **Required**: No

- ⚠ **This is an advanced option.** Advanced options are passed the same way as basic options,
but **may have complex implications** or side effects.
You should **try to avoid using advanced options** unless you are very comfortable using them.

[Documentation](https://next-auth.js.org/configuration/options#cookies) | [Usage example](https://next-auth.js.org/configuration/options#example)

___

### debug

• `Optional` **debug**: `boolean`

Set debug to true to enable debug messages for authentication and database operations.
* **Default value**: `false`
* **Required**: *No*

- ⚠ If you added a custom `logger`, this setting is ignored.

[Documentation](https://next-auth.js.org/configuration/options#debug) | [Logger documentation](https://next-auth.js.org/configuration/options#logger)

___

### events

• `Optional` **events**: `Partial`<[`EventCallbacks`](index.EventCallbacks.md)\>

Events are asynchronous functions that do not return a response, they are useful for audit logging.
You can specify a handler for any of these events below - e.g. for debugging or to create an audit log.
The content of the message object varies depending on the flow
(e.g. OAuth or Email authentication flow, JWT or database sessions, etc),
but typically contains a user object and/or contents of the JSON Web Token
and other information relevant to the event.
* **Default value**: `{}`
* **Required**: *No*

[Documentation](https://next-auth.js.org/configuration/options#events) | [Events documentation](https://next-auth.js.org/configuration/events)

___

### jwt

• `Optional` **jwt**: `Partial`<[`JWTOptions`](jwt.JWTOptions.md)\>

JSON Web Tokens are enabled by default if you have not specified a database.
By default JSON Web Tokens are signed (JWS) but not encrypted (JWE),
as JWT encryption adds additional overhead and comes with some caveats.
You can enable encryption by setting `encryption: true`.
* **Default value**: See the documentation page
* **Required**: *No*

[Documentation](https://next-auth.js.org/configuration/options#jwt)

___

### logger

• `Optional` **logger**: `Partial`<[`LoggerInstance`](index.LoggerInstance.md)\>

Override any of the logger levels (`undefined` levels will use the built-in logger),
and intercept logs in NextAuth. You can use this option to send NextAuth logs to a third-party logging service.
* **Default value**: `console`
* **Required**: *No*

**`Example`**

```js
// /pages/api/auth/[...nextauth].js
import log from "logging-service"
export default NextAuth({
  logger: {
    error(code, ...message) {
      log.error(code, message)
    },
    warn(code, ...message) {
      log.warn(code, message)
    },
    debug(code, ...message) {
      log.debug(code, message)
    }
  }
})
```

- ⚠ When set, the `debug` option is ignored

[Documentation](https://next-auth.js.org/configuration/options#logger) |
[Debug documentation](https://next-auth.js.org/configuration/options#debug)

___

### pages

• `Optional` **pages**: `Partial`<[`PagesOptions`](index.PagesOptions.md)\>

Specify URLs to be used if you want to create custom sign in, sign out and error pages.
Pages specified will override the corresponding built-in page.
* **Default value**: `{}`
* **Required**: *No*

**`Example`**

```js
  pages: {
    signIn: '/auth/signin',
    signOut: '/auth/signout',
    error: '/auth/error',
    verifyRequest: '/auth/verify-request',
    newUser: '/auth/new-user'
  }
```

[Documentation](https://next-auth.js.org/configuration/options#pages) | [Pages documentation](https://next-auth.js.org/configuration/pages)

___

### secret

• `Optional` **secret**: `string`

A random string used to hash tokens, sign cookies and generate cryptographic keys.
If not specified, it falls back to `jwt.secret` or `NEXTAUTH_SECRET` from environment vairables.
Otherwise it will use a hash of all configuration options, including Client ID / Secrets for entropy.

NOTE: The last behavior is extrmely volatile, and will throw an error in production.
* **Default value**: `string` (SHA hash of the "options" object)
* **Required**: No - **but strongly recommended**!

[Documentation](https://next-auth.js.org/configuration/options#secret)

___

### session

• `Optional` **session**: `Partial`<[`SessionOptions`](index.SessionOptions.md)\>

Configure your session like if you want to use JWT or a database,
how long until an idle session expires, or to throttle write operations in case you are using a database.
* **Default value**: See the documentation page
* **Required**: No

[Documentation](https://next-auth.js.org/configuration/options#session)

___

### theme

• `Optional` **theme**: [`Theme`](index.Theme.md)

Changes the theme of pages.
Set to `"light"` if you want to force pages to always be light.
Set to `"dark"` if you want to force pages to always be dark.
Set to `"auto"`, (or leave this option out)if you want the pages to follow the preferred system theme.
* **Default value**: `"auto"`
* **Required**: *No*

[Documentation](https://next-auth.js.org/configuration/options#theme) | [Pages documentation]("https://next-auth.js.org/configuration/pages")

___

### useSecureCookies

• `Optional` **useSecureCookies**: `boolean`

When set to `true` then all cookies set by NextAuth.js will only be accessible from HTTPS URLs.
This option defaults to `false` on URLs that start with `http://` (e.g. http://localhost:3000) for developer convenience.
You can manually set this option to `false` to disable this security feature and allow cookies
to be accessible from non-secured URLs (this is not recommended).
* **Default value**: `true` for HTTPS and `false` for HTTP sites
* **Required**: No

[Documentation](https://next-auth.js.org/configuration/options#usesecurecookies)

- ⚠ **This is an advanced option.** Advanced options are passed the same way as basic options,
but **may have complex implications** or side effects.
You should **try to avoid using advanced options** unless you are very comfortable using them.

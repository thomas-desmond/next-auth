# Interface: SessionOptions

[Documentation](https://next-auth.js.org/configuration/options#session)

## Table of contents

### Properties

- [generateSessionToken](SessionOptions.md#generatesessiontoken)
- [maxAge](SessionOptions.md#maxage)
- [strategy](SessionOptions.md#strategy)
- [updateAge](SessionOptions.md#updateage)

## Properties

### generateSessionToken

• **generateSessionToken**: () => `string`

#### Type declaration

▸ (): `string`

Generate a custom session token for database-based sessions.
By default, a random UUID or string is generated depending on the Node.js version.
However, you can specify your own custom string (such as CUID) to be used.

**`Default`**

`randomUUID` or `randomBytes.toHex` depending on the Node.js version

##### Returns

`string`

___

### maxAge

• **maxAge**: `number`

Relative time from now in seconds when to expire the session

**`Default`**

2592000 // 30 days

___

### strategy

• **strategy**: [`SessionStrategy`](../types/SessionStrategy.md)

Choose how you want to save the user session.
The default is `"jwt"`, an encrypted JWT (JWE) in the session cookie.

If you use an `adapter` however, we default it to `"database"` instead.
You can still force a JWT session by explicitly defining `"jwt"`.

When using `"database"`, the session cookie will only contain a `sessionToken` value,
which is used to look up the session in the database.

[Documentation](https://next-auth.js.org/configuration/options#session) | [Adapter](https://next-auth.js.org/configuration/options#adapter) | [About JSON Web Tokens](https://next-auth.js.org/faq#json-web-tokens)

___

### updateAge

• **updateAge**: `number`

How often the session should be updated in seconds.
If set to `0`, session is updated every time.

**`Default`**

86400 // 1 day

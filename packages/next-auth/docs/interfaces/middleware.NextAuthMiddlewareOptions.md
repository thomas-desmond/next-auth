# Interface: NextAuthMiddlewareOptions

[middleware](../modules/middleware.md).NextAuthMiddlewareOptions

## Table of contents

### Properties

- [callbacks](middleware.NextAuthMiddlewareOptions.md#callbacks)
- [cookies](middleware.NextAuthMiddlewareOptions.md#cookies)
- [jwt](middleware.NextAuthMiddlewareOptions.md#jwt)
- [pages](middleware.NextAuthMiddlewareOptions.md#pages)
- [secret](middleware.NextAuthMiddlewareOptions.md#secret)

## Properties

### callbacks

• `Optional` **callbacks**: `Object`

#### Type declaration

| Name | Type | Description |
| :------ | :------ | :------ |
| `authorized?` | `AuthorizedCallback` | Callback that receives the user's JWT payload and returns `true` to allow the user to continue.  This is similar to the `signIn` callback in `NextAuthOptions`.  If it returns `false`, the user is redirected to the sign-in page instead  The default is to let the user continue if they have a valid JWT (basic authentication).  How to restrict a page and all of it's subpages for admins-only:  **`Example`**  ```js // `middleware.js` import { withAuth } from "next-auth/middleware"  export default withAuth({   callbacks: {     authorized: ({ token }) => token?.user.isAdmin   } })  export const config = { matcher: ["/admin"] }  ```  --- [Documentation](https://next-auth.js.org/configuration/nextjs#middleware) \| [`signIn` callback](configuration/callbacks#sign-in-callback) |

___

### cookies

• `Optional` **cookies**: `Partial`<`Record`<``"sessionToken"``, `Omit`<[`CookieOption`](index.CookieOption.md), ``"options"``\>\>\>

You can override the default cookie names and options for any of the cookies
by this middleware. Similar to `cookies` in `NextAuth`.

Useful if the token is stored in not a default cookie.

---
[Documentation](https://next-auth.js.org/configuration/options#cookies)

- ⚠ **This is an advanced option.** Advanced options are passed the same way as basic options,
but **may have complex implications** or side effects.
You should **try to avoid using advanced options** unless you are very comfortable using them.

___

### jwt

• `Optional` **jwt**: `Partial`<`Pick`<[`JWTOptions`](jwt.JWTOptions.md), ``"decode"``\>\>

If a custom jwt `decode` method is set in `[...nextauth].ts`, the same method should be set here also.

---
[Documentation](https://next-auth.js.org/configuration/nextjs#custom-jwt-decode-method)

___

### pages

• `Optional` **pages**: `Partial`<[`PagesOptions`](index.PagesOptions.md)\>

Where to redirect the user in case of an error if they weren't logged in.
Similar to `pages` in `NextAuth`.

---
[Documentation](https://next-auth.js.org/configuration/pages)

___

### secret

• `Optional` **secret**: `string`

The same `secret` used in the `NextAuth` configuration.
Defaults to the `NEXTAUTH_SECRET` environment variable.

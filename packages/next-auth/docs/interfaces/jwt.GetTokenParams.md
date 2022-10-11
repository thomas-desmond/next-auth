# Interface: GetTokenParams<R\>

[jwt](../modules/jwt.md).GetTokenParams

## Type parameters

| Name | Type |
| :------ | :------ |
| `R` | extends `boolean` = ``false`` |

## Table of contents

### Properties

- [req](jwt.GetTokenParams.md#req)
- [cookieName](jwt.GetTokenParams.md#cookiename)
- [decode](jwt.GetTokenParams.md#decode)
- [logger](jwt.GetTokenParams.md#logger)
- [raw](jwt.GetTokenParams.md#raw)
- [secret](jwt.GetTokenParams.md#secret)
- [secureCookie](jwt.GetTokenParams.md#securecookie)

## Properties

### req

• **req**: `IncomingMessage` & {} \| `NextRequest` \| `NextApiRequest`

The request containing the JWT either in the cookies or in the `Authorization` header.

___

### cookieName

• `Optional` **cookieName**: `string`

If the JWT is in the cookie, what name `getToken()` should look for.

___

### decode

• `Optional` **decode**: (`params`: [`JWTDecodeParams`](jwt.JWTDecodeParams.md)) => [`Awaitable`](../types/index.Awaitable.md)<``null`` \| [`JWT`](jwt.JWT.md)\>

#### Type declaration

▸ (`params`): [`Awaitable`](../types/index.Awaitable.md)<``null`` \| [`JWT`](jwt.JWT.md)\>

Override this method to control the NextAuth.js issued JWT decoding.

##### Parameters

| Name | Type |
| :------ | :------ |
| `params` | [`JWTDecodeParams`](jwt.JWTDecodeParams.md) |

##### Returns

[`Awaitable`](../types/index.Awaitable.md)<``null`` \| [`JWT`](jwt.JWT.md)\>

___

### logger

• `Optional` **logger**: [`LoggerInstance`](index.LoggerInstance.md) \| `Console`

___

### raw

• `Optional` **raw**: `R`

`getToken()` will return the raw JWT if this is set to `true`

**`Default`**

false

___

### secret

• `Optional` **secret**: `string`

The same `secret` used in the `NextAuth` configuration.
Defaults to the `NEXTAUTH_SECRET` environment variable.

___

### secureCookie

• `Optional` **secureCookie**: `boolean`

Use secure prefix for cookie name, unless URL in `NEXTAUTH_URL` is http://
or not set (e.g. development or test instance) case use unprefixed name

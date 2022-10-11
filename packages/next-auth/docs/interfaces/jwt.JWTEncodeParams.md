# Interface: JWTEncodeParams

[jwt](../modules/jwt.md).JWTEncodeParams

## Table of contents

### Properties

- [secret](jwt.JWTEncodeParams.md#secret)
- [maxAge](jwt.JWTEncodeParams.md#maxage)
- [token](jwt.JWTEncodeParams.md#token)

## Properties

### secret

• **secret**: `string` \| `Buffer`

The secret used to encode the NextAuth.js issued JWT.

___

### maxAge

• `Optional` **maxAge**: `number`

The maximum age of the NextAuth.js issued JWT in seconds.

**`Default`**

30 * 24 * 30 * 60 // 30 days

___

### token

• `Optional` **token**: [`JWT`](jwt.JWT.md)

The JWT payload.

# Interface: JWTOptions

[jwt](../modules/jwt.md).JWTOptions

## Table of contents

### Properties

- [decode](jwt.JWTOptions.md#decode)
- [encode](jwt.JWTOptions.md#encode)
- [maxAge](jwt.JWTOptions.md#maxage)
- [secret](jwt.JWTOptions.md#secret)

## Properties

### decode

• **decode**: (`params`: [`JWTDecodeParams`](jwt.JWTDecodeParams.md)) => [`Awaitable`](../types/index.Awaitable.md)<``null`` \| [`JWT`](jwt.JWT.md)\>

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

### encode

• **encode**: (`params`: [`JWTEncodeParams`](jwt.JWTEncodeParams.md)) => [`Awaitable`](../types/index.Awaitable.md)<`string`\>

#### Type declaration

▸ (`params`): [`Awaitable`](../types/index.Awaitable.md)<`string`\>

Override this method to control the NextAuth.js issued JWT encoding.

##### Parameters

| Name | Type |
| :------ | :------ |
| `params` | [`JWTEncodeParams`](jwt.JWTEncodeParams.md) |

##### Returns

[`Awaitable`](../types/index.Awaitable.md)<`string`\>

___

### maxAge

• **maxAge**: `number`

The maximum age of the NextAuth.js issued JWT in seconds.

**`Default`**

30 * 24 * 30 * 60 // 30 days

___

### secret

• **secret**: `string`

The secret used to encode/decode the NextAuth.js issued JWT.

**`Deprecated`**

Set the `NEXTAUTH_SECRET` environment vairable or
use the top-level `secret` option instead

# Interface: JWT

[jwt](../modules/jwt.md).JWT

Returned by the `jwt` callback and `getToken`, when using JWT sessions

[`jwt` callback](https://next-auth.js.org/configuration/callbacks#jwt-callback) | [`getToken`](https://next-auth.js.org/tutorials/securing-pages-and-api-routes#using-gettoken)

## Hierarchy

- `Record`<`string`, `unknown`\>

- [`DefaultJWT`](jwt.DefaultJWT.md)

  ↳ **`JWT`**

## Table of contents

### Properties

- [email](jwt.JWT.md#email)
- [name](jwt.JWT.md#name)
- [picture](jwt.JWT.md#picture)
- [sub](jwt.JWT.md#sub)

## Properties

### email

• `Optional` **email**: ``null`` \| `string`

#### Inherited from

[DefaultJWT](jwt.DefaultJWT.md).[email](jwt.DefaultJWT.md#email)

___

### name

• `Optional` **name**: ``null`` \| `string`

#### Inherited from

[DefaultJWT](jwt.DefaultJWT.md).[name](jwt.DefaultJWT.md#name)

___

### picture

• `Optional` **picture**: ``null`` \| `string`

#### Inherited from

[DefaultJWT](jwt.DefaultJWT.md).[picture](jwt.DefaultJWT.md#picture)

___

### sub

• `Optional` **sub**: `string`

#### Inherited from

[DefaultJWT](jwt.DefaultJWT.md).[sub](jwt.DefaultJWT.md#sub)

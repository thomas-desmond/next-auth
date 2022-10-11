# Interface: AdapterUser

[adapters](../modules/adapters.md).AdapterUser

The shape of the returned object in the OAuth providers' `profile` callback,
available in the `jwt` and `session` callbacks,
or the second parameter of the `session` callback, when using a database.

[`signIn` callback](https://next-auth.js.org/configuration/callbacks#sign-in-callback) |
[`session` callback](https://next-auth.js.org/configuration/callbacks#jwt-callback) |
[`jwt` callback](https://next-auth.js.org/configuration/callbacks#jwt-callback) |
[`profile` OAuth provider callback](https://next-auth.js.org/configuration/providers#using-a-custom-provider)

## Hierarchy

- [`User`](index.User.md)

  ↳ **`AdapterUser`**

## Table of contents

### Properties

- [email](adapters.AdapterUser.md#email)
- [emailVerified](adapters.AdapterUser.md#emailverified)
- [id](adapters.AdapterUser.md#id)
- [image](adapters.AdapterUser.md#image)
- [name](adapters.AdapterUser.md#name)

## Properties

### email

• **email**: `string`

#### Overrides

[User](index.User.md).[email](index.User.md#email)

___

### emailVerified

• **emailVerified**: ``null`` \| `Date`

___

### id

• **id**: `string`

#### Overrides

[User](index.User.md).[id](index.User.md#id)

___

### image

• `Optional` **image**: ``null`` \| `string`

#### Inherited from

[User](index.User.md).[image](index.User.md#image)

___

### name

• `Optional` **name**: ``null`` \| `string`

#### Inherited from

[User](index.User.md).[name](index.User.md#name)

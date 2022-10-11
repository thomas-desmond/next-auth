# Interface: User

[index](../modules/index.md).User

The shape of the returned object in the OAuth providers' `profile` callback,
available in the `jwt` and `session` callbacks,
or the second parameter of the `session` callback, when using a database.

[`signIn` callback](https://next-auth.js.org/configuration/callbacks#sign-in-callback) |
[`session` callback](https://next-auth.js.org/configuration/callbacks#jwt-callback) |
[`jwt` callback](https://next-auth.js.org/configuration/callbacks#jwt-callback) |
[`profile` OAuth provider callback](https://next-auth.js.org/configuration/providers#using-a-custom-provider)

## Hierarchy

- [`DefaultUser`](index.DefaultUser.md)

  ↳ **`User`**

  ↳↳ [`AdapterUser`](adapters.AdapterUser.md)

## Table of contents

### Properties

- [id](index.User.md#id)
- [email](index.User.md#email)
- [image](index.User.md#image)
- [name](index.User.md#name)

## Properties

### id

• **id**: `string`

#### Inherited from

[DefaultUser](index.DefaultUser.md).[id](index.DefaultUser.md#id)

___

### email

• `Optional` **email**: ``null`` \| `string`

#### Inherited from

[DefaultUser](index.DefaultUser.md).[email](index.DefaultUser.md#email)

___

### image

• `Optional` **image**: ``null`` \| `string`

#### Inherited from

[DefaultUser](index.DefaultUser.md).[image](index.DefaultUser.md#image)

___

### name

• `Optional` **name**: ``null`` \| `string`

#### Inherited from

[DefaultUser](index.DefaultUser.md).[name](index.DefaultUser.md#name)

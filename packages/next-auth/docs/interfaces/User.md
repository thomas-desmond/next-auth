# Interface: User

The shape of the returned object in the OAuth providers' `profile` callback,
available in the `jwt` and `session` callbacks,
or the second parameter of the `session` callback, when using a database.

[`signIn` callback](https://next-auth.js.org/configuration/callbacks#sign-in-callback) |
[`session` callback](https://next-auth.js.org/configuration/callbacks#jwt-callback) |
[`jwt` callback](https://next-auth.js.org/configuration/callbacks#jwt-callback) |
[`profile` OAuth provider callback](https://next-auth.js.org/configuration/providers#using-a-custom-provider)

## Hierarchy

- [`DefaultUser`](DefaultUser.md)

  ↳ **`User`**

## Table of contents

### Properties

- [id](User.md#id)
- [email](User.md#email)
- [image](User.md#image)
- [name](User.md#name)

## Properties

### id

• **id**: `string`

#### Inherited from

[DefaultUser](DefaultUser.md).[id](DefaultUser.md#id)

___

### email

• `Optional` **email**: ``null`` \| `string`

#### Inherited from

[DefaultUser](DefaultUser.md).[email](DefaultUser.md#email)

___

### image

• `Optional` **image**: ``null`` \| `string`

#### Inherited from

[DefaultUser](DefaultUser.md).[image](DefaultUser.md#image)

___

### name

• `Optional` **name**: ``null`` \| `string`

#### Inherited from

[DefaultUser](DefaultUser.md).[name](DefaultUser.md#name)

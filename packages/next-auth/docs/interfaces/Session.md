# Interface: Session

Returned by `useSession`, `getSession`, returned by the `session` callback
and also the shape received as a prop on the `SessionProvider` React Context

[`useSession`](https://next-auth.js.org/getting-started/client#usesession) |
[`getSession`](https://next-auth.js.org/getting-started/client#getsession) |
[`SessionProvider`](https://next-auth.js.org/getting-started/client#sessionprovider) |
[`session` callback](https://next-auth.js.org/configuration/callbacks#jwt-callback)

## Hierarchy

- [`DefaultSession`](DefaultSession.md)

  ↳ **`Session`**

## Table of contents

### Properties

- [expires](Session.md#expires)
- [user](Session.md#user)

## Properties

### expires

• **expires**: `string`

#### Inherited from

[DefaultSession](DefaultSession.md).[expires](DefaultSession.md#expires)

___

### user

• `Optional` **user**: `Object`

#### Type declaration

| Name | Type |
| :------ | :------ |
| `email?` | ``null`` \| `string` |
| `image?` | ``null`` \| `string` |
| `name?` | ``null`` \| `string` |

#### Inherited from

[DefaultSession](DefaultSession.md).[user](DefaultSession.md#user)

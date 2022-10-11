# Interface: EventCallbacks

[index](../modules/index.md).EventCallbacks

The various event callbacks you can register for from next-auth

[Documentation](https://next-auth.js.org/configuration/events)

## Table of contents

### Properties

- [createUser](index.EventCallbacks.md#createuser)
- [linkAccount](index.EventCallbacks.md#linkaccount)
- [session](index.EventCallbacks.md#session)
- [signIn](index.EventCallbacks.md#signin)
- [signOut](index.EventCallbacks.md#signout)
- [updateUser](index.EventCallbacks.md#updateuser)

## Properties

### createUser

• **createUser**: (`message`: { `user`: [`User`](index.User.md)  }) => [`Awaitable`](../types/index.Awaitable.md)<`void`\>

#### Type declaration

▸ (`message`): [`Awaitable`](../types/index.Awaitable.md)<`void`\>

##### Parameters

| Name | Type |
| :------ | :------ |
| `message` | `Object` |
| `message.user` | [`User`](index.User.md) |

##### Returns

[`Awaitable`](../types/index.Awaitable.md)<`void`\>

___

### linkAccount

• **linkAccount**: (`message`: { `account`: [`Account`](index.Account.md) ; `profile`: [`User`](index.User.md) \| [`AdapterUser`](adapters.AdapterUser.md) \| { `email`: `string`  } ; `user`: [`User`](index.User.md) \| [`AdapterUser`](adapters.AdapterUser.md) \| { `email`: `string`  }  }) => [`Awaitable`](../types/index.Awaitable.md)<`void`\>

#### Type declaration

▸ (`message`): [`Awaitable`](../types/index.Awaitable.md)<`void`\>

##### Parameters

| Name | Type |
| :------ | :------ |
| `message` | `Object` |
| `message.account` | [`Account`](index.Account.md) |
| `message.profile` | [`User`](index.User.md) \| [`AdapterUser`](adapters.AdapterUser.md) \| { `email`: `string`  } |
| `message.user` | [`User`](index.User.md) \| [`AdapterUser`](adapters.AdapterUser.md) \| { `email`: `string`  } |

##### Returns

[`Awaitable`](../types/index.Awaitable.md)<`void`\>

___

### session

• **session**: (`message`: { `session`: [`Session`](index.Session.md) ; `token`: [`JWT`](jwt.JWT.md)  }) => [`Awaitable`](../types/index.Awaitable.md)<`void`\>

#### Type declaration

▸ (`message`): [`Awaitable`](../types/index.Awaitable.md)<`void`\>

The message object will contain one of these depending on
if you use JWT or database persisted sessions:
- `token`: The JWT token for this session.
- `session`: The session object from your adapter.

##### Parameters

| Name | Type |
| :------ | :------ |
| `message` | `Object` |
| `message.session` | [`Session`](index.Session.md) |
| `message.token` | [`JWT`](jwt.JWT.md) |

##### Returns

[`Awaitable`](../types/index.Awaitable.md)<`void`\>

___

### signIn

• **signIn**: (`message`: { `account`: ``null`` \| [`Account`](index.Account.md) ; `user`: [`User`](index.User.md) ; `isNewUser?`: `boolean` ; `profile?`: [`Profile`](index.Profile.md)  }) => [`Awaitable`](../types/index.Awaitable.md)<`void`\>

#### Type declaration

▸ (`message`): [`Awaitable`](../types/index.Awaitable.md)<`void`\>

If using a `credentials` type auth, the user is the raw response from your
credential provider.
For other providers, you'll get the User object from your adapter, the account,
and an indicator if the user was new to your Adapter.

##### Parameters

| Name | Type |
| :------ | :------ |
| `message` | `Object` |
| `message.account` | ``null`` \| [`Account`](index.Account.md) |
| `message.user` | [`User`](index.User.md) |
| `message.isNewUser?` | `boolean` |
| `message.profile?` | [`Profile`](index.Profile.md) |

##### Returns

[`Awaitable`](../types/index.Awaitable.md)<`void`\>

___

### signOut

• **signOut**: (`message`: { `session`: [`Session`](index.Session.md) ; `token`: [`JWT`](jwt.JWT.md)  }) => [`Awaitable`](../types/index.Awaitable.md)<`void`\>

#### Type declaration

▸ (`message`): [`Awaitable`](../types/index.Awaitable.md)<`void`\>

The message object will contain one of these depending on
if you use JWT or database persisted sessions:
- `token`: The JWT token for this session.
- `session`: The session object from your adapter that is being ended.

##### Parameters

| Name | Type |
| :------ | :------ |
| `message` | `Object` |
| `message.session` | [`Session`](index.Session.md) |
| `message.token` | [`JWT`](jwt.JWT.md) |

##### Returns

[`Awaitable`](../types/index.Awaitable.md)<`void`\>

___

### updateUser

• **updateUser**: (`message`: { `user`: [`User`](index.User.md)  }) => [`Awaitable`](../types/index.Awaitable.md)<`void`\>

#### Type declaration

▸ (`message`): [`Awaitable`](../types/index.Awaitable.md)<`void`\>

##### Parameters

| Name | Type |
| :------ | :------ |
| `message` | `Object` |
| `message.user` | [`User`](index.User.md) |

##### Returns

[`Awaitable`](../types/index.Awaitable.md)<`void`\>

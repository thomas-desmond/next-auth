# Interface: EventCallbacks

The various event callbacks you can register for from next-auth

[Documentation](https://next-auth.js.org/configuration/events)

## Table of contents

### Properties

- [createUser](EventCallbacks.md#createuser)
- [linkAccount](EventCallbacks.md#linkaccount)
- [session](EventCallbacks.md#session)
- [signIn](EventCallbacks.md#signin)
- [signOut](EventCallbacks.md#signout)
- [updateUser](EventCallbacks.md#updateuser)

## Properties

### createUser

• **createUser**: (`message`: { `user`: [`User`](User.md)  }) => [`Awaitable`](../types/Awaitable.md)<`void`\>

#### Type declaration

▸ (`message`): [`Awaitable`](../types/Awaitable.md)<`void`\>

##### Parameters

| Name | Type |
| :------ | :------ |
| `message` | `Object` |
| `message.user` | [`User`](User.md) |

##### Returns

[`Awaitable`](../types/Awaitable.md)<`void`\>

___

### linkAccount

• **linkAccount**: (`message`: { `account`: [`Account`](Account.md) ; `profile`: [`User`](User.md) \| `AdapterUser` \| { `email`: `string`  } ; `user`: [`User`](User.md) \| `AdapterUser` \| { `email`: `string`  }  }) => [`Awaitable`](../types/Awaitable.md)<`void`\>

#### Type declaration

▸ (`message`): [`Awaitable`](../types/Awaitable.md)<`void`\>

##### Parameters

| Name | Type |
| :------ | :------ |
| `message` | `Object` |
| `message.account` | [`Account`](Account.md) |
| `message.profile` | [`User`](User.md) \| `AdapterUser` \| { `email`: `string`  } |
| `message.user` | [`User`](User.md) \| `AdapterUser` \| { `email`: `string`  } |

##### Returns

[`Awaitable`](../types/Awaitable.md)<`void`\>

___

### session

• **session**: (`message`: { `session`: [`Session`](Session.md) ; `token`: `JWT`  }) => [`Awaitable`](../types/Awaitable.md)<`void`\>

#### Type declaration

▸ (`message`): [`Awaitable`](../types/Awaitable.md)<`void`\>

The message object will contain one of these depending on
if you use JWT or database persisted sessions:
- `token`: The JWT token for this session.
- `session`: The session object from your adapter.

##### Parameters

| Name | Type |
| :------ | :------ |
| `message` | `Object` |
| `message.session` | [`Session`](Session.md) |
| `message.token` | `JWT` |

##### Returns

[`Awaitable`](../types/Awaitable.md)<`void`\>

___

### signIn

• **signIn**: (`message`: { `account`: ``null`` \| [`Account`](Account.md) ; `user`: [`User`](User.md) ; `isNewUser?`: `boolean` ; `profile?`: [`Profile`](Profile.md)  }) => [`Awaitable`](../types/Awaitable.md)<`void`\>

#### Type declaration

▸ (`message`): [`Awaitable`](../types/Awaitable.md)<`void`\>

If using a `credentials` type auth, the user is the raw response from your
credential provider.
For other providers, you'll get the User object from your adapter, the account,
and an indicator if the user was new to your Adapter.

##### Parameters

| Name | Type |
| :------ | :------ |
| `message` | `Object` |
| `message.account` | ``null`` \| [`Account`](Account.md) |
| `message.user` | [`User`](User.md) |
| `message.isNewUser?` | `boolean` |
| `message.profile?` | [`Profile`](Profile.md) |

##### Returns

[`Awaitable`](../types/Awaitable.md)<`void`\>

___

### signOut

• **signOut**: (`message`: { `session`: [`Session`](Session.md) ; `token`: `JWT`  }) => [`Awaitable`](../types/Awaitable.md)<`void`\>

#### Type declaration

▸ (`message`): [`Awaitable`](../types/Awaitable.md)<`void`\>

The message object will contain one of these depending on
if you use JWT or database persisted sessions:
- `token`: The JWT token for this session.
- `session`: The session object from your adapter that is being ended.

##### Parameters

| Name | Type |
| :------ | :------ |
| `message` | `Object` |
| `message.session` | [`Session`](Session.md) |
| `message.token` | `JWT` |

##### Returns

[`Awaitable`](../types/Awaitable.md)<`void`\>

___

### updateUser

• **updateUser**: (`message`: { `user`: [`User`](User.md)  }) => [`Awaitable`](../types/Awaitable.md)<`void`\>

#### Type declaration

▸ (`message`): [`Awaitable`](../types/Awaitable.md)<`void`\>

##### Parameters

| Name | Type |
| :------ | :------ |
| `message` | `Object` |
| `message.user` | [`User`](User.md) |

##### Returns

[`Awaitable`](../types/Awaitable.md)<`void`\>

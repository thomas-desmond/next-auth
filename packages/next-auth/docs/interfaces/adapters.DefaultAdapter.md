# Interface: DefaultAdapter

[adapters](../modules/adapters.md).DefaultAdapter

## Table of contents

### Properties

- [createSession](adapters.DefaultAdapter.md#createsession)
- [createUser](adapters.DefaultAdapter.md#createuser)
- [deleteSession](adapters.DefaultAdapter.md#deletesession)
- [getSessionAndUser](adapters.DefaultAdapter.md#getsessionanduser)
- [getUser](adapters.DefaultAdapter.md#getuser)
- [getUserByAccount](adapters.DefaultAdapter.md#getuserbyaccount)
- [getUserByEmail](adapters.DefaultAdapter.md#getuserbyemail)
- [linkAccount](adapters.DefaultAdapter.md#linkaccount)
- [updateSession](adapters.DefaultAdapter.md#updatesession)
- [updateUser](adapters.DefaultAdapter.md#updateuser)
- [createVerificationToken](adapters.DefaultAdapter.md#createverificationtoken)
- [deleteUser](adapters.DefaultAdapter.md#deleteuser)
- [unlinkAccount](adapters.DefaultAdapter.md#unlinkaccount)
- [useVerificationToken](adapters.DefaultAdapter.md#useverificationtoken)

## Properties

### createSession

• **createSession**: (`session`: { `expires`: `Date` ; `sessionToken`: `string` ; `userId`: `string`  }) => [`Awaitable`](../types/index.Awaitable.md)<[`AdapterSession`](adapters.AdapterSession.md)\>

#### Type declaration

▸ (`session`): [`Awaitable`](../types/index.Awaitable.md)<[`AdapterSession`](adapters.AdapterSession.md)\>

Creates a session for the user and returns it.

##### Parameters

| Name | Type |
| :------ | :------ |
| `session` | `Object` |
| `session.expires` | `Date` |
| `session.sessionToken` | `string` |
| `session.userId` | `string` |

##### Returns

[`Awaitable`](../types/index.Awaitable.md)<[`AdapterSession`](adapters.AdapterSession.md)\>

___

### createUser

• **createUser**: (`user`: `Omit`<[`AdapterUser`](adapters.AdapterUser.md), ``"id"``\>) => [`Awaitable`](../types/index.Awaitable.md)<[`AdapterUser`](adapters.AdapterUser.md)\>

#### Type declaration

▸ (`user`): [`Awaitable`](../types/index.Awaitable.md)<[`AdapterUser`](adapters.AdapterUser.md)\>

##### Parameters

| Name | Type |
| :------ | :------ |
| `user` | `Omit`<[`AdapterUser`](adapters.AdapterUser.md), ``"id"``\> |

##### Returns

[`Awaitable`](../types/index.Awaitable.md)<[`AdapterUser`](adapters.AdapterUser.md)\>

___

### deleteSession

• **deleteSession**: (`sessionToken`: `string`) => `Promise`<`void`\> \| [`Awaitable`](../types/index.Awaitable.md)<`undefined` \| ``null`` \| [`AdapterSession`](adapters.AdapterSession.md)\>

#### Type declaration

▸ (`sessionToken`): `Promise`<`void`\> \| [`Awaitable`](../types/index.Awaitable.md)<`undefined` \| ``null`` \| [`AdapterSession`](adapters.AdapterSession.md)\>

Deletes a session from the database.
It is preferred that this method also returns the session
that is being deleted for logging purposes.

##### Parameters

| Name | Type |
| :------ | :------ |
| `sessionToken` | `string` |

##### Returns

`Promise`<`void`\> \| [`Awaitable`](../types/index.Awaitable.md)<`undefined` \| ``null`` \| [`AdapterSession`](adapters.AdapterSession.md)\>

___

### getSessionAndUser

• **getSessionAndUser**: (`sessionToken`: `string`) => [`Awaitable`](../types/index.Awaitable.md)<``null`` \| { `session`: [`AdapterSession`](adapters.AdapterSession.md) ; `user`: [`AdapterUser`](adapters.AdapterUser.md)  }\>

#### Type declaration

▸ (`sessionToken`): [`Awaitable`](../types/index.Awaitable.md)<``null`` \| { `session`: [`AdapterSession`](adapters.AdapterSession.md) ; `user`: [`AdapterUser`](adapters.AdapterUser.md)  }\>

##### Parameters

| Name | Type |
| :------ | :------ |
| `sessionToken` | `string` |

##### Returns

[`Awaitable`](../types/index.Awaitable.md)<``null`` \| { `session`: [`AdapterSession`](adapters.AdapterSession.md) ; `user`: [`AdapterUser`](adapters.AdapterUser.md)  }\>

___

### getUser

• **getUser**: (`id`: `string`) => [`Awaitable`](../types/index.Awaitable.md)<``null`` \| [`AdapterUser`](adapters.AdapterUser.md)\>

#### Type declaration

▸ (`id`): [`Awaitable`](../types/index.Awaitable.md)<``null`` \| [`AdapterUser`](adapters.AdapterUser.md)\>

##### Parameters

| Name | Type |
| :------ | :------ |
| `id` | `string` |

##### Returns

[`Awaitable`](../types/index.Awaitable.md)<``null`` \| [`AdapterUser`](adapters.AdapterUser.md)\>

___

### getUserByAccount

• **getUserByAccount**: (`providerAccountId`: `Pick`<[`AdapterAccount`](adapters.AdapterAccount.md), ``"provider"`` \| ``"providerAccountId"``\>) => [`Awaitable`](../types/index.Awaitable.md)<``null`` \| [`AdapterUser`](adapters.AdapterUser.md)\>

#### Type declaration

▸ (`providerAccountId`): [`Awaitable`](../types/index.Awaitable.md)<``null`` \| [`AdapterUser`](adapters.AdapterUser.md)\>

Using the provider id and the id of the user for a specific account, get the user.

##### Parameters

| Name | Type |
| :------ | :------ |
| `providerAccountId` | `Pick`<[`AdapterAccount`](adapters.AdapterAccount.md), ``"provider"`` \| ``"providerAccountId"``\> |

##### Returns

[`Awaitable`](../types/index.Awaitable.md)<``null`` \| [`AdapterUser`](adapters.AdapterUser.md)\>

___

### getUserByEmail

• **getUserByEmail**: (`email`: `string`) => [`Awaitable`](../types/index.Awaitable.md)<``null`` \| [`AdapterUser`](adapters.AdapterUser.md)\>

#### Type declaration

▸ (`email`): [`Awaitable`](../types/index.Awaitable.md)<``null`` \| [`AdapterUser`](adapters.AdapterUser.md)\>

##### Parameters

| Name | Type |
| :------ | :------ |
| `email` | `string` |

##### Returns

[`Awaitable`](../types/index.Awaitable.md)<``null`` \| [`AdapterUser`](adapters.AdapterUser.md)\>

___

### linkAccount

• **linkAccount**: (`account`: [`AdapterAccount`](adapters.AdapterAccount.md)) => `Promise`<`void`\> \| [`Awaitable`](../types/index.Awaitable.md)<`undefined` \| ``null`` \| [`AdapterAccount`](adapters.AdapterAccount.md)\>

#### Type declaration

▸ (`account`): `Promise`<`void`\> \| [`Awaitable`](../types/index.Awaitable.md)<`undefined` \| ``null`` \| [`AdapterAccount`](adapters.AdapterAccount.md)\>

##### Parameters

| Name | Type |
| :------ | :------ |
| `account` | [`AdapterAccount`](adapters.AdapterAccount.md) |

##### Returns

`Promise`<`void`\> \| [`Awaitable`](../types/index.Awaitable.md)<`undefined` \| ``null`` \| [`AdapterAccount`](adapters.AdapterAccount.md)\>

___

### updateSession

• **updateSession**: (`session`: `Partial`<[`AdapterSession`](adapters.AdapterSession.md)\> & `Pick`<[`AdapterSession`](adapters.AdapterSession.md), ``"sessionToken"``\>) => [`Awaitable`](../types/index.Awaitable.md)<`undefined` \| ``null`` \| [`AdapterSession`](adapters.AdapterSession.md)\>

#### Type declaration

▸ (`session`): [`Awaitable`](../types/index.Awaitable.md)<`undefined` \| ``null`` \| [`AdapterSession`](adapters.AdapterSession.md)\>

##### Parameters

| Name | Type |
| :------ | :------ |
| `session` | `Partial`<[`AdapterSession`](adapters.AdapterSession.md)\> & `Pick`<[`AdapterSession`](adapters.AdapterSession.md), ``"sessionToken"``\> |

##### Returns

[`Awaitable`](../types/index.Awaitable.md)<`undefined` \| ``null`` \| [`AdapterSession`](adapters.AdapterSession.md)\>

___

### updateUser

• **updateUser**: (`user`: `Partial`<[`AdapterUser`](adapters.AdapterUser.md)\>) => [`Awaitable`](../types/index.Awaitable.md)<[`AdapterUser`](adapters.AdapterUser.md)\>

#### Type declaration

▸ (`user`): [`Awaitable`](../types/index.Awaitable.md)<[`AdapterUser`](adapters.AdapterUser.md)\>

##### Parameters

| Name | Type |
| :------ | :------ |
| `user` | `Partial`<[`AdapterUser`](adapters.AdapterUser.md)\> |

##### Returns

[`Awaitable`](../types/index.Awaitable.md)<[`AdapterUser`](adapters.AdapterUser.md)\>

___

### createVerificationToken

• `Optional` **createVerificationToken**: (`verificationToken`: [`VerificationToken`](adapters.VerificationToken.md)) => [`Awaitable`](../types/index.Awaitable.md)<`undefined` \| ``null`` \| [`VerificationToken`](adapters.VerificationToken.md)\>

#### Type declaration

▸ (`verificationToken`): [`Awaitable`](../types/index.Awaitable.md)<`undefined` \| ``null`` \| [`VerificationToken`](adapters.VerificationToken.md)\>

##### Parameters

| Name | Type |
| :------ | :------ |
| `verificationToken` | [`VerificationToken`](adapters.VerificationToken.md) |

##### Returns

[`Awaitable`](../types/index.Awaitable.md)<`undefined` \| ``null`` \| [`VerificationToken`](adapters.VerificationToken.md)\>

___

### deleteUser

• `Optional` **deleteUser**: (`userId`: `string`) => `Promise`<`void`\> \| [`Awaitable`](../types/index.Awaitable.md)<`undefined` \| ``null`` \| [`AdapterUser`](adapters.AdapterUser.md)\>

#### Type declaration

▸ (`userId`): `Promise`<`void`\> \| [`Awaitable`](../types/index.Awaitable.md)<`undefined` \| ``null`` \| [`AdapterUser`](adapters.AdapterUser.md)\>

**`Todo`**

Implement

##### Parameters

| Name | Type |
| :------ | :------ |
| `userId` | `string` |

##### Returns

`Promise`<`void`\> \| [`Awaitable`](../types/index.Awaitable.md)<`undefined` \| ``null`` \| [`AdapterUser`](adapters.AdapterUser.md)\>

___

### unlinkAccount

• `Optional` **unlinkAccount**: (`providerAccountId`: `Pick`<[`AdapterAccount`](adapters.AdapterAccount.md), ``"provider"`` \| ``"providerAccountId"``\>) => `Promise`<`void`\> \| [`Awaitable`](../types/index.Awaitable.md)<`undefined` \| [`AdapterAccount`](adapters.AdapterAccount.md)\>

#### Type declaration

▸ (`providerAccountId`): `Promise`<`void`\> \| [`Awaitable`](../types/index.Awaitable.md)<`undefined` \| [`AdapterAccount`](adapters.AdapterAccount.md)\>

**`Todo`**

Implement

##### Parameters

| Name | Type |
| :------ | :------ |
| `providerAccountId` | `Pick`<[`AdapterAccount`](adapters.AdapterAccount.md), ``"provider"`` \| ``"providerAccountId"``\> |

##### Returns

`Promise`<`void`\> \| [`Awaitable`](../types/index.Awaitable.md)<`undefined` \| [`AdapterAccount`](adapters.AdapterAccount.md)\>

___

### useVerificationToken

• `Optional` **useVerificationToken**: (`params`: { `identifier`: `string` ; `token`: `string`  }) => [`Awaitable`](../types/index.Awaitable.md)<``null`` \| [`VerificationToken`](adapters.VerificationToken.md)\>

#### Type declaration

▸ (`params`): [`Awaitable`](../types/index.Awaitable.md)<``null`` \| [`VerificationToken`](adapters.VerificationToken.md)\>

Return verification token from the database
and delete it so it cannot be used again.

##### Parameters

| Name | Type |
| :------ | :------ |
| `params` | `Object` |
| `params.identifier` | `string` |
| `params.token` | `string` |

##### Returns

[`Awaitable`](../types/index.Awaitable.md)<``null`` \| [`VerificationToken`](adapters.VerificationToken.md)\>

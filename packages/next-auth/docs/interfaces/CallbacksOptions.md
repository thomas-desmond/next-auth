# Interface: CallbacksOptions<P, A\>

[Documentation](https://next-auth.js.org/configuration/callbacks)

## Type parameters

| Name | Type |
| :------ | :------ |
| `P` | [`Profile`](Profile.md) |
| `A` | [`Account`](Account.md) |

## Table of contents

### Properties

- [jwt](CallbacksOptions.md#jwt)
- [redirect](CallbacksOptions.md#redirect)
- [session](CallbacksOptions.md#session)
- [signIn](CallbacksOptions.md#signin)

## Properties

### jwt

• **jwt**: (`params`: { `token`: `JWT` ; `account?`: ``null`` \| `A` ; `isNewUser?`: `boolean` ; `profile?`: `P` ; `user?`: [`User`](User.md) \| `AdapterUser`  }) => [`Awaitable`](../types/Awaitable.md)<`JWT`\>

#### Type declaration

▸ (`params`): [`Awaitable`](../types/Awaitable.md)<`JWT`\>

This callback is called whenever a JSON Web Token is created (i.e. at sign in)
or updated (i.e whenever a session is accessed in the client).
Its content is forwarded to the `session` callback,
where you can control what should be returned to the client.
Anything else will be kept from your front-end.

⚠ By default the JWT is signed, but not encrypted.

[Documentation](https://next-auth.js.org/configuration/callbacks#jwt-callback) |
[`session` callback](https://next-auth.js.org/configuration/callbacks#session-callback)

##### Parameters

| Name | Type |
| :------ | :------ |
| `params` | `Object` |
| `params.token` | `JWT` |
| `params.account?` | ``null`` \| `A` |
| `params.isNewUser?` | `boolean` |
| `params.profile?` | `P` |
| `params.user?` | [`User`](User.md) \| `AdapterUser` |

##### Returns

[`Awaitable`](../types/Awaitable.md)<`JWT`\>

___

### redirect

• **redirect**: (`params`: { `baseUrl`: `string` ; `url`: `string`  }) => [`Awaitable`](../types/Awaitable.md)<`string`\>

#### Type declaration

▸ (`params`): [`Awaitable`](../types/Awaitable.md)<`string`\>

This callback is called anytime the user is redirected to a callback URL (e.g. on signin or signout).
By default only URLs on the same URL as the site are allowed,
you can use this callback to customise that behaviour.

[Documentation](https://next-auth.js.org/configuration/callbacks#redirect-callback)

##### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `params` | `Object` | - |
| `params.baseUrl` | `string` | Default base URL of site (can be used as fallback) |
| `params.url` | `string` | URL provided as callback URL by the client |

##### Returns

[`Awaitable`](../types/Awaitable.md)<`string`\>

___

### session

• **session**: (`params`: { `session`: [`Session`](Session.md) ; `token`: `JWT` ; `user`: [`User`](User.md)  }) => [`Awaitable`](../types/Awaitable.md)<[`Session`](Session.md)\>

#### Type declaration

▸ (`params`): [`Awaitable`](../types/Awaitable.md)<[`Session`](Session.md)\>

This callback is called whenever a session is checked.
(Eg.: invoking the `/api/session` endpoint, using `useSession` or `getSession`)

⚠ By default, only a subset (email, name, image)
of the token is returned for increased security.

If you want to make something available you added to the token through the `jwt` callback,
you have to explicitly forward it here to make it available to the client.

[Documentation](https://next-auth.js.org/configuration/callbacks#session-callback) |
[`jwt` callback](https://next-auth.js.org/configuration/callbacks#jwt-callback) |
[`useSession`](https://next-auth.js.org/getting-started/client#usesession) |
[`getSession`](https://next-auth.js.org/getting-started/client#getsession) |

##### Parameters

| Name | Type |
| :------ | :------ |
| `params` | `Object` |
| `params.session` | [`Session`](Session.md) |
| `params.token` | `JWT` |
| `params.user` | [`User`](User.md) |

##### Returns

[`Awaitable`](../types/Awaitable.md)<[`Session`](Session.md)\>

___

### signIn

• **signIn**: (`params`: { `account`: ``null`` \| `A` ; `user`: [`User`](User.md) \| { `email`: `string`  } ; `credentials?`: `Record`<`string`, `CredentialInput`\> ; `email?`: { `verificationRequest?`: `boolean`  } ; `profile?`: `P`  }) => [`Awaitable`](../types/Awaitable.md)<`string` \| `boolean`\>

#### Type declaration

▸ (`params`): [`Awaitable`](../types/Awaitable.md)<`string` \| `boolean`\>

Use this callback to control if a user is allowed to sign in.
Returning true will continue the sign-in flow.
Throwing an error or returning a string will stop the flow, and redirect the user.

[Documentation](https://next-auth.js.org/configuration/callbacks#sign-in-callback)

##### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `params` | `Object` | - |
| `params.account` | ``null`` \| `A` | - |
| `params.user` | [`User`](User.md) \| { `email`: `string`  } | - |
| `params.credentials?` | `Record`<`string`, `CredentialInput`\> | If Credentials provider is used, it contains the user credentials |
| `params.email?` | `Object` | If Email provider is used, on the first call, it contains a `verificationRequest: true` property to indicate it is being triggered in the verification request flow. When the callback is invoked after a user has clicked on a sign in link, this property will not be present. You can check for the `verificationRequest` property to avoid sending emails to addresses or domains on a blocklist or to only explicitly generate them for email address in an allow list. |
| `params.email.verificationRequest?` | `boolean` | - |
| `params.profile?` | `P` | If OAuth provider is used, it contains the full OAuth profile returned by your provider. |

##### Returns

[`Awaitable`](../types/Awaitable.md)<`string` \| `boolean`\>

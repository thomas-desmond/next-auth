# Type alias: Adapter<WithVerificationToken\>

[adapters](../modules/adapters.md).Adapter

Ƭ **Adapter**<`WithVerificationToken`\>: [`DefaultAdapter`](../interfaces/adapters.DefaultAdapter.md) & `WithVerificationToken` extends ``true`` ? { `createVerificationToken`: (`verificationToken`: [`VerificationToken`](../interfaces/adapters.VerificationToken.md)) => [`Awaitable`](index.Awaitable.md)<[`VerificationToken`](../interfaces/adapters.VerificationToken.md) \| ``null`` \| `undefined`\> ; `useVerificationToken`: (`params`: { `identifier`: `string` ; `token`: `string`  }) => [`Awaitable`](index.Awaitable.md)<[`VerificationToken`](../interfaces/adapters.VerificationToken.md) \| ``null``\>  } : {}

Using a custom adapter you can connect to any database backend or even several different databases.
Custom adapters created and maintained by our community can be found in the adapters repository.
Feel free to add a custom adapter from your project to the repository,
or even become a maintainer of a certain adapter.
Custom adapters can still be created and used in a project without being added to the repository.

**Required methods**

_(These methods are required for all sign in flows)_
- `createUser`
- `getUser`
- `getUserByEmail`
- `getUserByAccount`
- `linkAccount`
- `createSession`
- `getSessionAndUser`
- `updateSession`
- `deleteSession`
- `updateUser`

_(Required to support email / passwordless sign in)_

- `createVerificationToken`
- `useVerificationToken`

**Unimplemented methods**

_(These methods will be required in a future release, but are not yet invoked)_
- `deleteUser`
- `unlinkAccount`

[Adapters Overview](https://next-auth.js.org/adapters/overview) |
[Create a custom adapter](https://next-auth.js.org/tutorials/creating-a-database-adapter)

#### Type parameters

| Name | Type |
| :------ | :------ |
| `WithVerificationToken` | `boolean` |

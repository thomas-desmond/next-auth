# Interface: AdapterAccount

[adapters](../modules/adapters.md).AdapterAccount

Usually contains information about the provider being used
and also extends `TokenSet`, which is different tokens returned by OAuth Providers.

## Hierarchy

- [`Account`](index.Account.md)

  ↳ **`AdapterAccount`**

## Table of contents

### Properties

- [provider](adapters.AdapterAccount.md#provider)
- [providerAccountId](adapters.AdapterAccount.md#provideraccountid)
- [type](adapters.AdapterAccount.md#type)
- [userId](adapters.AdapterAccount.md#userid)

## Properties

### provider

• **provider**: `string`

id of the provider used for this account

#### Inherited from

[Account](index.Account.md).[provider](index.Account.md#provider)

___

### providerAccountId

• **providerAccountId**: `string`

This value depends on the type of the provider being used to create the account.
- oauth: The OAuth account's id, returned from the `profile()` callback.
- email: The user's email address.
- credentials: `id` returned from the `authorize()` callback

#### Inherited from

[Account](index.Account.md).[providerAccountId](index.Account.md#provideraccountid)

___

### type

• **type**: `ProviderType`

Provider's type for this account

#### Inherited from

[Account](index.Account.md).[type](index.Account.md#type)

___

### userId

• **userId**: `string`

id of the user this account belongs to.

#### Overrides

[Account](index.Account.md).[userId](index.Account.md#userid)

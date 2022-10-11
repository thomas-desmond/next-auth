# Interface: Account

Usually contains information about the provider being used
and also extends `TokenSet`, which is different tokens returned by OAuth Providers.

## Hierarchy

- `Partial`<[`TokenSet`](../types/TokenSet.md)\>

  ↳ **`Account`**

## Table of contents

### Properties

- [provider](Account.md#provider)
- [providerAccountId](Account.md#provideraccountid)
- [type](Account.md#type)
- [userId](Account.md#userid)

## Properties

### provider

• **provider**: `string`

id of the provider used for this account

___

### providerAccountId

• **providerAccountId**: `string`

This value depends on the type of the provider being used to create the account.
- oauth: The OAuth account's id, returned from the `profile()` callback.
- email: The user's email address.
- credentials: `id` returned from the `authorize()` callback

___

### type

• **type**: `ProviderType`

Provider's type for this account

___

### userId

• `Optional` **userId**: `string`

id of the user this account belongs to.

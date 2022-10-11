# Interface: Account

[index](../modules/index.md).Account

Usually contains information about the provider being used
and also extends `TokenSet`, which is different tokens returned by OAuth Providers.

## Hierarchy

- `Partial`<[`TokenSet`](../types/index.TokenSet.md)\>

  ↳ **`Account`**

  ↳↳ [`AdapterAccount`](adapters.AdapterAccount.md)

## Table of contents

### Properties

- [provider](index.Account.md#provider)
- [providerAccountId](index.Account.md#provideraccountid)
- [type](index.Account.md#type)
- [userId](index.Account.md#userid)

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

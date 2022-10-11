# Interface: LoggerInstance

[index](../modules/index.md).LoggerInstance

Override any of the methods, and the rest will use the default logger.

[Documentation](https://next-auth.js.org/configuration/options#logger)

## Hierarchy

- `Record`<`string`, `Function`\>

  ↳ **`LoggerInstance`**

## Table of contents

### Properties

- [debug](index.LoggerInstance.md#debug)
- [error](index.LoggerInstance.md#error)
- [warn](index.LoggerInstance.md#warn)

## Properties

### debug

• **debug**: (`code`: `string`, `metadata`: `unknown`) => `void`

#### Type declaration

▸ (`code`, `metadata`): `void`

##### Parameters

| Name | Type |
| :------ | :------ |
| `code` | `string` |
| `metadata` | `unknown` |

##### Returns

`void`

___

### error

• **error**: (`code`: `string`, `metadata`: `Error` \| { `[key: string]`: `unknown`; `error`: `Error`  }) => `void`

#### Type declaration

▸ (`code`, `metadata`): `void`

##### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `code` | `string` | - |
| `metadata` | `Error` \| { `[key: string]`: `unknown`; `error`: `Error`  } | Either an instance of (JSON serializable) Error or an object that contains some debug information. (Error is still available through `metadata.error`) |

##### Returns

`void`

___

### warn

• **warn**: (`code`: `WarningCode`) => `void`

#### Type declaration

▸ (`code`): `void`

##### Parameters

| Name | Type |
| :------ | :------ |
| `code` | `WarningCode` |

##### Returns

`void`

# Function: getToken

[jwt](../modules/jwt.md).getToken

▸ **getToken**<`R`\>(`params`): `Promise`<`R` extends ``true`` ? `string` : [`JWT`](../interfaces/jwt.JWT.md) \| ``null``\>

Takes a NextAuth.js request (`req`) and returns either the NextAuth.js issued JWT's payload,
or the raw JWT string. We look for the JWT in the either the cookies, or the `Authorization` header.
[Documentation](https://next-auth.js.org/tutorials/securing-pages-and-api-routes#using-gettoken)

#### Type parameters

| Name | Type |
| :------ | :------ |
| `R` | extends `boolean` = ``false`` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `params` | [`GetTokenParams`](../interfaces/jwt.GetTokenParams.md)<`R`\> |

#### Returns

`Promise`<`R` extends ``true`` ? `string` : [`JWT`](../interfaces/jwt.JWT.md) \| ``null``\>

# Function: withAuth

[middleware](../modules/middleware.md).withAuth

▸ **withAuth**(...`args`): `Promise`<`NextMiddlewareResult`\> \| (...`args`: [request: NextRequestWithAuth, event: NextFetchEvent]) => `Promise`<`NextMiddlewareResult`\>

Middleware that checks if the user is authenticated/authorized.
If if they aren't, they will be redirected to the login page.
Otherwise, continue.

**`Example`**

```js
// `middleware.js`
export { default } from "next-auth/middleware"
```

---
[Documentation](https://next-auth.js.org/configuration/nextjs#middleware)

#### Parameters

| Name | Type |
| :------ | :------ |
| `...args` | [`WithAuthArgs`](../types/middleware.WithAuthArgs.md) |

#### Returns

`Promise`<`NextMiddlewareResult`\> \| (...`args`: [request: NextRequestWithAuth, event: NextFetchEvent]) => `Promise`<`NextMiddlewareResult`\>

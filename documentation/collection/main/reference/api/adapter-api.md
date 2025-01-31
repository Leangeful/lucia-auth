---
_order: 1
title: "Adapter API"
---

These can be imported from `lucia-auth/adapter`.

```ts
import { getUpdateData } from "lucia-auth/adapter";
```

## `getUpdateData()`

Takes the `data` argument of [`updateUser()`](/reference/adapters/api#updateuser) adapter method and converts it to `UserSchema` compatible object. Also removed keys with a value of undefined.

```ts
const getUpdateData: (data: {
	providerId?: string | null;
	hashedPassword?: string | null;
	attributes?: Record<string, any>;
}) => Partial<UserSchema>;
```

#### Parameter

| name | type                                                                |
| ---- | ------------------------------------------------------------------- |
| data | [`updateUser()`](/reference/adapters/api#updateuser)`.arguments[1]` |

#### Returns

| type                                                                        |
| --------------------------------------------------------------------------- |
| `Partial<`[`UserSchema`](/reference/adapters/database-model#schema-type)`>` |

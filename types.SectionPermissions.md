# Interface: SectionPermissions<T\>

[types](../wiki/types).SectionPermissions

Signer/agent permissions for a specific type

## Type parameters

| Name | Description |
| :------ | :------ |
| `T` | type of Permissions (Asset, Transaction, Portfolio, etc) |

## Hierarchy

- **`SectionPermissions`**

  ↳ [`TransactionPermissions`](../wiki/types.TransactionPermissions)

## Table of contents

### Properties

- [type](../wiki/types.SectionPermissions#type)
- [values](../wiki/types.SectionPermissions#values)

## Properties

### type

• **type**: [`PermissionType`](../wiki/types.PermissionType)

Whether the permissions are inclusive or exclusive

#### Defined in

[types/index.ts:900](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L900)

___

### values

• **values**: `T`[]

Values to be included/excluded

#### Defined in

[types/index.ts:896](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L896)

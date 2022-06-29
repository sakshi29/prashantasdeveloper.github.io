# Interface: TransactionPermissions

[types](../wiki/types).TransactionPermissions

Permissions related to Transactions. Can include/exclude individual transactions or entire modules

## Hierarchy

- [`SectionPermissions`](../wiki/types.SectionPermissions)<`TxTag` \| `ModuleName`\>

  ↳ **`TransactionPermissions`**

## Table of contents

### Properties

- [exceptions](../wiki/types.TransactionPermissions#exceptions)
- [type](../wiki/types.TransactionPermissions#type)
- [values](../wiki/types.TransactionPermissions#values)

## Properties

### exceptions

• `Optional` **exceptions**: `TxTag`[]

Transactions to be exempted from inclusion/exclusion. This allows more granularity when
  setting permissions. For example, let's say we want to include only the `asset` and `staking` modules,
  but exclude the `asset.registerTicker` transaction. We could add both modules to `values`, and add
  `TxTags.asset.registerTicker` to `exceptions`

#### Defined in

[types/index.ts:913](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L913)

___

### type

• **type**: [`PermissionType`](../wiki/types.PermissionType)

Whether the permissions are inclusive or exclusive

#### Inherited from

[SectionPermissions](../wiki/types.SectionPermissions).[type](../wiki/types.SectionPermissions#type)

#### Defined in

[types/index.ts:900](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L900)

___

### values

• **values**: (`TxTag` \| `ModuleName`)[]

Values to be included/excluded

#### Inherited from

[SectionPermissions](../wiki/types.SectionPermissions).[values](../wiki/types.SectionPermissions#values)

#### Defined in

[types/index.ts:896](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L896)

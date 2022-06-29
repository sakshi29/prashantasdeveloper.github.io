# Interface: Permissions

[types](../wiki/types).Permissions

Permissions a Secondary Key has over the Identity. A null value means the key has
  all permissions of that type (i.e. if `assets` is null, the key has permissions over all
  of the Identity's Assets)

## Table of contents

### Properties

- [assets](../wiki/types.Permissions#assets)
- [portfolios](../wiki/types.Permissions#portfolios)
- [transactionGroups](../wiki/types.Permissions#transactiongroups)
- [transactions](../wiki/types.Permissions#transactions)

## Properties

### assets

• **assets**: ``null`` \| [`SectionPermissions`](../wiki/types.SectionPermissions)<[`Asset`](../wiki/api.entities.Asset.Asset)\>

Assets over which this key has permissions

#### Defined in

[types/index.ts:925](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L925)

___

### portfolios

• **portfolios**: ``null`` \| [`SectionPermissions`](../wiki/types.SectionPermissions)<[`NumberedPortfolio`](../wiki/api.entities.NumberedPortfolio.NumberedPortfolio) \| [`DefaultPortfolio`](../wiki/api.entities.DefaultPortfolio.DefaultPortfolio)\>

#### Defined in

[types/index.ts:939](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L939)

___

### transactionGroups

• **transactionGroups**: [`TxGroup`](../wiki/types.TxGroup)[]

list of Transaction Groups this key can execute. Having permissions over a TxGroup
  means having permissions over every TxTag in said group. Partial group permissions are not
  covered by this value. For a full picture of transaction permissions, see the `transactions` property

NOTE: If transactions is null, ignore this value

#### Defined in

[types/index.ts:937](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L937)

___

### transactions

• **transactions**: ``null`` \| [`TransactionPermissions`](../wiki/types.TransactionPermissions)

Transactions this key can execute

#### Defined in

[types/index.ts:929](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/types/index.ts#L929)

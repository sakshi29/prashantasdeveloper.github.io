# Interface: SetPermissionGroupParams

[api/procedures/setPermissionGroup](../wiki/api.procedures.setPermissionGroup).SetPermissionGroupParams

This procedure can be called with:
  - An Asset's existing Custom Permission Group. The Identity will be assigned as an Agent of that Group for that Asset
  - A Known Permission Group and an Asset. The Identity will be assigned as an Agent of that Group for that Asset
  - A set of Transaction Permissions and an Asset. If there is no Custom Permission Group with those permissions, a Custom Permission Group will be created for that Asset with those permissions, and
    the Identity will be assigned as an Agent of that Group for that Asset. Otherwise, the existing Group will be used
  - An array of [Transaction Groups](../wiki/types.TxGroup) that represent a set of permissions. If there is no Custom Permission Group with those permissions, a Custom Permission Group will be created with those permissions, and
    the Identity will be assigned as an Agent of that Group for that Asset. Otherwise, the existing Group will be used

## Table of contents

### Properties

- [group](../wiki/api.procedures.setPermissionGroup.SetPermissionGroupParams#group)

## Properties

### group

• **group**: [`CustomPermissionGroup`](../wiki/api.entities.CustomPermissionGroup.CustomPermissionGroup) \| [`KnownPermissionGroup`](../wiki/api.entities.KnownPermissionGroup.KnownPermissionGroup) \| `TransactionsParams` \| `TxGroupParams`

#### Defined in

[api/procedures/setPermissionGroup.ts:53](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/procedures/setPermissionGroup.ts#L53)

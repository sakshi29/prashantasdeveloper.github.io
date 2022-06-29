# Class: TransferRestrictionBase<T\>

[api/entities/Asset/TransferRestrictions/TransferRestrictionBase](../wiki/api.entities.Asset.TransferRestrictions.TransferRestrictionBase).TransferRestrictionBase

Base class for managing Transfer Restrictions

## Type parameters

| Name | Type |
| :------ | :------ |
| `T` | extends [`TransferRestrictionType`](../wiki/types.TransferRestrictionType) |

## Hierarchy

- `Namespace`<[`Asset`](../wiki/api.entities.Asset.Asset)\>

  ↳ **`TransferRestrictionBase`**

  ↳↳ [`Count`](../wiki/api.entities.Asset.TransferRestrictions.Count.Count)

  ↳↳ [`Percentage`](../wiki/api.entities.Asset.TransferRestrictions.Percentage.Percentage)

## Table of contents

### Methods

- [addRestriction](../wiki/api.entities.Asset.TransferRestrictions.TransferRestrictionBase.TransferRestrictionBase#addrestriction)
- [get](../wiki/api.entities.Asset.TransferRestrictions.TransferRestrictionBase.TransferRestrictionBase#get)
- [removeRestrictions](../wiki/api.entities.Asset.TransferRestrictions.TransferRestrictionBase.TransferRestrictionBase#removerestrictions)
- [setRestrictions](../wiki/api.entities.Asset.TransferRestrictions.TransferRestrictionBase.TransferRestrictionBase#setrestrictions)

## Methods

### addRestriction

▸ **addRestriction**(`args`, `opts?`): `Promise`<`TransactionQueue`<`BigNumber`, `BigNumber`, `unknown`[][]\>\>

Add a Transfer Restriction of the corresponding type to this Asset

**`note`** the result is the total amount of restrictions after the procedure has run

**`note`** this method is of type [ProcedureMethod](../wiki/types.ProcedureMethod), which means you can call [addRestriction.checkAuthorization](../wiki/types.ProcedureMethod#checkauthorization)
  on it to see whether the signing Account and Identity have the required roles and permissions to run it

#### Parameters

| Name | Type |
| :------ | :------ |
| `args` | `AddRestrictionParams`<`T`\> |
| `opts?` | [`ProcedureOpts`](../wiki/types.ProcedureOpts) |

#### Returns

`Promise`<`TransactionQueue`<`BigNumber`, `BigNumber`, `unknown`[][]\>\>

#### Defined in

[api/entities/Asset/TransferRestrictions/TransferRestrictionBase.ts:128](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Asset/TransferRestrictions/TransferRestrictionBase.ts#L128)

___

### get

▸ **get**(): `Promise`<`GetReturnType`<`T`\>\>

Retrieve all active Transfer Restrictions of the corresponding type

**`note`** there is a maximum number of restrictions allowed across all types.
  The `availableSlots` property of the result represents how many more restrictions can be added
  before reaching that limit

#### Returns

`Promise`<`GetReturnType`<`T`\>\>

#### Defined in

[api/entities/Asset/TransferRestrictions/TransferRestrictionBase.ts:163](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Asset/TransferRestrictions/TransferRestrictionBase.ts#L163)

___

### removeRestrictions

▸ **removeRestrictions**(`opts?`): `Promise`<`TransactionQueue`<`BigNumber`, `BigNumber`, `unknown`[][]\>\>

Removes all Transfer Restrictions of the corresponding type from this Asset

**`note`** the result is the total amount of restrictions after the procedure has run

**`note`** this method is of type [NoArgsProcedureMethod](../wiki/types.NoArgsProcedureMethod), which means you can call [removeRestrictions.checkAuthorization](../wiki/types.NoArgsProcedureMethod#checkauthorization)
  on it to see whether the signing Account and Identity have the required roles and permissions to run it

#### Parameters

| Name | Type |
| :------ | :------ |
| `opts?` | [`ProcedureOpts`](../wiki/types.ProcedureOpts) |

#### Returns

`Promise`<`TransactionQueue`<`BigNumber`, `BigNumber`, `unknown`[][]\>\>

#### Defined in

[api/entities/Asset/TransferRestrictions/TransferRestrictionBase.ts:152](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Asset/TransferRestrictions/TransferRestrictionBase.ts#L152)

___

### setRestrictions

▸ **setRestrictions**(`args`, `opts?`): `Promise`<`TransactionQueue`<`BigNumber`, `BigNumber`, `unknown`[][]\>\>

Sets all Transfer Restrictions of the corresponding type on this Asset

**`note`** the result is the total amount of restrictions after the procedure has run

**`note`** this method is of type [ProcedureMethod](../wiki/types.ProcedureMethod), which means you can call [setRestrictions.checkAuthorization](../wiki/types.ProcedureMethod#checkauthorization)
  on it to see whether the signing Account and Identity have the required roles and permissions to run it

#### Parameters

| Name | Type |
| :------ | :------ |
| `args` | `SetRestrictionsParams`<`T`\> |
| `opts?` | [`ProcedureOpts`](../wiki/types.ProcedureOpts) |

#### Returns

`Promise`<`TransactionQueue`<`BigNumber`, `BigNumber`, `unknown`[][]\>\>

#### Defined in

[api/entities/Asset/TransferRestrictions/TransferRestrictionBase.ts:140](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Asset/TransferRestrictions/TransferRestrictionBase.ts#L140)

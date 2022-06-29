# Class: Count

[api/entities/Asset/TransferRestrictions/Count](../wiki/api.entities.Asset.TransferRestrictions.Count).Count

Handles all Count Transfer Restriction related functionality

## Hierarchy

- [`TransferRestrictionBase`](../wiki/api.entities.Asset.TransferRestrictions.TransferRestrictionBase.TransferRestrictionBase)<[`Count`](../wiki/types.TransferRestrictionType#count)\>

  ↳ **`Count`**

## Table of contents

### Properties

- [addRestriction](../wiki/api.entities.Asset.TransferRestrictions.Count.Count#addrestriction)
- [get](../wiki/api.entities.Asset.TransferRestrictions.Count.Count#get)
- [removeRestrictions](../wiki/api.entities.Asset.TransferRestrictions.Count.Count#removerestrictions)
- [setRestrictions](../wiki/api.entities.Asset.TransferRestrictions.Count.Count#setrestrictions)

## Properties

### addRestriction

• **addRestriction**: [`ProcedureMethod`](../wiki/types.ProcedureMethod)<`Omit`<[`AddCountTransferRestrictionParams`](../wiki/api.procedures.addTransferRestriction#addcounttransferrestrictionparams), ``"type"``\>, `BigNumber`, `BigNumber`\>

Add a Count Transfer Restriction to this Asset

**`note`** the result is the total amount of restrictions after the procedure has run

#### Overrides

[TransferRestrictionBase](../wiki/api.entities.Asset.TransferRestrictions.TransferRestrictionBase.TransferRestrictionBase).[addRestriction](../wiki/api.entities.Asset.TransferRestrictions.TransferRestrictionBase.TransferRestrictionBase#addrestriction)

#### Defined in

[api/entities/Asset/TransferRestrictions/Count.ts:27](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Asset/TransferRestrictions/Count.ts#L27)

___

### get

• **get**: () => `Promise`<[`ActiveTransferRestrictions`](../wiki/types.ActiveTransferRestrictions)<[`CountTransferRestriction`](../wiki/types.CountTransferRestriction)\>\>

#### Type declaration

▸ (): `Promise`<[`ActiveTransferRestrictions`](../wiki/types.ActiveTransferRestrictions)<[`CountTransferRestriction`](../wiki/types.CountTransferRestriction)\>\>

Retrieve all active Count Transfer Restrictions

**`note`** there is a maximum number of restrictions allowed across all types.
  The `availableSlots` property of the result represents how many more restrictions can be added
  before reaching that limit

##### Returns

`Promise`<[`ActiveTransferRestrictions`](../wiki/types.ActiveTransferRestrictions)<[`CountTransferRestriction`](../wiki/types.CountTransferRestriction)\>\>

#### Overrides

[TransferRestrictionBase](../wiki/api.entities.Asset.TransferRestrictions.TransferRestrictionBase.TransferRestrictionBase).[get](../wiki/api.entities.Asset.TransferRestrictions.TransferRestrictionBase.TransferRestrictionBase#get)

#### Defined in

[api/entities/Asset/TransferRestrictions/Count.ts:56](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Asset/TransferRestrictions/Count.ts#L56)

___

### removeRestrictions

• **removeRestrictions**: [`NoArgsProcedureMethod`](../wiki/types.NoArgsProcedureMethod)<`BigNumber`, `BigNumber`\>

Removes all Count Transfer Restrictions from this Asset

**`note`** the result is the total amount of restrictions after the procedure has run

#### Overrides

[TransferRestrictionBase](../wiki/api.entities.Asset.TransferRestrictions.TransferRestrictionBase.TransferRestrictionBase).[removeRestrictions](../wiki/api.entities.Asset.TransferRestrictions.TransferRestrictionBase.TransferRestrictionBase#removerestrictions)

#### Defined in

[api/entities/Asset/TransferRestrictions/Count.ts:47](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Asset/TransferRestrictions/Count.ts#L47)

___

### setRestrictions

• **setRestrictions**: [`ProcedureMethod`](../wiki/types.ProcedureMethod)<`Omit`<[`SetCountTransferRestrictionsParams`](../wiki/api.procedures.setTransferRestrictions.SetCountTransferRestrictionsParams), ``"type"``\>, `BigNumber`, `BigNumber`\>

Sets all Count Transfer Restrictions on this Asset

**`note`** the result is the total amount of restrictions after the procedure has run

#### Overrides

[TransferRestrictionBase](../wiki/api.entities.Asset.TransferRestrictions.TransferRestrictionBase.TransferRestrictionBase).[setRestrictions](../wiki/api.entities.Asset.TransferRestrictions.TransferRestrictionBase.TransferRestrictionBase#setrestrictions)

#### Defined in

[api/entities/Asset/TransferRestrictions/Count.ts:37](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Asset/TransferRestrictions/Count.ts#L37)

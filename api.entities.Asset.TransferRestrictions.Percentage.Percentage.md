# Class: Percentage

[api/entities/Asset/TransferRestrictions/Percentage](../wiki/api.entities.Asset.TransferRestrictions.Percentage).Percentage

Handles all Percentage Transfer Restriction related functionality

## Hierarchy

- [`TransferRestrictionBase`](../wiki/api.entities.Asset.TransferRestrictions.TransferRestrictionBase.TransferRestrictionBase)<[`Percentage`](../wiki/types.TransferRestrictionType#percentage)\>

  ↳ **`Percentage`**

## Table of contents

### Properties

- [addRestriction](../wiki/api.entities.Asset.TransferRestrictions.Percentage.Percentage#addrestriction)
- [get](../wiki/api.entities.Asset.TransferRestrictions.Percentage.Percentage#get)
- [removeRestrictions](../wiki/api.entities.Asset.TransferRestrictions.Percentage.Percentage#removerestrictions)
- [setRestrictions](../wiki/api.entities.Asset.TransferRestrictions.Percentage.Percentage#setrestrictions)

## Properties

### addRestriction

• **addRestriction**: [`ProcedureMethod`](../wiki/types.ProcedureMethod)<`Omit`<[`AddPercentageTransferRestrictionParams`](../wiki/api.procedures.addTransferRestriction#addpercentagetransferrestrictionparams), ``"type"``\>, `BigNumber`, `BigNumber`\>

Add a Percentage Transfer Restriction to this Asset

**`note`** the result is the total amount of restrictions after the procedure has run

#### Overrides

[TransferRestrictionBase](../wiki/api.entities.Asset.TransferRestrictions.TransferRestrictionBase.TransferRestrictionBase).[addRestriction](../wiki/api.entities.Asset.TransferRestrictions.TransferRestrictionBase.TransferRestrictionBase#addrestriction)

#### Defined in

[api/entities/Asset/TransferRestrictions/Percentage.ts:27](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Asset/TransferRestrictions/Percentage.ts#L27)

___

### get

• **get**: () => `Promise`<[`ActiveTransferRestrictions`](../wiki/types.ActiveTransferRestrictions)<[`PercentageTransferRestriction`](../wiki/types.PercentageTransferRestriction)\>\>

#### Type declaration

▸ (): `Promise`<[`ActiveTransferRestrictions`](../wiki/types.ActiveTransferRestrictions)<[`PercentageTransferRestriction`](../wiki/types.PercentageTransferRestriction)\>\>

Retrieve all active Percentage Transfer Restrictions

**`note`** there is a maximum number of restrictions allowed across all types.
  The `availableSlots` property of the result represents how many more restrictions can be added
  before reaching that limit

##### Returns

`Promise`<[`ActiveTransferRestrictions`](../wiki/types.ActiveTransferRestrictions)<[`PercentageTransferRestriction`](../wiki/types.PercentageTransferRestriction)\>\>

#### Overrides

[TransferRestrictionBase](../wiki/api.entities.Asset.TransferRestrictions.TransferRestrictionBase.TransferRestrictionBase).[get](../wiki/api.entities.Asset.TransferRestrictions.TransferRestrictionBase.TransferRestrictionBase#get)

#### Defined in

[api/entities/Asset/TransferRestrictions/Percentage.ts:56](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Asset/TransferRestrictions/Percentage.ts#L56)

___

### removeRestrictions

• **removeRestrictions**: [`NoArgsProcedureMethod`](../wiki/types.NoArgsProcedureMethod)<`BigNumber`, `BigNumber`\>

Removes all Percentage Transfer Restrictions from this Asset

**`note`** the result is the total amount of restrictions after the procedure has run

#### Overrides

[TransferRestrictionBase](../wiki/api.entities.Asset.TransferRestrictions.TransferRestrictionBase.TransferRestrictionBase).[removeRestrictions](../wiki/api.entities.Asset.TransferRestrictions.TransferRestrictionBase.TransferRestrictionBase#removerestrictions)

#### Defined in

[api/entities/Asset/TransferRestrictions/Percentage.ts:47](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Asset/TransferRestrictions/Percentage.ts#L47)

___

### setRestrictions

• **setRestrictions**: [`ProcedureMethod`](../wiki/types.ProcedureMethod)<`Omit`<[`SetPercentageTransferRestrictionsParams`](../wiki/api.procedures.setTransferRestrictions.SetPercentageTransferRestrictionsParams), ``"type"``\>, `BigNumber`, `BigNumber`\>

Sets all Percentage Transfer Restrictions on this Asset

**`note`** the result is the total amount of restrictions after the procedure has run

#### Overrides

[TransferRestrictionBase](../wiki/api.entities.Asset.TransferRestrictions.TransferRestrictionBase.TransferRestrictionBase).[setRestrictions](../wiki/api.entities.Asset.TransferRestrictions.TransferRestrictionBase.TransferRestrictionBase#setrestrictions)

#### Defined in

[api/entities/Asset/TransferRestrictions/Percentage.ts:37](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Asset/TransferRestrictions/Percentage.ts#L37)

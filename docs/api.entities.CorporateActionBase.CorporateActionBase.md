# Class: CorporateActionBase

[api/entities/CorporateActionBase](../wiki/api.entities.CorporateActionBase).CorporateActionBase

Represents an action initiated by the issuer of an Asset which may affect the positions of
  the Asset Holders

## Hierarchy

- [`Entity`](../wiki/api.entities.Entity.Entity)<[`UniqueIdentifiers`](../wiki/api.entities.CorporateActionBase.UniqueIdentifiers), `unknown`\>

  ↳ **`CorporateActionBase`**

  ↳↳ [`CorporateAction`](../wiki/api.entities.CorporateAction.CorporateAction)

  ↳↳ [`DividendDistribution`](../wiki/api.entities.DividendDistribution.DividendDistribution)

## Table of contents

### Properties

- [asset](../wiki/api.entities.CorporateActionBase.CorporateActionBase#asset)
- [declarationDate](../wiki/api.entities.CorporateActionBase.CorporateActionBase#declarationdate)
- [defaultTaxWithholding](../wiki/api.entities.CorporateActionBase.CorporateActionBase#defaulttaxwithholding)
- [description](../wiki/api.entities.CorporateActionBase.CorporateActionBase#description)
- [id](../wiki/api.entities.CorporateActionBase.CorporateActionBase#id)
- [targets](../wiki/api.entities.CorporateActionBase.CorporateActionBase#targets)
- [taxWithholdings](../wiki/api.entities.CorporateActionBase.CorporateActionBase#taxwithholdings)
- [uuid](../wiki/api.entities.CorporateActionBase.CorporateActionBase#uuid)

### Methods

- [checkpoint](../wiki/api.entities.CorporateActionBase.CorporateActionBase#checkpoint)
- [exists](../wiki/api.entities.CorporateActionBase.CorporateActionBase#exists)
- [isEqual](../wiki/api.entities.CorporateActionBase.CorporateActionBase#isequal)
- [linkDocuments](../wiki/api.entities.CorporateActionBase.CorporateActionBase#linkdocuments)
- [modifyCheckpoint](../wiki/api.entities.CorporateActionBase.CorporateActionBase#modifycheckpoint)
- [toHuman](../wiki/api.entities.CorporateActionBase.CorporateActionBase#tohuman)
- [generateUuid](../wiki/api.entities.CorporateActionBase.CorporateActionBase#generateuuid)
- [unserialize](../wiki/api.entities.CorporateActionBase.CorporateActionBase#unserialize)

## Properties

### asset

• **asset**: [`Asset`](../wiki/api.entities.Asset.Asset)

Asset affected by this Corporate Action

#### Defined in

[api/entities/CorporateActionBase/index.ts:77](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/CorporateActionBase/index.ts#L77)

___

### declarationDate

• **declarationDate**: `Date`

date at which the Corporate Action was created

#### Defined in

[api/entities/CorporateActionBase/index.ts:82](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/CorporateActionBase/index.ts#L82)

___

### defaultTaxWithholding

• **defaultTaxWithholding**: `BigNumber`

default percentage (0-100) of tax withholding for this Corporate Action

#### Defined in

[api/entities/CorporateActionBase/index.ts:98](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/CorporateActionBase/index.ts#L98)

___

### description

• **description**: `string`

brief text description of the Corporate Action

#### Defined in

[api/entities/CorporateActionBase/index.ts:87](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/CorporateActionBase/index.ts#L87)

___

### id

• **id**: `BigNumber`

internal Corporate Action ID

#### Defined in

[api/entities/CorporateActionBase/index.ts:72](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/CorporateActionBase/index.ts#L72)

___

### targets

• **targets**: [`CorporateActionTargets`](../wiki/api.entities.CorporateActionBase.types.CorporateActionTargets)

Asset Holder Identities related to this Corporate action. If the treatment is `Exclude`, the Identities
  in the array will not be targeted by the Action, Identities not in the array will be targeted, and vice versa

#### Defined in

[api/entities/CorporateActionBase/index.ts:93](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/CorporateActionBase/index.ts#L93)

___

### taxWithholdings

• **taxWithholdings**: [`TaxWithholding`](../wiki/api.entities.CorporateActionBase.types.TaxWithholding)[]

percentage (0-100) of tax withholding per Identity. Any Identity not present
  in this array uses the default tax withholding percentage

#### Defined in

[api/entities/CorporateActionBase/index.ts:104](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/CorporateActionBase/index.ts#L104)

___

### uuid

• **uuid**: `string`

#### Inherited from

[Entity](../wiki/api.entities.Entity.Entity).[uuid](../wiki/api.entities.Entity.Entity#uuid)

#### Defined in

[api/entities/Entity.ts:46](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Entity.ts#L46)

## Methods

### checkpoint

▸ **checkpoint**(): `Promise`<``null`` \| [`CheckpointSchedule`](../wiki/api.entities.CheckpointSchedule.CheckpointSchedule) \| [`Checkpoint`](../wiki/api.entities.Checkpoint.Checkpoint)\>

Retrieve the Checkpoint associated with this Corporate Action. If the Checkpoint is scheduled and has
  not been created yet, the corresponding CheckpointSchedule is returned instead. A null value means
  the Corporate Action was created without an associated Checkpoint

#### Returns

`Promise`<``null`` \| [`CheckpointSchedule`](../wiki/api.entities.CheckpointSchedule.CheckpointSchedule) \| [`Checkpoint`](../wiki/api.entities.Checkpoint.Checkpoint)\>

#### Defined in

[api/entities/CorporateActionBase/index.ts:183](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/CorporateActionBase/index.ts#L183)

___

### exists

▸ **exists**(): `Promise`<`boolean`\>

Determine whether this Corporate Action exists on chain

#### Returns

`Promise`<`boolean`\>

#### Overrides

[Entity](../wiki/api.entities.Entity.Entity).[exists](../wiki/api.entities.Entity.Entity#exists)

#### Defined in

[api/entities/CorporateActionBase/index.ts:172](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/CorporateActionBase/index.ts#L172)

___

### isEqual

▸ **isEqual**(`entity`): `boolean`

Determine whether this Entity is the same as another one

#### Parameters

| Name | Type |
| :------ | :------ |
| `entity` | [`Entity`](../wiki/api.entities.Entity.Entity)<`unknown`, `unknown`\> |

#### Returns

`boolean`

#### Inherited from

[Entity](../wiki/api.entities.Entity.Entity).[isEqual](../wiki/api.entities.Entity.Entity#isequal)

#### Defined in

[api/entities/Entity.ts:61](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Entity.ts#L61)

___

### linkDocuments

▸ **linkDocuments**(`args`, `opts?`): `Promise`<`TransactionQueue`<`void`, `void`, `unknown`[][]\>\>

Link a list of documents to this corporate action

**`note`** any previous links are removed in favor of the new list

**`note`** this method is of type [ProcedureMethod](../wiki/types.ProcedureMethod), which means you can call [linkDocuments.checkAuthorization](../wiki/types.ProcedureMethod#checkauthorization)
  on it to see whether the signing Account and Identity have the required roles and permissions to run it

#### Parameters

| Name | Type |
| :------ | :------ |
| `args` | [`LinkCaDocsParams`](../wiki/api.procedures.linkCaDocs.LinkCaDocsParams) |
| `opts?` | [`ProcedureOpts`](../wiki/types.ProcedureOpts) |

#### Returns

`Promise`<`TransactionQueue`<`void`, `void`, `unknown`[][]\>\>

#### Defined in

[api/entities/CorporateActionBase/index.ts:152](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/CorporateActionBase/index.ts#L152)

___

### modifyCheckpoint

▸ `Abstract` **modifyCheckpoint**(`args`, `opts?`): `Promise`<`TransactionQueue`<`void`, `void`, `unknown`[][]\>\>

Modify the Corporate Action's Checkpoint

**`note`** this method is of type [ProcedureMethod](../wiki/types.ProcedureMethod), which means you can call [modifyCheckpoint.checkAuthorization](../wiki/types.ProcedureMethod#checkauthorization)
  on it to see whether the signing Account and Identity have the required roles and permissions to run it

#### Parameters

| Name | Type |
| :------ | :------ |
| `args` | [`Modify`](../wiki/types.utils#modify)<`ModifyCaCheckpointParams`, { `checkpoint`: [`InputCaCheckpoint`](../wiki/api.entities.Asset.Checkpoints.types#inputcacheckpoint)  }\> |
| `opts?` | [`ProcedureOpts`](../wiki/types.ProcedureOpts) |

#### Returns

`Promise`<`TransactionQueue`<`void`, `void`, `unknown`[][]\>\>

#### Defined in

[api/entities/CorporateActionBase/index.ts:162](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/CorporateActionBase/index.ts#L162)

___

### toHuman

▸ **toHuman**(): [`HumanReadable`](../wiki/api.entities.CorporateActionBase.HumanReadable)

Return the Corporate Action's static data

#### Returns

[`HumanReadable`](../wiki/api.entities.CorporateActionBase.HumanReadable)

#### Overrides

[Entity](../wiki/api.entities.Entity.Entity).[toHuman](../wiki/api.entities.Entity.Entity#tohuman)

#### Defined in

[api/entities/CorporateActionBase/index.ts:262](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/CorporateActionBase/index.ts#L262)

___

### generateUuid

▸ `Static` **generateUuid**<`Identifiers`\>(`identifiers`): `string`

Generate the Entity's UUID from its identifying properties

#### Type parameters

| Name |
| :------ |
| `Identifiers` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `identifiers` | `Identifiers` |

#### Returns

`string`

#### Inherited from

[Entity](../wiki/api.entities.Entity.Entity).[generateUuid](../wiki/api.entities.Entity.Entity#generateuuid)

#### Defined in

[api/entities/Entity.ts:14](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Entity.ts#L14)

___

### unserialize

▸ `Static` **unserialize**<`Identifiers`\>(`serialized`): `Identifiers`

Unserialize a UUID into its Unique Identifiers

#### Type parameters

| Name |
| :------ |
| `Identifiers` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `serialized` | `string` | UUID to unserialize |

#### Returns

`Identifiers`

#### Inherited from

[Entity](../wiki/api.entities.Entity.Entity).[unserialize](../wiki/api.entities.Entity.Entity#unserialize)

#### Defined in

[api/entities/Entity.ts:23](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Entity.ts#L23)

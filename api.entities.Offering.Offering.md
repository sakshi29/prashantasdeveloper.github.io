# Class: Offering

[api/entities/Offering](../wiki/api.entities.Offering).Offering

Represents an Asset Offering in the Polymesh blockchain

## Hierarchy

- [`Entity`](../wiki/api.entities.Entity.Entity)<[`UniqueIdentifiers`](../wiki/api.entities.Offering.UniqueIdentifiers), `HumanReadable`\>

  ↳ **`Offering`**

## Table of contents

### Properties

- [asset](../wiki/api.entities.Offering.Offering#asset)
- [id](../wiki/api.entities.Offering.Offering#id)
- [uuid](../wiki/api.entities.Offering.Offering#uuid)

### Methods

- [close](../wiki/api.entities.Offering.Offering#close)
- [details](../wiki/api.entities.Offering.Offering#details)
- [exists](../wiki/api.entities.Offering.Offering#exists)
- [freeze](../wiki/api.entities.Offering.Offering#freeze)
- [getInvestments](../wiki/api.entities.Offering.Offering#getinvestments)
- [invest](../wiki/api.entities.Offering.Offering#invest)
- [isEqual](../wiki/api.entities.Offering.Offering#isequal)
- [modifyTimes](../wiki/api.entities.Offering.Offering#modifytimes)
- [toHuman](../wiki/api.entities.Offering.Offering#tohuman)
- [unfreeze](../wiki/api.entities.Offering.Offering#unfreeze)
- [generateUuid](../wiki/api.entities.Offering.Offering#generateuuid)
- [unserialize](../wiki/api.entities.Offering.Offering#unserialize)

## Properties

### asset

• **asset**: [`Asset`](../wiki/api.entities.Asset.Asset)

Asset being offered

#### Defined in

[api/entities/Offering/index.ts:66](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Offering/index.ts#L66)

___

### id

• **id**: `BigNumber`

identifier number of the Offering

#### Defined in

[api/entities/Offering/index.ts:61](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Offering/index.ts#L61)

___

### uuid

• **uuid**: `string`

#### Inherited from

[Entity](../wiki/api.entities.Entity.Entity).[uuid](../wiki/api.entities.Entity.Entity#uuid)

#### Defined in

[api/entities/Entity.ts:46](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Entity.ts#L46)

## Methods

### close

▸ **close**(`opts?`): `Promise`<`TransactionQueue`<`void`, `void`, `unknown`[][]\>\>

Close the Offering

**`note`** this method is of type [NoArgsProcedureMethod](../wiki/types.NoArgsProcedureMethod), which means you can call [close.checkAuthorization](../wiki/types.NoArgsProcedureMethod#checkauthorization)
  on it to see whether the signing Account and Identity have the required roles and permissions to run it

#### Parameters

| Name | Type |
| :------ | :------ |
| `opts?` | [`ProcedureOpts`](../wiki/types.ProcedureOpts) |

#### Returns

`Promise`<`TransactionQueue`<`void`, `void`, `unknown`[][]\>\>

#### Defined in

[api/entities/Offering/index.ts:159](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Offering/index.ts#L159)

___

### details

▸ **details**(): `Promise`<[`OfferingDetails`](../wiki/api.entities.Offering.types.OfferingDetails)\>

Retrieve the Offering's details

**`note`** can be subscribed to

#### Returns

`Promise`<[`OfferingDetails`](../wiki/api.entities.Offering.types.OfferingDetails)\>

#### Defined in

[api/entities/Offering/index.ts:112](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Offering/index.ts#L112)

▸ **details**(`callback`): `Promise`<[`UnsubCallback`](../wiki/types#unsubcallback)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `callback` | [`SubCallback`](../wiki/types#subcallback)<[`OfferingDetails`](../wiki/api.entities.Offering.types.OfferingDetails)\> |

#### Returns

`Promise`<[`UnsubCallback`](../wiki/types#unsubcallback)\>

#### Defined in

[api/entities/Offering/index.ts:113](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Offering/index.ts#L113)

___

### exists

▸ **exists**(): `Promise`<`boolean`\>

Determine whether this Offering exists on chain

#### Returns

`Promise`<`boolean`\>

#### Overrides

[Entity](../wiki/api.entities.Entity.Entity).[exists](../wiki/api.entities.Entity.Entity#exists)

#### Defined in

[api/entities/Offering/index.ts:278](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Offering/index.ts#L278)

___

### freeze

▸ **freeze**(`opts?`): `Promise`<`TransactionQueue`<[`Offering`](../wiki/api.entities.Offering.Offering), [`Offering`](../wiki/api.entities.Offering.Offering), `unknown`[][]\>\>

Freeze the Offering

**`note`** this method is of type [NoArgsProcedureMethod](../wiki/types.NoArgsProcedureMethod), which means you can call [freeze.checkAuthorization](../wiki/types.NoArgsProcedureMethod#checkauthorization)
  on it to see whether the signing Account and Identity have the required roles and permissions to run it

#### Parameters

| Name | Type |
| :------ | :------ |
| `opts?` | [`ProcedureOpts`](../wiki/types.ProcedureOpts) |

#### Returns

`Promise`<`TransactionQueue`<[`Offering`](../wiki/api.entities.Offering.Offering), [`Offering`](../wiki/api.entities.Offering.Offering), `unknown`[][]\>\>

#### Defined in

[api/entities/Offering/index.ts:169](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Offering/index.ts#L169)

___

### getInvestments

▸ **getInvestments**(`opts?`): `Promise`<[`ResultSet`](../wiki/types.ResultSet)<[`Investment`](../wiki/api.entities.Offering.types.Investment)\>\>

Retrieve all investments made on this Offering

**`note`** supports pagination

**`note`** uses the middleware

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `opts` | `Object` | - |
| `opts.size?` | `BigNumber` | page size |
| `opts.start?` | `BigNumber` | page offset |

#### Returns

`Promise`<[`ResultSet`](../wiki/types.ResultSet)<[`Investment`](../wiki/api.entities.Offering.types.Investment)\>\>

#### Defined in

[api/entities/Offering/index.ts:221](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Offering/index.ts#L221)

___

### invest

▸ **invest**(`args`, `opts?`): `Promise`<`TransactionQueue`<`void`, `void`, `unknown`[][]\>\>

Invest in the Offering

**`note`** required roles:
  - Purchase Portfolio Custodian
  - Funding Portfolio Custodian

**`note`** this method is of type [ProcedureMethod](../wiki/types.ProcedureMethod), which means you can call [invest.checkAuthorization](../wiki/types.ProcedureMethod#checkauthorization)
  on it to see whether the signing Account and Identity have the required roles and permissions to run it

#### Parameters

| Name | Type |
| :------ | :------ |
| `args` | [`InvestInOfferingParams`](../wiki/api.procedures.investInOffering.InvestInOfferingParams) |
| `opts?` | [`ProcedureOpts`](../wiki/types.ProcedureOpts) |

#### Returns

`Promise`<`TransactionQueue`<`void`, `void`, `unknown`[][]\>\>

#### Defined in

[api/entities/Offering/index.ts:208](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Offering/index.ts#L208)

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

### modifyTimes

▸ **modifyTimes**(`args`, `opts?`): `Promise`<`TransactionQueue`<`void`, `void`, `unknown`[][]\>\>

Modify the start/end time of the Offering

**`throws`** if:
  - Trying to modify the start time on an Offering that already started
  - Trying to modify anything on an Offering that already ended
  - Trying to change start or end time to a past date

**`note`** this method is of type [ProcedureMethod](../wiki/types.ProcedureMethod), which means you can call [modifyTimes.checkAuthorization](../wiki/types.ProcedureMethod#checkauthorization)
  on it to see whether the signing Account and Identity have the required roles and permissions to run it

#### Parameters

| Name | Type |
| :------ | :------ |
| `args` | [`ModifyOfferingTimesParams`](../wiki/api.procedures.modifyOfferingTimes#modifyofferingtimesparams) |
| `opts?` | [`ProcedureOpts`](../wiki/types.ProcedureOpts) |

#### Returns

`Promise`<`TransactionQueue`<`void`, `void`, `unknown`[][]\>\>

#### Defined in

[api/entities/Offering/index.ts:194](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Offering/index.ts#L194)

___

### toHuman

▸ **toHuman**(): `HumanReadable`

Return the Offering's ID and Asset ticker

#### Returns

`HumanReadable`

#### Overrides

[Entity](../wiki/api.entities.Entity.Entity).[toHuman](../wiki/api.entities.Entity.Entity#tohuman)

#### Defined in

[api/entities/Offering/index.ts:296](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Offering/index.ts#L296)

___

### unfreeze

▸ **unfreeze**(`opts?`): `Promise`<`TransactionQueue`<[`Offering`](../wiki/api.entities.Offering.Offering), [`Offering`](../wiki/api.entities.Offering.Offering), `unknown`[][]\>\>

Unfreeze the Offering

**`note`** this method is of type [NoArgsProcedureMethod](../wiki/types.NoArgsProcedureMethod), which means you can call [unfreeze.checkAuthorization](../wiki/types.NoArgsProcedureMethod#checkauthorization)
  on it to see whether the signing Account and Identity have the required roles and permissions to run it

#### Parameters

| Name | Type |
| :------ | :------ |
| `opts?` | [`ProcedureOpts`](../wiki/types.ProcedureOpts) |

#### Returns

`Promise`<`TransactionQueue`<[`Offering`](../wiki/api.entities.Offering.Offering), [`Offering`](../wiki/api.entities.Offering.Offering), `unknown`[][]\>\>

#### Defined in

[api/entities/Offering/index.ts:179](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Offering/index.ts#L179)

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

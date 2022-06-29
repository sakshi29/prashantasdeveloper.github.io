# Class: Venue

[api/entities/Venue](../wiki/api.entities.Venue).Venue

Represents a Venue through which settlements are handled

## Hierarchy

- [`Entity`](../wiki/api.entities.Entity.Entity)<[`UniqueIdentifiers`](../wiki/api.entities.Venue.UniqueIdentifiers), `string`\>

  ↳ **`Venue`**

## Table of contents

### Properties

- [id](../wiki/api.entities.Venue.Venue#id)
- [uuid](../wiki/api.entities.Venue.Venue#uuid)

### Methods

- [addInstruction](../wiki/api.entities.Venue.Venue#addinstruction)
- [addInstructions](../wiki/api.entities.Venue.Venue#addinstructions)
- [details](../wiki/api.entities.Venue.Venue#details)
- [exists](../wiki/api.entities.Venue.Venue#exists)
- [getInstructions](../wiki/api.entities.Venue.Venue#getinstructions)
- [getPendingInstructions](../wiki/api.entities.Venue.Venue#getpendinginstructions)
- [isEqual](../wiki/api.entities.Venue.Venue#isequal)
- [modify](../wiki/api.entities.Venue.Venue#modify)
- [toHuman](../wiki/api.entities.Venue.Venue#tohuman)
- [generateUuid](../wiki/api.entities.Venue.Venue#generateuuid)
- [unserialize](../wiki/api.entities.Venue.Venue#unserialize)

## Properties

### id

• **id**: `BigNumber`

identifier number of the Venue

#### Defined in

[api/entities/Venue/index.ts:57](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Venue/index.ts#L57)

___

### uuid

• **uuid**: `string`

#### Inherited from

[Entity](../wiki/api.entities.Entity.Entity).[uuid](../wiki/api.entities.Entity.Entity#uuid)

#### Defined in

[api/entities/Entity.ts:46](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Entity.ts#L46)

## Methods

### addInstruction

▸ **addInstruction**(`args`, `opts?`): `Promise`<`TransactionQueue`<[`Instruction`](../wiki/api.entities.Instruction.Instruction)[], [`Instruction`](../wiki/api.entities.Instruction.Instruction), `unknown`[][]\>\>

Creates a settlement Instruction in this Venue

**`note`** required role:
  - Venue Owner

**`note`** this method is of type [ProcedureMethod](../wiki/types.ProcedureMethod), which means you can call [addInstruction.checkAuthorization](../wiki/types.ProcedureMethod#checkauthorization)
  on it to see whether the signing Account and Identity have the required roles and permissions to run it

#### Parameters

| Name | Type |
| :------ | :------ |
| `args` | [`AddInstructionParams`](../wiki/api.procedures.addInstruction.AddInstructionParams) |
| `opts?` | [`ProcedureOpts`](../wiki/types.ProcedureOpts) |

#### Returns

`Promise`<`TransactionQueue`<[`Instruction`](../wiki/api.entities.Instruction.Instruction)[], [`Instruction`](../wiki/api.entities.Instruction.Instruction), `unknown`[][]\>\>

#### Defined in

[api/entities/Venue/index.ts:214](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Venue/index.ts#L214)

___

### addInstructions

▸ **addInstructions**(`args`, `opts?`): `Promise`<`TransactionQueue`<[`Instruction`](../wiki/api.entities.Instruction.Instruction)[], [`Instruction`](../wiki/api.entities.Instruction.Instruction)[], `unknown`[][]\>\>

Creates a batch of settlement Instructions in this Venue

**`note`** required role:
  - Venue Owner

**`note`** this method is of type [ProcedureMethod](../wiki/types.ProcedureMethod), which means you can call [addInstructions.checkAuthorization](../wiki/types.ProcedureMethod#checkauthorization)
  on it to see whether the signing Account and Identity have the required roles and permissions to run it

#### Parameters

| Name | Type |
| :------ | :------ |
| `args` | [`AddInstructionsParams`](../wiki/api.procedures.addInstruction.AddInstructionsParams) |
| `opts?` | [`ProcedureOpts`](../wiki/types.ProcedureOpts) |

#### Returns

`Promise`<`TransactionQueue`<[`Instruction`](../wiki/api.entities.Instruction.Instruction)[], [`Instruction`](../wiki/api.entities.Instruction.Instruction)[], `unknown`[][]\>\>

#### Defined in

[api/entities/Venue/index.ts:227](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Venue/index.ts#L227)

___

### details

▸ **details**(): `Promise`<[`VenueDetails`](../wiki/api.entities.Venue.types.VenueDetails)\>

Retrieve information specific to this Venue

#### Returns

`Promise`<[`VenueDetails`](../wiki/api.entities.Venue.types.VenueDetails)\>

#### Defined in

[api/entities/Venue/index.ts:110](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Venue/index.ts#L110)

___

### exists

▸ **exists**(): `Promise`<`boolean`\>

Determine whether this Venue exists on chain

#### Returns

`Promise`<`boolean`\>

#### Overrides

[Entity](../wiki/api.entities.Entity.Entity).[exists](../wiki/api.entities.Entity.Entity#exists)

#### Defined in

[api/entities/Venue/index.ts:91](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Venue/index.ts#L91)

___

### getInstructions

▸ **getInstructions**(): `Promise`<`Pick`<[`GroupedInstructions`](../wiki/types.GroupedInstructions), ``"pending"`` \| ``"failed"``\>\>

Retrieve all pending and failed Instructions in this Venue

#### Returns

`Promise`<`Pick`<[`GroupedInstructions`](../wiki/types.GroupedInstructions), ``"pending"`` \| ``"failed"``\>\>

#### Defined in

[api/entities/Venue/index.ts:139](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Venue/index.ts#L139)

___

### getPendingInstructions

▸ **getPendingInstructions**(): `Promise`<[`Instruction`](../wiki/api.entities.Instruction.Instruction)[]\>

Retrieve all pending Instructions in this Venue

**`deprecated`** in favor of `getInstructions`

#### Returns

`Promise`<[`Instruction`](../wiki/api.entities.Instruction.Instruction)[]\>

#### Defined in

[api/entities/Venue/index.ts:168](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Venue/index.ts#L168)

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

### modify

▸ **modify**(`args`, `opts?`): `Promise`<`TransactionQueue`<`void`, `void`, `unknown`[][]\>\>

Modify description and type

**`note`** required role:
  - Venue Owner

**`note`** this method is of type [ProcedureMethod](../wiki/types.ProcedureMethod), which means you can call [modify.checkAuthorization](../wiki/types.ProcedureMethod#checkauthorization)
  on it to see whether the signing Account and Identity have the required roles and permissions to run it

#### Parameters

| Name | Type |
| :------ | :------ |
| `args` | [`ModifyVenueParams`](../wiki/api.procedures.modifyVenue#modifyvenueparams) |
| `opts?` | [`ProcedureOpts`](../wiki/types.ProcedureOpts) |

#### Returns

`Promise`<`TransactionQueue`<`void`, `void`, `unknown`[][]\>\>

#### Defined in

[api/entities/Venue/index.ts:240](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Venue/index.ts#L240)

___

### toHuman

▸ **toHuman**(): `string`

Return the Venue's ID

#### Returns

`string`

#### Overrides

[Entity](../wiki/api.entities.Entity.Entity).[toHuman](../wiki/api.entities.Entity.Entity#tohuman)

#### Defined in

[api/entities/Venue/index.ts:247](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Venue/index.ts#L247)

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

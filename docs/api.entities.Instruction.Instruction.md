# Class: Instruction

[api/entities/Instruction](../wiki/api.entities.Instruction).Instruction

Represents a settlement Instruction to be executed on a certain Venue

## Hierarchy

- [`Entity`](../wiki/api.entities.Entity.Entity)<[`UniqueIdentifiers`](../wiki/api.entities.Instruction.UniqueIdentifiers), `string`\>

  ↳ **`Instruction`**

## Table of contents

### Properties

- [id](../wiki/api.entities.Instruction.Instruction#id)
- [uuid](../wiki/api.entities.Instruction.Instruction#uuid)

### Methods

- [affirm](../wiki/api.entities.Instruction.Instruction#affirm)
- [details](../wiki/api.entities.Instruction.Instruction#details)
- [exists](../wiki/api.entities.Instruction.Instruction#exists)
- [getAffirmations](../wiki/api.entities.Instruction.Instruction#getaffirmations)
- [getLegs](../wiki/api.entities.Instruction.Instruction#getlegs)
- [getStatus](../wiki/api.entities.Instruction.Instruction#getstatus)
- [isEqual](../wiki/api.entities.Instruction.Instruction#isequal)
- [isExecuted](../wiki/api.entities.Instruction.Instruction#isexecuted)
- [isPending](../wiki/api.entities.Instruction.Instruction#ispending)
- [reject](../wiki/api.entities.Instruction.Instruction#reject)
- [reschedule](../wiki/api.entities.Instruction.Instruction#reschedule)
- [toHuman](../wiki/api.entities.Instruction.Instruction#tohuman)
- [withdraw](../wiki/api.entities.Instruction.Instruction#withdraw)
- [generateUuid](../wiki/api.entities.Instruction.Instruction#generateuuid)
- [unserialize](../wiki/api.entities.Instruction.Instruction#unserialize)

## Properties

### id

• **id**: `BigNumber`

Identifier number of the venue

#### Defined in

[api/entities/Instruction/index.ts:77](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Instruction/index.ts#L77)

___

### uuid

• **uuid**: `string`

#### Inherited from

[Entity](../wiki/api.entities.Entity.Entity).[uuid](../wiki/api.entities.Entity.Entity#uuid)

#### Defined in

[api/entities/Entity.ts:46](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Entity.ts#L46)

## Methods

### affirm

▸ **affirm**(`opts?`): `Promise`<`TransactionQueue`<[`Instruction`](../wiki/api.entities.Instruction.Instruction), [`Instruction`](../wiki/api.entities.Instruction.Instruction), `unknown`[][]\>\>

Affirm this instruction (authorize)

**`note`** this method is of type [NoArgsProcedureMethod](../wiki/types.NoArgsProcedureMethod), which means you can call [affirm.checkAuthorization](../wiki/types.NoArgsProcedureMethod#checkauthorization)
  on it to see whether the signing Account and Identity have the required roles and permissions to run it

#### Parameters

| Name | Type |
| :------ | :------ |
| `opts?` | [`ProcedureOpts`](../wiki/types.ProcedureOpts) |

#### Returns

`Promise`<`TransactionQueue`<[`Instruction`](../wiki/api.entities.Instruction.Instruction), [`Instruction`](../wiki/api.entities.Instruction.Instruction), `unknown`[][]\>\>

#### Defined in

[api/entities/Instruction/index.ts:406](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Instruction/index.ts#L406)

___

### details

▸ **details**(): `Promise`<[`InstructionDetails`](../wiki/api.entities.Instruction.types#instructiondetails)\>

Retrieve information specific to this Instruction

#### Returns

`Promise`<[`InstructionDetails`](../wiki/api.entities.Instruction.types#instructiondetails)\>

#### Defined in

[api/entities/Instruction/index.ts:198](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Instruction/index.ts#L198)

___

### exists

▸ **exists**(): `Promise`<`boolean`\>

Determine whether this Instruction exists on chain (or existed and was pruned)

#### Returns

`Promise`<`boolean`\>

#### Overrides

[Entity](../wiki/api.entities.Entity.Entity).[exists](../wiki/api.entities.Entity.Entity#exists)

#### Defined in

[api/entities/Instruction/index.ts:180](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Instruction/index.ts#L180)

___

### getAffirmations

▸ **getAffirmations**(`paginationOpts?`): `Promise`<[`ResultSet`](../wiki/types.ResultSet)<[`InstructionAffirmation`](../wiki/api.entities.Instruction.types.InstructionAffirmation)\>\>

Retrieve every authorization generated by this Instruction (status and authorizing Identity)

**`note`** supports pagination

#### Parameters

| Name | Type |
| :------ | :------ |
| `paginationOpts?` | [`PaginationOptions`](../wiki/types.PaginationOptions) |

#### Returns

`Promise`<[`ResultSet`](../wiki/types.ResultSet)<[`InstructionAffirmation`](../wiki/api.entities.Instruction.types.InstructionAffirmation)\>\>

#### Defined in

[api/entities/Instruction/index.ts:257](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Instruction/index.ts#L257)

___

### getLegs

▸ **getLegs**(`paginationOpts?`): `Promise`<[`ResultSet`](../wiki/types.ResultSet)<[`Leg`](../wiki/api.entities.Instruction.types.Leg)\>\>

Retrieve all legs of this Instruction

**`note`** supports pagination

#### Parameters

| Name | Type |
| :------ | :------ |
| `paginationOpts?` | [`PaginationOptions`](../wiki/types.PaginationOptions) |

#### Returns

`Promise`<[`ResultSet`](../wiki/types.ResultSet)<[`Leg`](../wiki/api.entities.Instruction.types.Leg)\>\>

#### Defined in

[api/entities/Instruction/index.ts:303](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Instruction/index.ts#L303)

___

### getStatus

▸ **getStatus**(): `Promise`<[`InstructionStatusResult`](../wiki/api.entities.Instruction.types#instructionstatusresult)\>

Retrieve current status of this Instruction

**`note`** uses the middleware

#### Returns

`Promise`<[`InstructionStatusResult`](../wiki/api.entities.Instruction.types#instructionstatusresult)\>

#### Defined in

[api/entities/Instruction/index.ts:354](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Instruction/index.ts#L354)

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

### isExecuted

▸ **isExecuted**(): `Promise`<`boolean`\>

Retrieve whether the Instruction has already been executed and pruned from
  the chain.

#### Returns

`Promise`<`boolean`\>

#### Defined in

[api/entities/Instruction/index.ts:135](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Instruction/index.ts#L135)

___

### isPending

▸ **isPending**(): `Promise`<`boolean`\>

Retrieve whether the Instruction is still pending on chain

#### Returns

`Promise`<`boolean`\>

#### Defined in

[api/entities/Instruction/index.ts:159](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Instruction/index.ts#L159)

___

### reject

▸ **reject**(`opts?`): `Promise`<`TransactionQueue`<[`Instruction`](../wiki/api.entities.Instruction.Instruction), [`Instruction`](../wiki/api.entities.Instruction.Instruction), `unknown`[][]\>\>

Reject this instruction

**`note`** reject on `SettleOnAffirmation` will execute the settlement and it will fail immediately.

**`note`** reject on `SettleOnBlock` behaves just like unauthorize

**`note`** this method is of type [NoArgsProcedureMethod](../wiki/types.NoArgsProcedureMethod), which means you can call [reject.checkAuthorization](../wiki/types.NoArgsProcedureMethod#checkauthorization)
  on it to see whether the signing Account and Identity have the required roles and permissions to run it

#### Parameters

| Name | Type |
| :------ | :------ |
| `opts?` | [`ProcedureOpts`](../wiki/types.ProcedureOpts) |

#### Returns

`Promise`<`TransactionQueue`<[`Instruction`](../wiki/api.entities.Instruction.Instruction), [`Instruction`](../wiki/api.entities.Instruction.Instruction), `unknown`[][]\>\>

#### Defined in

[api/entities/Instruction/index.ts:396](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Instruction/index.ts#L396)

___

### reschedule

▸ **reschedule**(`opts?`): `Promise`<`TransactionQueue`<[`Instruction`](../wiki/api.entities.Instruction.Instruction), [`Instruction`](../wiki/api.entities.Instruction.Instruction), `unknown`[][]\>\>

Reschedules a failed Instruction to be tried again

**`throws`** if the Instruction status is not `InstructionStatus.Failed`

**`note`** this method is of type [NoArgsProcedureMethod](../wiki/types.NoArgsProcedureMethod), which means you can call [reschedule.checkAuthorization](../wiki/types.NoArgsProcedureMethod#checkauthorization)
  on it to see whether the signing Account and Identity have the required roles and permissions to run it

#### Parameters

| Name | Type |
| :------ | :------ |
| `opts?` | [`ProcedureOpts`](../wiki/types.ProcedureOpts) |

#### Returns

`Promise`<`TransactionQueue`<[`Instruction`](../wiki/api.entities.Instruction.Instruction), [`Instruction`](../wiki/api.entities.Instruction.Instruction), `unknown`[][]\>\>

#### Defined in

[api/entities/Instruction/index.ts:428](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Instruction/index.ts#L428)

___

### toHuman

▸ **toHuman**(): `string`

Return the Instruction's ID

#### Returns

`string`

#### Overrides

[Entity](../wiki/api.entities.Entity.Entity).[toHuman](../wiki/api.entities.Entity.Entity#tohuman)

#### Defined in

[api/entities/Instruction/index.ts:457](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Instruction/index.ts#L457)

___

### withdraw

▸ **withdraw**(`opts?`): `Promise`<`TransactionQueue`<[`Instruction`](../wiki/api.entities.Instruction.Instruction), [`Instruction`](../wiki/api.entities.Instruction.Instruction), `unknown`[][]\>\>

Withdraw affirmation from this instruction (unauthorize)

**`note`** this method is of type [NoArgsProcedureMethod](../wiki/types.NoArgsProcedureMethod), which means you can call [withdraw.checkAuthorization](../wiki/types.NoArgsProcedureMethod#checkauthorization)
  on it to see whether the signing Account and Identity have the required roles and permissions to run it

#### Parameters

| Name | Type |
| :------ | :------ |
| `opts?` | [`ProcedureOpts`](../wiki/types.ProcedureOpts) |

#### Returns

`Promise`<`TransactionQueue`<[`Instruction`](../wiki/api.entities.Instruction.Instruction), [`Instruction`](../wiki/api.entities.Instruction.Instruction), `unknown`[][]\>\>

#### Defined in

[api/entities/Instruction/index.ts:416](https://github.com/PolymathNetwork/polymesh-sdk/blob/31dfa0dc/src/api/entities/Instruction/index.ts#L416)

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